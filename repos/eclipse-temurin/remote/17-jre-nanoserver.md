## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:705b9e970a60080705ad408d370de69d2f234e535e60e546607415f7951d0abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:8eb20810bddccf276f1cb2b403751dc58932b9e1443fbe60613bb876befb8f9e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249792619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17db34d3ca994f3a70b9704c6840165ad298cf4699de29743781ec84e66bba0b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:33 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:33 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 27 Feb 2025 19:13:34 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 27 Feb 2025 19:13:34 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:37 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:39 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Thu, 27 Feb 2025 19:13:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa29d6dbc972fafe20fb95ebc50296281012fc39450be3406c058ee5b673d1c`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0a304dadf14c875823cdd0785cf0184e557ee0f289bb51aff80cd6fdef0219`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c33a413f0c70cdb418591bdda7baa01c20f938b31dc5ae14ee9f59c105bf43`  
		Last Modified: Thu, 27 Feb 2025 19:13:48 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1687baea7476e45477f344b0a1a27e19bf88cf7c42abb2abf50fcd32dc6dcea`  
		Last Modified: Thu, 27 Feb 2025 19:13:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d57a1bc6c68d26365fab672387d86fc9b7af83a7533ddc22b6db5b77cc4a9`  
		Last Modified: Thu, 27 Feb 2025 19:13:46 GMT  
		Size: 75.8 KB (75766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008c986ef193a663e1da29752d8d73d0dfbdff6694e04267d7b64cdb2ffc9d36`  
		Last Modified: Thu, 27 Feb 2025 19:13:46 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fec54162cca477f9b9cec91c831c1bd6474641246d7309038909af495d117f1`  
		Last Modified: Thu, 27 Feb 2025 19:13:52 GMT  
		Size: 43.7 MB (43728851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774d4c61b796f02a6b01863c08d5eeb2398ac2467c295a895237a5de73138497`  
		Last Modified: Thu, 27 Feb 2025 19:13:46 GMT  
		Size: 92.5 KB (92532 bytes)  
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
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593697fda94bcfebf73dac6ddee81942ff5f16b4e2a9d8afdf7fbf7afe3ecab0`  
		Last Modified: Thu, 13 Feb 2025 01:17:59 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5604dcc3a4e115d2a87d8f55189faab2a92deaab4003d209cc9cba96ca141e4`  
		Last Modified: Thu, 13 Feb 2025 01:17:59 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2015764c29246e5d0bc4398bf2935779bb12c1a43b22fd8c409221c234a8baa`  
		Last Modified: Thu, 13 Feb 2025 01:17:59 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f6c9acfd925c01a9fceaa0ae1b5687ae6f3fc465b63805186b954d596a3480`  
		Last Modified: Thu, 13 Feb 2025 01:17:58 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe9fc43e6a3ac82249795766fe11b037227c6e84793fa088e4089c9a3bec535`  
		Last Modified: Thu, 13 Feb 2025 01:17:58 GMT  
		Size: 78.3 KB (78254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a04119052400cdc769a2125e17c51874ff27678fab83939240c05e1a41fb098`  
		Last Modified: Thu, 13 Feb 2025 01:17:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b7826d4003deeca48ee396ecfbabac6a376fd567a0b17ed38f74a8ee41cc2c`  
		Last Modified: Thu, 13 Feb 2025 01:18:03 GMT  
		Size: 43.7 MB (43727517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee8223d920ecb83b699898b0577bfb74f2d77457e62698645cfac82e6775888`  
		Last Modified: Thu, 13 Feb 2025 01:17:58 GMT  
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
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958b11c984c6aa68666387d6ab414ae3098297c10b24b5c45ec2fb71aafd8953`  
		Last Modified: Thu, 13 Feb 2025 01:12:03 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2caaef4e573d8d040930f054e8bef1378e275a42ae05dcaaa5d9049440a90e`  
		Last Modified: Thu, 13 Feb 2025 01:12:02 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda177d081dfb0de973cb8ded6c2100ca51ff9f733161211b45c2c87a0a4268e`  
		Last Modified: Thu, 13 Feb 2025 01:12:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4fe738576f6791c860b4d05677b9ee22923c0a2acd15b2165d48ad2e3c189`  
		Last Modified: Thu, 13 Feb 2025 01:12:00 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af19e563f907f504e35d3d7a7dca3917bed170c39206f29b0cbaaf3ace662df6`  
		Last Modified: Thu, 13 Feb 2025 01:12:01 GMT  
		Size: 71.2 KB (71207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9179edb36d39caad80d04672c1297143b81b34f6ef6e1875a65371a7b3d434ed`  
		Last Modified: Thu, 13 Feb 2025 01:12:00 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e46c2baa70659697980d1eea01b33a536973bb8cdc0bc998768780fab3bb760`  
		Last Modified: Thu, 13 Feb 2025 01:12:06 GMT  
		Size: 43.7 MB (43726855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8cf54ead13b3f1a8d9e4cba79f96f9ee1f6b6517b7205457b6fca912d87c528`  
		Last Modified: Thu, 13 Feb 2025 01:12:01 GMT  
		Size: 3.0 MB (3003320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
