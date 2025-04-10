## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2fe91ecfdcf6f2e941346515d48945c3bb2c5bbcf5db862725ea9130c5f883bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:1c01cbf1cce2ecc546aa0f54f029c310d83355285c09541213953a78a2c591ed
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234016561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03e099f62042f3145caf06119d0c02fbade2ed775792a2d9375aca3fac403f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 02:17:15 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:17:15 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 09 Apr 2025 02:17:16 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Apr 2025 02:17:17 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:17:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:17:21 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:17:25 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 09 Apr 2025 02:17:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc5ae0430016cf2cb002f46af4aaa8169fb2c5badcf5eeb49be1c7fae0de854`  
		Last Modified: Wed, 09 Apr 2025 02:17:33 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7854e35d86cd9de464b61700c307cddf64c55a53e3c5bc242e927b536937d4e2`  
		Last Modified: Wed, 09 Apr 2025 02:17:33 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bb9708f7bbd2838fa0f8bf9f95b5e184b57917c2452a6665315e3df2d5595f`  
		Last Modified: Wed, 09 Apr 2025 02:17:33 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5542e2a37df7c27297e79197c7a6b064a860a6d50f2df5d1cae8f4fc019c06`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77786ed6f297f768d3707067cebd22955042c136166fc7fabd667cf3c5bde03`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 76.3 KB (76328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109316969678b62c7f38b26acdc50badba9a77c28a66b90fdd106d02c426a052`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244385b3ad35485feb3eb3c83ffdc07732e1550c86290d6265c2277033ed6680`  
		Last Modified: Wed, 09 Apr 2025 02:17:37 GMT  
		Size: 43.7 MB (43729009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c29d8f0e6c90393a9a58b6595453837d8be2005b8a182c8a3d23c1c279ac28`  
		Last Modified: Wed, 09 Apr 2025 02:17:32 GMT  
		Size: 92.7 KB (92654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:8386860cadff69e02ed1271bea2cd753fa5e7b08c6155d678ab43d59f93fd643
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164640093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf714a5bbe3944476f0607ba803688d848912e4f42f3c5f36ee65deffda847f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 02:21:46 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:21:46 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 09 Apr 2025 02:21:47 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Apr 2025 02:21:48 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:21:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:21:51 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:21:55 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 09 Apr 2025 02:21:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e189a98b89057ff91cb516fef5335cf6994780cae9b1f65aa3446069ceb3eb8a`  
		Last Modified: Wed, 09 Apr 2025 02:22:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37e1866386b3622d892d73fa1c54ce2c6d2e9b812b46beab082f5cc61a55c14`  
		Last Modified: Wed, 09 Apr 2025 02:22:02 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64d77f125d12a5208970e72763f808e21dd3c12416159e9c1023e738697fdf`  
		Last Modified: Wed, 09 Apr 2025 02:22:02 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee466b2b2272a6f6215148071dbd551db4fc514e90bfc8c2ec1134a55e1c3b8`  
		Last Modified: Wed, 09 Apr 2025 02:22:01 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfc106cdd5814579e11a5d68463aa71d40ba5ea92b32d9a46052532876d485d`  
		Last Modified: Wed, 09 Apr 2025 02:22:01 GMT  
		Size: 77.2 KB (77245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0cdfe50da7db74c526adcf532b47b6931b6f6d444e65f04752a0cff7a0cc1d`  
		Last Modified: Wed, 09 Apr 2025 02:22:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0086d733d0f564183ba0e0ae31f879ed797216904c43b58d035221f4ad4848a`  
		Last Modified: Wed, 09 Apr 2025 02:22:06 GMT  
		Size: 43.7 MB (43726807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1de75e8d9118aaf4b817f93babbf323f3a658299baea062264e934aadc655ce`  
		Last Modified: Wed, 09 Apr 2025 02:22:01 GMT  
		Size: 94.6 KB (94579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:6dc7e9969cc5ca60eaace5022d87fc1707405fc93b85f7bea3a80dcd3c2b7175
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153720074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05be022baedbcc1f78dd208d83132167cb292b16cafaa86ce5d7a0fcc7ddba24`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:17:00 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:02 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 09 Apr 2025 01:17:03 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Apr 2025 01:17:03 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:07 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:11 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Wed, 09 Apr 2025 01:17:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dc514fefbf2d0cfc7984b3a58ae947f59a63a9314118a77c01af4e5dab65ac`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f42753104e204304bc7ff86ec5db339a81af1fe5fa4fb2dad7ca78d2ff03fd`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1713f59e5f0f196b7df5ee248f889b416f3f36372da2a539241286a4462293`  
		Last Modified: Wed, 09 Apr 2025 01:17:19 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a5f811168e67fdc05c94ffc17dad4ff51fd79dd3c3365a1a8efe0f7361b4f7`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6647f1764f769fb166bfeb8a6ceb21acac502bdbc2a26bbd91c1582da4f3b94a`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 70.7 KB (70700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e2e19566a976e5bd865319568e52bbca156ee516b3558881bd41c85c88c7f7`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5138965f2f6a5875324d759dfd93f984deb8a8e7e79f1508840302a7aef97c`  
		Last Modified: Wed, 09 Apr 2025 01:17:23 GMT  
		Size: 43.7 MB (43728614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bfec6f6b85768e75f0c22e93566d4dfdcf8b03874106e089c71d295db43997`  
		Last Modified: Wed, 09 Apr 2025 01:17:18 GMT  
		Size: 3.0 MB (2993105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
