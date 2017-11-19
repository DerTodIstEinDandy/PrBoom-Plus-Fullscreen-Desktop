#
# automake Makefile.am for the PrBoom source directory
#
#
# Process this file with automake to produce Makefile.in
#
#

SUBDIRS = SDL POSIX MAC PCSOUND TEXTSCREEN MUSIC   

gamesdir=$(prefix)/games

if BUILD_SERVER
games_PROGRAMS = prboom-plus prboom-plus-game-server
else
games_PROGRAMS = prboom-plus
endif

CFLAGS = @CFLAGS@ @SDL_CFLAGS@


COMMON_SRC = \
 am_map.c \
 am_map.h \
 d_deh.c \
 d_deh.h \
 d_englsh.h \
 d_event.h \
 d_items.c \
 d_items.h \
 d_main.c \
 d_main.h \
 d_net.h \
 d_player.h \
 d_think.h \
 d_ticcmd.h \
 doomdata.h \
 doomdef.c \
 doomdef.h \
 doomstat.c \
 doomstat.h \
 doomtype.h \
 dstrings.c \
 dstrings.h \
 e6y.c \
 e6y.h \
 f_finale.c \
 f_finale.h \
 f_wipe.c \
 f_wipe.h \
 g_game.c \
 g_game.h \
 g_overflow.c \
 g_overflow.h \
 hu_lib.c \
 hu_lib.h \
 hu_stuff.c \
 hu_stuff.h \
 hu_tracers.c \
 hu_tracers.h \
 i_capture.c \
 i_capture.h \
 i_joy.h \
 i_main.h \
 i_network.h \
 i_pcsound.c \
 i_pcsound.h \
 i_sound.h \
 i_system.h \
 i_video.h \
 info.c \
 info.h \
 lprintf.c \
 lprintf.h \
 m_argv.c \
 m_argv.h \
 m_bbox.c \
 m_bbox.h \
 m_cheat.c \
 m_cheat.h \
 m_fixed.h \
 m_menu.c \
 m_menu.h \
 m_misc.c \
 m_misc.h \
 m_random.c \
 m_random.h \
 m_swap.h \
 md5.c \
 md5.h \
 p_ceilng.c \
 p_checksum.c \
 p_checksum.h \
 p_doors.c \
 p_enemy.c \
 p_enemy.h \
 p_floor.c \
 p_genlin.c \
 p_inter.c \
 p_inter.h \
 p_lights.c \
 p_map.c \
 p_map.h \
 p_maputl.c \
 p_maputl.h \
 p_mobj.c \
 p_mobj.h \
 p_plats.c \
 p_pspr.c \
 p_pspr.h \
 p_saveg.c \
 p_saveg.h \
 p_setup.c \
 p_setup.h \
 p_sight.c \
 p_spec.c \
 p_spec.h \
 p_switch.c \
 p_telept.c \
 p_tick.c \
 p_tick.h \
 p_user.c \
 p_user.h \
 protocol.h \
 r_bsp.c \
 r_bsp.h \
 r_data.c \
 r_data.h \
 r_defs.h \
 r_demo.c \
 r_demo.h \
 r_draw.c \
 r_draw.h \
 r_filter.c \
 r_filter.h \
 r_fps.c \
 r_fps.h \
 r_main.c \
 r_main.h \
 r_patch.c \
 r_patch.h \
 r_plane.c \
 r_plane.h \
 r_segs.c \
 r_segs.h \
 r_sky.c \
 r_sky.h \
 r_state.h \
 r_things.c \
 r_things.h \
 s_advsound.c \
 s_advsound.h \
 s_sound.c \
 s_sound.h \
 sc_man.c \
 sc_man.h \
 sounds.c \
 sounds.h \
 st_lib.c \
 st_lib.h \
 st_stuff.c \
 st_stuff.h \
 tables.c \
 tables.h \
 v_video.c \
 v_video.h \
 version.c \
 version.h \
 w_wad.c \
 w_wad.h \
 wi_stuff.c \
 wi_stuff.h \
 z_bmalloc.c \
 z_bmalloc.h \
 z_zone.c \
 z_zone.h

NET_CLIENT_SRC = d_client.c

if BUILD_GL
USE_GL_SRC = \
 gl_clipper.c \
 gl_detail.c \
 gl_drawinfo.c \
 gl_fbo.c \
 gl_gamma.c \
 gl_hires.c \
 gl_hqresize.c \
 gl_intern.h \
 gl_light.c \
 gl_main.c \
 gl_map.c \
 gl_missingtexture.c \
 gl_opengl.c \
 gl_opengl.h \
 gl_preprocess.c \
 gl_shader.c \
 gl_shadow.c \
 gl_sky.c \
 gl_struct.h \
 gl_texture.c \
 gl_vertex.c \
 gl_wipe.c
else
USE_GL_SRC =
endif

if WAD_MMAP
WAD_SRC = w_mmap.c
else
WAD_SRC = w_memcache.c
endif

MUS2MID_SRC = \
 memio.c \
 memio.h \
 mus2mid.c \
 mus2mid.h

prboom_plus_SOURCES = \
 $(COMMON_SRC) \
 $(NET_CLIENT_SRC) \
 $(USE_GL_SRC) \
 $(WAD_SRC) \
 $(MUS2MID_SRC)

prboom_plus_LDADD = \
 SDL/libsdldoom.a \
 PCSOUND/libpcsound.a \
 TEXTSCREEN/libtextscreen.a \
 MUSIC/libdoommusic.a \
 @MIXER_LIBS@ \
 @NET_LIBS@ \
 @SDL_LIBS@ \
 @GL_LIBS@ \
 @MATH_LIB@

prboom_plus_game_server_SOURCES = \
 d_server.c \
 protocol.h

prboom_plus_game_server_LDADD = \
 POSIX/libposixdoom.a \
 SDL/i_network.o \
 @NET_LIBS@ \
 @SDL_LIBS@

EXTRA_DIST = \
 r_drawcolpipeline.inl \
 r_drawcolumn.inl \
 r_drawflush.inl \
 r_drawspan.inl \
 icon.c
