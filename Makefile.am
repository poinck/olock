@CODE_COVERAGE_RULES@

echo-version:
	@echo "@OLOCK_VERSION@"

bin_PROGRAMS = olock

dist_man1_MANS = olock.1

pamddir = $(sysconfdir)/pam.d
pamd_files = pam/olock
pamd_DATA = $(pamd_files)

AM_CPPFLAGS = \
	@AX_EXTEND_SRCDIR_CPPFLAGS@

olock_CFLAGS = \
	$(AM_CFLAGS) \
	$(XCB_CFLAGS) \
	$(XCB_IMAGE_CFLAGS) \
	$(XCB_UTIL_CFLAGS) \
	$(XKBCOMMON_CFLAGS) \
	$(CAIRO_CFLAGS) \
	$(FONTCONFIG_CFLAGS) \
	$(JPEG_CFLAGS) \
	$(CODE_COVERAGE_CFLAGS)

olock_CPPFLAGS = \
	$(AM_CPPFLAGS) \
	$(CODE_COVERAGE_CPPFLAGS)

olock_LDADD = \
	$(XCB_LIBS) \
	$(XCB_IMAGE_LIBS) \
	$(XCB_UTIL_LIBS) \
	$(XKBCOMMON_LIBS) \
	$(CAIRO_LIBS) \
	$(JPEG_LIBS) \
	$(FONTCONFIG_LIBS) \
	$(CODE_COVERAGE_LDFLAGS)

olock_SOURCES = \
	cursors.h \
	olock.c \
	olock.h \
	randr.c \
	randr.h \
	unlock_indicator.c \
	unlock_indicator.h \
	xcb.c \
	xcb.h \
	tinyexpr.c \
	tinyexpr.h \
	blur_simd.c \
	blur.c \
	blur.h \
	jpg.c \
	jpg.h \
	fonts.h


EXTRA_DIST = \
	$(pamd_files) \
	CHANGELOG \
	LICENSE \
	README.md
