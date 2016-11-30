SHELL := bash
##
## HELP
##

help :
	@echo "Disponible:"
	@echo "whire "
	@echo "test   => all test on output"
	@echo "pack => produce the tgz archive"
wire:
		vdump lana | wireshark -i - -k &
clear:
	rm *.disk
test:
	clear
	lcrash
	rm *.disk
	tcpdump -r lana.cap -n

TGZ_FILES :=  rapport.txt lana.cap lab/alice.startup lab/eve.startup lab/dnsnet.startup lab/nestor.startup lab/nestor/etc/bind/db.net.estami
PROJ_DIR := labdm
pack :
		[ -e cr.pdf ] || echo > cr.pdf
		cd .. ; tar czf $(PROJ_DIR)/$(PROJ_DIR).tgz $(TGZ_FILES:%=$(PROJ_DIR)/%)
