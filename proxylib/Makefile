include ../Makefile.quiet
include ../Makefile.defs

PROXYLIB_GOLDFLAGS=$(GOLDFLAGS) -extldflags -Wl,-soname,libcilium.so.$(VERSION_MAJOR)
PROXYLIB_GOBUILD=-ldflags '$(PROXYLIB_GOLDFLAGS)'

TARGET=libcilium.so
DEPS := $(shell find ../pkg accesslog npds test . \( -name '*.go' ! -name '*_test.go' \))
$(TARGET): $(DEPS)
	@$(ECHO_GO)
	$(QUIET)$(_GO) build $(GOBUILD) $(PROXYLIB_GOBUILD) -o $@.$(VERSION_MAJOR) -buildmode=c-shared
	$(QUIET)ln -sf $@.$(VERSION_MAJOR) $@ || cp $@.$(VERSION_MAJOR) $@

all: $(TARGET)

clean:
	@$(ECHO_CLEAN)
	-$(QUIET)rm -f $(TARGET)
	$(QUIET)$(_GO) clean $(GOCLEAN)

install:
	$(QUIET)$(INSTALL) -m 0755 -d $(DESTDIR)$(LIBDIR)
	$(QUIET)$(INSTALL) -m 0755 $(TARGET).$(VERSION_MAJOR) $(DESTDIR)$(LIBDIR)
	ln -sf $(TARGET).$(VERSION_MAJOR) $(DESTDIR)$(LIBDIR)/$(TARGET)
