SUBDIRS = playback
DIST_SUBDIRS = playback

benchmark_appsink_SOURCES = benchmark-appsink.c
benchmark_appsink_CFLAGS = \
	$(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_CFLAGS)
benchmark_appsink_LDADD = \
	$(top_builddir)/gst-libs/gst/app/libgstapp-$(GST_API_VERSION).la \
	$(GST_LIBS)

benchmark_appsrc_SOURCES = benchmark-appsrc.c
benchmark_appsrc_CFLAGS = \
	$(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_CFLAGS)
benchmark_appsrc_LDADD = \
	$(top_builddir)/gst-libs/gst/app/libgstapp-$(GST_API_VERSION).la \
	$(GST_LIBS)

benchmark_video_conversion_SOURCES = benchmark-video-conversion.c
benchmark_video_conversion_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_BASE_CFLAGS) $(GST_CFLAGS)
benchmark_video_conversion_LDADD = \
	$(top_builddir)/gst-libs/gst/video/libgstvideo-$(GST_API_VERSION).la \
	$(GST_LIBS) $(LIBM)

if USE_X
X_TESTS = stress-videooverlay

stress_videooverlay_SOURCES = stress-videooverlay.c
stress_videooverlay_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_BASE_CFLAGS) $(GST_CFLAGS) $(X_CFLAGS)
stress_videooverlay_LDADD = \
	$(top_builddir)/gst-libs/gst/video/libgstvideo-$(GST_API_VERSION).la \
	$(GST_LIBS) $(X_LIBS) $(LIBM)

if HAVE_GTK_X11
X_TESTS += test-colorkey test-videooverlay

test_colorkey_SOURCES = test-colorkey.c
test_colorkey_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_BASE_CFLAGS) $(GST_CFLAGS) $(X_CFLAGS) $(GTK_CFLAGS)
test_colorkey_LDADD = \
	$(top_builddir)/gst-libs/gst/video/libgstvideo-$(GST_API_VERSION).la \
	$(GST_LIBS) $(X_LIBS) $(LIBM) $(GTK_LIBS)

test_videooverlay_SOURCES = test-videooverlay.c
test_videooverlay_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_BASE_CFLAGS) $(GST_CFLAGS) $(X_CFLAGS) $(GTK_CFLAGS)
test_videooverlay_LDADD = \
	$(top_builddir)/gst-libs/gst/video/libgstvideo-$(GST_API_VERSION).la \
	$(GST_LIBS) $(X_LIBS) $(LIBM) $(GTK_LIBS)
endif

output_selector_test_SOURCES = output-selector-test.c
output_selector_test_CFLAGS  = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
output_selector_test_LDADD   = $(GST_LIBS)
output_selector_test_LDFLAGS = $(GST_PLUGIN_LDFLAGS)

input_selector_test_SOURCES = input-selector-test.c
input_selector_test_CFLAGS  = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
input_selector_test_LDADD   = $(GST_LIBS)
input_selector_test_LDFLAGS = $(GST_PLUGIN_LDFLAGS)

X_TESTS += output-selector-test input-selector-test

else
X_TESTS =
endif

if USE_PANGO
PANGO_TESTS = test-textoverlay

test_textoverlay_SOURCES = test-textoverlay.c
test_textoverlay_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
test_textoverlay_LDADD = $(GST_LIBS) $(LIBM)

else
PANGO_TESTS = 
endif

audio_trickplay_SOURCES = audio-trickplay.c
audio_trickplay_CFLAGS  = $(GST_CONTROLLER_CFLAGS) $(GST_CFLAGS)
audio_trickplay_LDADD = $(GST_CONTROLLER_LIBS) $(GST_LIBS) $(LIBM)

playbin_text_SOURCES = playbin-text.c
playbin_text_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
playbin_text_LDADD = $(GST_LIBS) $(LIBM)

position_formats_SOURCES = position-formats.c
position_formats_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
position_formats_LDADD = $(GST_LIBS) $(LIBM)

stress_playbin_SOURCES = stress-playbin.c
stress_playbin_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
stress_playbin_LDADD = $(GST_LIBS) $(LIBM)

test_effect_switch_SOURCES = test-effect-switch.c
test_effect_switch_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
test_effect_switch_LDADD = $(GST_LIBS)

test_overlay_blending_SOURCES = test-overlay-blending.c
test_overlay_blending_CFLAGS = \
	$(GST_PLUGINS_BASE_CFLAGS) \
	$(GST_CFLAGS) $(GIO_CFLAGS)
test_overlay_blending_LDADD = \
	$(top_builddir)/gst-libs/gst/video/libgstvideo-$(GST_API_VERSION).la \
	$(GST_LIBS) $(GIO_LIBS) $(LIBM)

test_scale_SOURCES = test-scale.c
test_scale_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
test_scale_LDADD = $(GST_LIBS) $(LIBM)

test_resample_SOURCES = test-resample.c
test_resample_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
test_resample_LDADD = $(GST_LIBS) $(LIBM)

test_box_SOURCES = test-box.c
test_box_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
test_box_LDADD = $(GST_LIBS) $(LIBM)

test_reverseplay_SOURCES = test-reverseplay.c
test_reverseplay_CFLAGS = $(GST_PLUGINS_BASE_CFLAGS) $(GST_CFLAGS)
test_reverseplay_LDADD = $(GST_LIBS) $(LIBM)

noinst_PROGRAMS = $(X_TESTS) $(PANGO_TESTS) \
	audio-trickplay playbin-text position-formats stress-playbin \
	test-scale test-box test-effect-switch test-overlay-blending test-reverseplay \
	test-resample benchmark-appsink benchmark-appsrc benchmark-video-conversion
