AM_CXXFLAGS = -Wall -Werror -g -O2 -I$(top_srcdir)/src

# Yaggo variable
noinst_HEADERS = $(YAGGO_SOURCES)
BUILT_SOURCES = $(YAGGO_SOURCES)
DISTCLEANFILES = $(BUILT_SOURCES)

# Yaggo automatic rules with silencing
V_YAGGO = $(V_YAGGO_$(V))
V_YAGGO_ = $(V_YAGGO_$(AM_DEFAULT_VERBOSITY))
V_YAGGO_0 = @echo "  YAGGO " $@;
.yaggo.hpp:
	$(V_YAGGO)$(YAGGO) -o $@ $<
YAGGO_SOURCES = # Append all file to be built by yaggo

##############################
# Programs
##############################
bin_PROGRAMS = test
test_SOURCES = src/test.cc
noinst_HEADERS += src/test.hpp
YAGGO_SOURCES += src/test_cmdline.hpp

dist_bin_SCRIPTS = src/find_path.py src/create_exon_fasta.py src/add_read_counts.py src/delta_splitting.py src/generate_gtf.py src/majority_vote.py src/niffler.sh
