# APK-Page-Size-Analyzer

==========================================================================================================

# HOW TO USE:

1. Download the file (Page File Checker.exe) from repository.
2. When you open the file it'll show and security error from windows saying the Publisher of this file is unkown. Just Click (Show More) in text body of error and then Click (Run Anyway).
3. I assure you this file does not have any virus or anything it has just missing publishing details that's why Windows treat this file as Virus.
4. BROWSE you APK from you local storage.
5. LOCATE your NDK Folder. (Suggestion : Go to Unity/Android-Studio and copy the path of NDK from its settings)
6. Make sure to select the NDK folder in which the whole NDK is stored.
7. Make sure the llvm-objdump field shows the path of required file. If its empty that means the wrong folder is selected or file is missing.
8. Note : Copying the path of NDK into field does not auto locate the file. You have to press locate and then select the folder of NDK.
9. Press (Analyze). This will take a few seconds to analyze and generate the results. Once generated it will shown you which library files are 16kb memory supported and which are not.
10. Once you got the results you can lookup to internet, which library belongs to which package.
11. Once you update all the files Analyze again to see the results. All the files should be marked as ✅.
12. Whenever you analyze the apk a text file of results is generated along the selected apk.
    
==========================================================================================================

# Results

# Example 1 (Not Resolved):

libFirebaseCppAnalytics.so                  2**12      ❌

libFirebaseCppApp-12_1_0.so                 2**12      ❌

libFirebaseCppRemoteConfig.so               2**12      ❌

lib_burst_generated.so                      2**14      ✅

libapminsighta.so                           2**12      ❌

libapminsightb.so                           2**12      ❌

libapplovin-native-crash-reporter.so        2**14      ✅

libbuffer_pg.so                             2**12      ❌

libfile_lock_pg.so                          2**12      ❌

libil2cpp.so                                2**14      ✅

libmain.so                                  2**14      ✅

libmediapipe_jni.so                         2**12      ❌

libnms.so                                   2**12      ❌

libopencv_java3.so                          2**16      ✅

libpglarmor.so                              2**12      ❌

libsigner.so                                2**14      ✅

libtobEmbedPagEncrypt.so                    2**12      ❌

libtt_ugen_yoga.so                          2**12      ❌

libunity.so                                 2**14      ✅

libvosk.so                                  2**12      ❌


# Example 2 (Resolved):

libFirebaseCppAnalytics.so                  2**14      ✅

libFirebaseCppApp-13_3_0.so                 2**14      ✅

libFirebaseCppRemoteConfig.so               2**14      ✅

lib_burst_generated.so                      2**14      ✅

libapminsighta.so                           2**14      ✅

libapminsightb.so                           2**14      ✅

libapplovin-native-crash-reporter.so        2**14      ✅

libbuffer_pgl.so                            2**14      ✅

libfile_lock_pgl.so                         2**14      ✅

libil2cpp.so                                2**14      ✅

libmain.so                                  2**14      ✅

libmediapipe_jni.so                         2**14      ✅

libnms.so                                   2**14      ✅

libopencv_java4.so                          2**14      ✅

libpglarmor.so                              2**14      ✅

libsigner.so                                2**14      ✅

libtobEmbedPagEncrypt.so                    2**14      ✅

libtt_ugen_layout.so                        2**14      ✅

libunity.so                                 2**14      ✅

==========================================================================================================

# Dictionary

-> ✅ : Good to Go

-> ❌ : Needs to be updated

-> 2**14 : 16KB supported

-> 2**12 : 4KB supported


libAndroidCpuUsage.so                      -> Adaptive Performance package

libFirebaseCppAnalytics.so                 -> Firebase Analytics

libFirebaseCppApp-13_3_0.so                -> Firebase

libFirebaseCppRemoteConfig.so              -> Firebase Remote Config

lib_burst_generated.so                     -> Burst Compiler

libapminsighta.so                          -> Pangle Network Adapter

libapminsightb.so                          -> Pangle Network Adapter

libapplovin-native-crash-reporter.so       -> Max Apploving

libbuffer_pgl.so                           -> Pangle Network Adapter

libfile_lock_pgl.so                        -> Pangle Network Adapter

libil2cpp.so                               -> Unity Native Library

libmain.so                                 -> Unity Native Library

libmediapipe_jni.so                        -> MediaPipe (Custom Library)

libnms.so                                  -> Pangle Network Adapter

libopencv_java4.so                         -> OpenCV (Custom Library)

libpglarmor.so                             -> Pangle Network Adapter

libsigner.so                               -> Pangle Network Adapter

libtobEmbedPagEncrypt.so                   -> Pangle Network Adapter

libtt_ugen_yoga.so                         -> Pangle Network Adapter

libunity.so                                -> Unity Native Library

libvosk.so                                 -> Vosk (Custom Library)
