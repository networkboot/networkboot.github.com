#
# make file
#  documents  .svg generation
#
#
all: bios_post_and_bbs.svg

bios_post_and_bbs.svg: bios_post_and_bbs.dia
	dia --export=$@ --export-to-format=svg $<
	sed --in-place '3s/svg width.*viewBox/svg viewBox/' $<

# l l
