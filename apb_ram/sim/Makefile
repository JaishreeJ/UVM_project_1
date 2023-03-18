VLOG=C:\questasim64_10.6c\win64\vlog
VSIM=C:\questasim64_10.6c\win64\vsim
VCOVER=C:\questasim64_10.6c\win64\vcover
VOPT=C:\questasim64_10.6c\win64\vopt

QUESTA_SIM_PATH =  C:\questasim64_10.6c\win64

compile:
	$(VLOG) C:\questasim64_10.6c\apbram\rtl\apb_ram.sv -l compile.log  
	$(VLOG)	C:\questasim64_10.6c\apbram\ut\uvm_tb\src\tb.sv -l compile.log
	
RUN: compile
	$(VSIM) tb "+UVM_TESTNAME=test" +UVM_VERBOSITY=UVM_HIGH -wlf waveform_apb.wlf -do "log -r/*" -do "run -all" -c 

RUN_WAVE: RUN
	$(VSIM) waveform_apb.wlf
