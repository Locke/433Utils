
# Defines the RPI variable which is needed by rc-switch/RCSwitch.h
CXXFLAGS=-DRPI
LIBS = -lwiringPi

all: send codesend RFSniffer

send: ../rc-switch/RCSwitch.o send.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ $(LIBS)
	
codesend: ../rc-switch/RCSwitch.o codesend.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ $(LIBS)
	
RFSniffer: ../rc-switch/RCSwitch.o RFSniffer.o
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $+ -o $@ $(LIBS)
	

clean:
	$(RM) ../rc-switch/*.o *.o send codesend servo RFSniffer

