## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ecbd5e9a46383aa74bed2b80ff8af26b13002e329e128d2eff829bc686c4afe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:c6e9998c96c4eae369596dc68c16926a3b102ac73ae4d27a818bebe929da9b37
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242958213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6965c219ac6a486b9bb1e759838db0b02fdaf2f64a2fba1aafea628d1de4922f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:15:43 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:15:44 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 02:15:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 02:15:46 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:15:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:15:49 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:15:53 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Fri, 31 Jan 2025 02:15:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f1cfb1a515301c5d46cf52e997da0cd6b39b4931276bb0a8f949bf64df59b`  
		Last Modified: Tue, 18 Feb 2025 10:25:16 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361c604da3cd668ec671428558ab50f8041ccbabb3e2d701206ebe8fc4d2f82`  
		Last Modified: Tue, 18 Feb 2025 10:25:17 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8678fb2273aaea0e5d8b4a4d441519357db4ba2c0ed3d698c5f6d700b8da8`  
		Last Modified: Tue, 18 Feb 2025 10:25:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d357b54a9ccdeda6a0652b96b0af50cf040baf64894e289a3854b14b6c92f88`  
		Last Modified: Tue, 18 Feb 2025 10:25:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4868e4d22dcd0f4885ea20c49394df92ba867e8417b085cdec5b960b265e540e`  
		Last Modified: Tue, 18 Feb 2025 10:25:19 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf18df91fa4de25aa893064c380b047c7860e68b005375d1819e6b1636639bb`  
		Last Modified: Tue, 18 Feb 2025 10:25:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee17614b6e84590d7aab5cc47da2e026a4503522e09d4d43ca950f61fe84bf30`  
		Last Modified: Tue, 18 Feb 2025 10:25:22 GMT  
		Size: 43.7 MB (43728332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bb93e23d0fcf21539e3b4be7aafd5164ccdb181fa8afaac39d956ea7be442a`  
		Last Modified: Tue, 18 Feb 2025 10:25:23 GMT  
		Size: 93.9 KB (93906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:749dd8f1be58c4012b42a1f093aa574117b58690b2296adbdb4ddd0b716949b0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164587273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1994ab931b45cb7733933c4560ce03fec7432abc7b942ada74f0330c839bf087`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:17:45 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:17:46 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 01:17:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 13 Feb 2025 01:17:47 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:17:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:17:49 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:17:53 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Thu, 13 Feb 2025 01:17:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593697fda94bcfebf73dac6ddee81942ff5f16b4e2a9d8afdf7fbf7afe3ecab0`  
		Last Modified: Thu, 13 Feb 2025 04:14:13 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5604dcc3a4e115d2a87d8f55189faab2a92deaab4003d209cc9cba96ca141e4`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2015764c29246e5d0bc4398bf2935779bb12c1a43b22fd8c409221c234a8baa`  
		Last Modified: Thu, 13 Feb 2025 04:14:13 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6c9acfd925c01a9fceaa0ae1b5687ae6f3fc465b63805186b954d596a3480`  
		Last Modified: Thu, 13 Feb 2025 04:14:13 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe9fc43e6a3ac82249795766fe11b037227c6e84793fa088e4089c9a3bec535`  
		Last Modified: Thu, 13 Feb 2025 04:14:13 GMT  
		Size: 78.3 KB (78254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a04119052400cdc769a2125e17c51874ff27678fab83939240c05e1a41fb098`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b7826d4003deeca48ee396ecfbabac6a376fd567a0b17ed38f74a8ee41cc2c`  
		Last Modified: Thu, 13 Feb 2025 04:14:16 GMT  
		Size: 43.7 MB (43727517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee8223d920ecb83b699898b0577bfb74f2d77457e62698645cfac82e6775888`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 109.7 KB (109694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:0477f0ecf3645e40cfbaca1c6203cf4a71e3b9b6501ada8e160c4ae54d99458a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153722040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8beafa0c5efff1bd156d1ec1af7bcab0538b949c1cb7f6bd1d45db8b4305d42`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:11:43 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:11:45 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 13 Feb 2025 01:11:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 13 Feb 2025 01:11:46 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:11:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:11:49 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:11:53 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Thu, 13 Feb 2025 01:11:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958b11c984c6aa68666387d6ab414ae3098297c10b24b5c45ec2fb71aafd8953`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2caaef4e573d8d040930f054e8bef1378e275a42ae05dcaaa5d9049440a90e`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda177d081dfb0de973cb8ded6c2100ca51ff9f733161211b45c2c87a0a4268e`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4fe738576f6791c860b4d05677b9ee22923c0a2acd15b2165d48ad2e3c189`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af19e563f907f504e35d3d7a7dca3917bed170c39206f29b0cbaaf3ace662df6`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 71.2 KB (71207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9179edb36d39caad80d04672c1297143b81b34f6ef6e1875a65371a7b3d434ed`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46c2baa70659697980d1eea01b33a536973bb8cdc0bc998768780fab3bb760`  
		Last Modified: Thu, 13 Feb 2025 04:14:22 GMT  
		Size: 43.7 MB (43726855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf54ead13b3f1a8d9e4cba79f96f9ee1f6b6517b7205457b6fca912d87c528`  
		Last Modified: Thu, 13 Feb 2025 04:14:14 GMT  
		Size: 3.0 MB (3003320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
