# MyReactNative
POC to test RN project on xcode 14.2


Able to launch app on iOS Simulator by running the command 
```
expo run:ios
  
 ```
 but not 
 ```
 react-native run-ios
 ```


Facing this error in xcode 
```
2023-02-23 10:34:30.725912+0800 MyReactNative[30968:492764] [connection] nw_socket_handle_socket_event [C1.1.1:2] Socket SO_ERROR [61: Connection refused]
2023-02-23 10:34:30.727972+0800 MyReactNative[30968:492764] [connection] nw_socket_handle_socket_event [C1.1.2:2] Socket SO_ERROR [61: Connection refused]
2023-02-23 10:34:30.729251+0800 MyReactNative[30968:492764] Connection 1: received failure notification
2023-02-23 10:34:30.729391+0800 MyReactNative[30968:492764] Connection 1: failed to connect 1:61, reason -1
2023-02-23 10:34:30.729483+0800 MyReactNative[30968:492764] Connection 1: encountered error(1:61)
2023-02-23 10:34:30.730924+0800 MyReactNative[30968:492764] Task <F937D716-B99C-4263-8B98-53DC65A1B2A5>.<1> HTTP load failed, 0/0 bytes (error code: -1004 [1:61])
2023-02-23 10:34:30.760315+0800 MyReactNative[30968:492773] Task <F937D716-B99C-4263-8B98-53DC65A1B2A5>.<1> finished with error [-1004] Error Domain=NSURLErrorDomain Code=-1004 "Could not connect to the server." UserInfo={_kCFStreamErrorCodeKey=61, NSUnderlyingError=0x6000034b4300 {Error Domain=kCFErrorDomainCFNetwork Code=-1004 "(null)" UserInfo={_NSURLErrorNWPathKey=satisfied (Path is satisfied), interface: en0[802.11], _kCFStreamErrorCodeKey=61, _kCFStreamErrorDomainKey=1}}, _NSURLErrorFailingURLSessionTaskErrorKey=LocalDataTask <F937D716-B99C-4263-8B98-53DC65A1B2A5>.<1>, _NSURLErrorRelatedURLSessionTaskErrorKey=(
    "LocalDataTask <F937D716-B99C-4263-8B98-53DC65A1B2A5>.<1>"
), NSLocalizedDescription=Could not connect to the server., NSErrorFailingURLStringKey=http://localhost:8081/status, NSErrorFailingURLKey=http://localhost:8081/status, _kCFStreamErrorDomainKey=1}
2023-02-23 10:34:30.890297+0800 MyReactNative[30968:492449] [native] No bundle URL present.

Make sure you're running a packager server or have included a .jsbundle file in your application bundle.

```
Fix

run 
react-native start
followed by build on xcode 14.2
