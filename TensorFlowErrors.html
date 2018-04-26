cuda sdk
https://devtalk.nvidia.com/default/topic/750562/where-is-the-cuda-sdk-for-version-6-/
Prior to cuda 5 there was a cuda "toolkit" which contained things like compilers and tools and libraries, and there was an "SDK" that could be installed separately that mostly contained sample codes. Starting with CUDA 5, these are combined into a single "toolkit" installer and the tookit installer (on linux, a "runfile", on windows, an exe file) will now install 3 major components:
- GPU driver
- CUDA toolkit
- CUDA "samples"

There is no longer a separate installer for the "SDK" and it is now called the CUDA "Samples".


Building NVCC error MSB6006
https://stackoverflow.com/questions/45918446/compiling-opencv-3-3-with-cuda-9-0rc
https://devtalk.nvidia.com/default/topic/1027299/cuda-setup-and-installation/cuda-9-failed-to-support-the-latest-visual-studio-2017-version-15-5/1
Cuda compiler 路径错误，2017后不再是$(VSInstall)/bin了
In the cited version check from CUDA 9, it is clear that only MSC version up to and including 1911 are supported, while the latest MSVS update identifies as version 1912. The discussions of such issues in these forums tend to follow a predictable trajectory: Someone will suggest a "workaround" that consists in modifying or eliminating the version check. That then seems to work for trivial code, but the next thing that typically happens is that the compilation for more complex code results in "strange error messages" (a consequence of missing adjustments). Some really clever people will then propose various hacks to CUDA header files, and this then seems to eliminate the compilation bugs.

The problem with that: this is hackery, not a reliable fix. Things may seem to work but may silently compile into an incorrect binary. There is no validation of the changes because CUDA programmers don't normally have the large body of code at their disposal that NVIDIA uses for validation. It also effectively creates a one-off branch of the CUDA tool chain that makes support impossible should other problems occur later on. I highly doubt that NVIDIA accepts bug reports that state: "I am using CUDA version N, except for the following modified header files you will find attached to the bug report." As I said, that is a guess, but it is an educated one.

The scheme of CUDA requiring specific host tool chains has lead to an increasing number of version mismatch issues as in this thread (on all OS platforms) as the cadence of CUDA releases has slowed down, while the cadence of host tool chain releases has increased rapidly. 

[speculation] Why not have rapid-fire CUDA releases to deal with the issue? Plausible approach, but would likely drive up development costs. How would NVIDIA recoup that cost when the entire CUDA ecosystem is provided free of charge? Last time I purchased the equivalent ecosystem for my CPU (which also has a MSVS integration challenge), it set me back around $2K, so I have a pretty good idea how that vendor recoups (at least a part of) their cost.

Before someone points out that additional cost could be recouped through hardware sales, keep in mind that the bulk of GPU sales is still GeForce, and that in the consumer market the additional money NVIDIA can charge for providing CUDA is approximately $0. The price in that market is pretty much determined by how GeForce competes against the competition in popular games (I think any secondary pricing effects from crypto currency mining will be temporary).[/speculation] 2017.12.09
sln2：https://charlottehong.blogspot.com/2017/12/visutal-studio-2017-cuda90.html
sln3：https://blogs.msdn.microsoft.com/vcblog/2017/11/15/side-by-side-minor-version-msvc-toolsets-in-visual-studio-2017/
先安装14.11工具集，3.6G，然后在项目的命令行中添加额外的选项-Bv


Windows 10 with CUDA 9 compile errors
https://github.com/fireice-uk/xmr-stak/issues/91
solution：降低版本
I am getting the following error:
c:\program files\nvidia gpu computing toolkit\cuda\v9.1\include\crt/host_config.h(135): fatal error C1189: #error: -- unsupported Microsoft Visual Studio version! Only the versions 2012, 2013, 2015 and 2017 are supported! [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj]

I tried to change C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.1\include\crt\host_config.h
#if _MSC_VER < 1600 || _MSC_VER > 1911 => #if _MSC_VER < 1600

and got even more errors
C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(504): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(505): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(506): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(538): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(1043): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(1558): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(2371): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\type_traits(2371): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xutility(543): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xtr1common(58): error : class "std::enable_if<<error-constant>, int>" has no member "type" [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xmemory0(390): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xmemory0(1002): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xmemory0(1322): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xstring(1693): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xtr1common(58): error : class "std::enable_if<<error-constant>, void>" has no member "type" [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj] C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.12.25827\include\xutility(298): error : expression must have a constant value [C:\xmr-stak\build\xmrstak_cuda_backend.vcxproj]

=========================================================
warning：warning : calling a __host__ function from a __host__ __device__ function is not allowed

===========================================================
failed to generate #include "tensorflow/core/framework/tensor.pb.h" file

===========================================================
 warning C4819: The file contains a character that cannot be represented in the current code page (936). Save the file in Unicode format to prevent data loss
228>c:\program files\nvidia gpu computing toolkit\cuda\v9.0\include\sm_20_intrinsics.h(925): warning C4819: The file contains a character that cannot be represented in the current code page (936). Save the file in Unicode format to prevent data loss

====================================================================
228>d:\ai\1.5tensorflow_build\external\eigen_archive\unsupported\eigen\cxx11\src/Tensor/TensorContractionCuda.h(290): warning C4003: not enough actual parameters for macro 'writeRegToShmem'
228>d:\ai\1.5tensorflow_build\external\eigen_archive\eigen\src/Core/products/Parallelizer.h(20): warning : variable "m_maxThreads" was set but never used

=======================================================================
 fatal error C1060: compiler is out of heap space (compiling source file D:\ai\tensorflow\tensorflow\core\kernels\conv_ops_3d.cc) for project tf_core_kernels
如果内存有限制的话可以先完整构建一遍，针对C1060报错的文件进行单独编译，然后再进行构建，内存压力将极大的减小。
 
 ================================================================================
 EXEC : error : invalid command 'bdist_wheel'
 pip install wheel(先装好wheel包）
 
 
============================================================================
 LINK : fatal error LNK1181: cannot open input file '\pywrap_tensorflow_internal.lib'
 
 