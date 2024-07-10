## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c80988b22ec8610ff180af35ffdb652b1c0ba959fb19ea1fdf9f46c877f5ca19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:454aeb876beea7a66ec9e5e701276bdb4f76a549f760db7ed3b1d15537640726
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164024129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5b95a31eb9c408a6fd744cc50dfa3f4c5578e3a72f8bb48178c4c117f41197`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:18:26 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 17:18:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Jul 2024 17:18:27 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:18:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:18:36 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:19:16 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Wed, 10 Jul 2024 17:19:25 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49db8259042be4df6cd427a4f8d442f29492106caea180a69ab6e573bfede29`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcae028b75a0ab4790b64c099f969203447b12bb79e308919e09b019a7d169b`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de042bb20d46965d4aa43c5cea3a8d1aebfee8eb9a0bd7a00cc801f72bd12ce`  
		Last Modified: Wed, 10 Jul 2024 17:39:35 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614effc4c5e5f8461be75269c0ff2273b6958fe3364c1b0885c0c581ccbaf708`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 81.2 KB (81195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dadaa039ffed31184e70603ab50918341815d96581fbeec22d8c5bbecbf0b89`  
		Last Modified: Wed, 10 Jul 2024 17:39:33 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51f694678cd93050385edc31c52d5463bf23678c545b7996aa19fe66ba525c9`  
		Last Modified: Wed, 10 Jul 2024 17:40:03 GMT  
		Size: 43.4 MB (43384369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a60a21497cdb5befc9cda11d496a1dba5b84e3b2002d012bd90f961c146de7`  
		Last Modified: Wed, 10 Jul 2024 17:39:57 GMT  
		Size: 62.5 KB (62491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:37b0dc79c0433d1bdcfdb90eb4d7ba37a99d2c9d46e3a514f86f460321f64d64
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198632638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ecedfcefaf28d5636d289238f139f7371153462ef8ae7d33a1e167ebaa81df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 16:46:39 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 10 Jul 2024 16:46:39 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Jul 2024 16:46:40 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 16:46:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 16:46:48 GMT
USER ContainerUser
# Wed, 10 Jul 2024 16:50:51 GMT
COPY dir:b092036da9619d86aad01e40fe92454a038bf12563d3a63208d5f3f51004688a in C:\openjdk-11 
# Wed, 10 Jul 2024 16:51:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c254e529e474f59a4578fb2028d068f7b14b05ac32bb741b48bddd3c305f91`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03428648c72b9188308e33592b4f418c573a42c0dd50dfceccedf848fb9cb597`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49fe0deee1dde51a87e53a2556f4de0d0653e1e3fb5dabfbe93f5a9e68729dec`  
		Last Modified: Wed, 10 Jul 2024 17:30:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc49ab9383cb6875d5fd12ff6e4009a9b34a7ad2037963f0aed12ac4a2127dc`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 68.9 KB (68922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccd083b75e153d6a232a41157a52842d30b52f61057ee5fe680248fc19eef26`  
		Last Modified: Wed, 10 Jul 2024 17:30:22 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b11ca36be9ee87f7a5123b8be02ed80488c80265f4484022e0a896f2598343`  
		Last Modified: Wed, 10 Jul 2024 17:31:26 GMT  
		Size: 43.4 MB (43384426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59fc55328e7c4be2420940aa3ec30f340c6e69fab2999a3ed33ae93a5408991`  
		Last Modified: Wed, 10 Jul 2024 17:31:20 GMT  
		Size: 92.1 KB (92118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
