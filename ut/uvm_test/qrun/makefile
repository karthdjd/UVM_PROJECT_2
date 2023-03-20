VLOG=/tool/mentor/questa-10.7c/questasim/bin/vlog
VSIM=/tool/mentor/questa-10.7c/questasim/bin/vsim
VCOVER=/tool/mentor/questa-10.7c/questasim/bin/vcover
VOPT=/tool/mentor/questa-10.7c/questasim/bin/vopt

TEST=TEST

QUESTA_SIM_PATH = /tool/mento/questa-10.7c/questasim/bin

compile:
	$(VLOG) /home/karthikeyan/Desktop/UVM_PR1/rtl/DUT.sv /home/karthikeyan/Desktop/UVM_PR1/ut/uvm_test/src/TOP.sv -l compile.log
RUN: compile
	$(VSIM) dram_top +UVM_TESTNAME=dram_test +UVM_VERBOSITY=UVM_HIGH -wlf waveform.wlf -do "log -r /*" -do "run -all" -c

RUN_WAVE: RUN
	$(VSIM) waveform.wlf
