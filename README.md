### Integration notes

These projects provide native libraries via Eclipse plugin fragments. 

Currently, the inclusion of the fragment is not enough to make the dynamic code load work from within
the signal libraries on a Windows host. 

In both cases 

- org.whispersystems.signal-client-java_0.9.0.jar 
- org.signal.zkgroup-java.0.7.3.jar

the existing .so native libraries must be removed from the root of the respective jar file. 

Otherwise the existing native loading code in both libraries will not correctly load the .dll files. 