## `openjdk:26-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:25d7fe7d1e5d2bc23e2d19f5e305ee774102028f8e7d6c1daaea74709a263e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-jdk-nanoserver` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:0cde35c79492abaf81baddc28916b2561f6eaf7b68d6426eb8d87819a2611403
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414931690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3894e86fb2a163de4220f27cc797ab05cba0f447d468a3689319521aabb1bf1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Mon, 13 Oct 2025 19:12:15 GMT
SHELL [cmd /s /c]
# Mon, 13 Oct 2025 19:12:16 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 19:12:16 GMT
USER ContainerAdministrator
# Mon, 13 Oct 2025 19:12:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 13 Oct 2025 19:12:27 GMT
USER ContainerUser
# Mon, 13 Oct 2025 19:12:27 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 19:13:04 GMT
COPY dir:83313e74e1bdca6c4da8521f7958b3cb9f989c8b9d5087396f320ade6e966d10 in C:\openjdk-26 
# Mon, 13 Oct 2025 19:13:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 13 Oct 2025 19:13:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440ab8e560a8a0b2fbf0eee870d85cb038575979204780124b9b2add13964327`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f207fe48eac331b93a8e20d0f3c904e94bbba525ff986a3b066a247641a287c3`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a0286251f886eea2a48dcc0c9552bd0b1986b298a4fc913637fef3fffebc80`  
		Last Modified: Mon, 13 Oct 2025 19:14:10 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16815cceb162d698fd470cdef226c82f82fc349603c7518d7ff759f2396d29f9`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 76.2 KB (76189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c163079d397c8d14d67ade2e1e1bbf8e26e18fb7b8d09cb6862c9b441f94fac`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265f98eb653b663d28047c56eb22b431e161a9f7c055d5ef06a30d384b05118e`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90db886916a2220901537ff8869b6127dc1f440960d1db931a48d6ab267978`  
		Last Modified: Mon, 13 Oct 2025 21:24:11 GMT  
		Size: 221.2 MB (221201313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4748fd41f46e4f5d73b6ae6e980df0a338c08774d4303e3731d04638caccc48`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 96.9 KB (96924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671b14d0b84bca3421a89cce7aec57e6b2424bdec5895875ed8fb3f4d7733a1e`  
		Last Modified: Mon, 13 Oct 2025 19:14:09 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-jdk-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:15756a0890fd7705e8cbb2d09430ff0c4289bb74e5f1dc895ecfb870a7962527
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344136582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afd64ac65a3722e92a4884c6fe2d4e278d62a5ccd365be8a370f1a6d4798cdf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Mon, 13 Oct 2025 20:18:30 GMT
SHELL [cmd /s /c]
# Mon, 13 Oct 2025 20:18:31 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 20:18:33 GMT
USER ContainerAdministrator
# Mon, 13 Oct 2025 20:18:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 13 Oct 2025 20:18:44 GMT
USER ContainerUser
# Mon, 13 Oct 2025 20:18:45 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 20:19:56 GMT
COPY dir:83313e74e1bdca6c4da8521f7958b3cb9f989c8b9d5087396f320ade6e966d10 in C:\openjdk-26 
# Mon, 13 Oct 2025 20:20:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 13 Oct 2025 20:20:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa8975bee983a0965126ce10c9b6b93cfac4f64538e80402d7d0578f13b9ff7`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee5f8cbb91b4b576db531d90e42aabb2533282769791c93733bac5888d15e70`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca2c88e757d4b5d5220ef4b2ec8883a4216dbb1bc5ca3012de66f26092694d2`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04a9bb4b5d7f5410d52fd4856303e9bed0bdeb4c8491ce48189cfb3a7313fec`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 87.0 KB (87050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057eee2a5dc68c3fe690c80aea0f636ee52dc81cfba8dff633f740eb40c4d59c`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b065ace366f9757ee03b8dd8888e3bfa9de3bcd19964c17ec56cce7c2fb0e7eb`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28817b336b727504313e39d5fdb792b2d5f7a5b0c15c79c711552104581e749a`  
		Last Modified: Mon, 13 Oct 2025 21:24:16 GMT  
		Size: 221.2 MB (221201009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eef051caa93f4d0c2a50e9246252ef9db703ee9ebd165045b6081e02adbdcd`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 122.2 KB (122218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5a1e09d6c881df444e9004345bdfde1e7a3ca59302beaf7be6f5b70c0cf0f4`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
