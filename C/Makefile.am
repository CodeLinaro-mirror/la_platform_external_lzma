ACLOCAL_AMFLAGS := -I m4

AM_CFLAGS := -Wundef \
        -Wstrict-prototypes \
        -Wno-trigraphs \
        -g -O0 \
        $(LOCBASEUTIL_CFLAGS) \
        -fno-inline \
        -fno-short-enums \
        -fpic \
        -fpermissive \
        -D_7ZIP_ST \
        -D_GNU_SOURCE \
        -DHAVE_CONFIG_H=1 \
        -DBUILD_DIVSUFSORT64 \
        -I../android_include \
        -I../include

AM_CPPFLAGS := \
        -I. \
        -I$(WORKSPACE)/OTA/streaming/external/modp_b64 \
        -I$(WORKSPACE)/OTA/streaming/external/libevent/include \
        -D_FILE_OFFSET_BITS=64 \
        -D_USE_RTTI_FOR_TYPE_TAGS \
        -D_use_allocator="none" \
        -D_OS="linux" \
        -std=c++11 \
        -DUSE_LE_MODE \
        -fpermissive

AUTOMAKE_OPTIONS = subdir-objects

AM_LDFLAGS := -shared -version-info 1:0:0


libalzma_src_la_SOURCES := 7zAlloc.c \
        7zArcIn.c \
        7zBuf2.c \
        7zBuf.c \
        7zCrc.c \
        7zCrcOpt.c \
        7zDec.c \
        7zFile.c \
        7zStream.c \
        Aes.c \
        AesOpt.c \
        Alloc.c \
        Bcj2.c \
        Bra86.c \
        Bra.c \
        BraIA64.c \
        CpuArch.c \
        Delta.c \
        LzFind.c \
        Lzma2Dec.c \
        Lzma2Enc.c \
        Lzma86Dec.c \
        Lzma86Enc.c \
        LzmaDec.c \
        LzmaEnc.c \
        LzmaLib.c \
        Ppmd7.c \
        Ppmd7Dec.c \
        Ppmd7Enc.c \
        Sha256.c \
        Sort.c \
        Xz.c \
        XzCrc64.c \
        XzCrc64Opt.c \
        XzDec.c \
        XzEnc.c \
        XzIn.c



library_includedir := $(pkgincludedir)


if USE_GLIB
libalzma_la_CFLAGS := $(AM_CFLAGS) -DUSE_GLIB @GLIB_CFLAGS@
libalzma_la_CPPFLAGS := $(AM_CPPFLAGS) -DUSE_GLIB @GLIB_CFLAGS@
libalzma_la_LDFLAGS = -shared
else
libalzma_la_CFLAGS := $(AM_CFLAGS)
libalzma_la_CPPFLAGS := $(AM_CPPFLAGS)
libalzma_la_LDFLAGS = -shared
endif
lib_LTLIBRARIES := libalzma.la
libalzma_la_SOURCES := $(libalzma_src_la_SOURCES)



