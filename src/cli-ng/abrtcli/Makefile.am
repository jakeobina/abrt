PYFILES= \
	__init__.py \
	cli.py \
	config.py \
	filtering.py \
	l18n.py \
	match.py \
	utils.py

abrtcli_PYTHON = $(PYFILES)
abrtclidir = $(py3execdir)/abrtcli

config.py: config.py.in
	sed -e s,\@LOCALE_DIR\@,$(localedir),g \
	-e s,\@VERSION\@,$(PACKAGE_VERSION),g \
	$< >$@

EXTRA_DIST = config.py.in

all-local: config.py
