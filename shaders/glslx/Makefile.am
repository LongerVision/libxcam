glslx_sources = \
    shader_copy.comp.slx            \
    shader_geomap.comp.slx          \
    shader_gauss_scale_pyr.comp.slx \
    shader_lap_trans_pyr.comp.slx   \
    shader_blend_pyr.comp.slx       \
    shader_reconstruct_pyr.comp.slx \
    $(NULL)

add_quotation_marks_sh = \
    $(top_srcdir)/tools/add-quotation-marks.sh

glsl_dir = $(top_srcdir)/shaders/glsl

all-local: $(glslx_sources)

$(glslx_sources): %.slx: $(glsl_dir)/%.sl
	@$(add_quotation_marks_sh) $< $@

CLEANFILES = $(glslx_sources)
