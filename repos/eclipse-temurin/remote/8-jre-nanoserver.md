## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6b0826e23d6c7bd8b2c0909847b0b0e413edd5c23c703f9fde845841742d6108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:134e79556068470fb178f07d94009c8e890d40617a55d76055da3c5ed65b0d84
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160631153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd7943b88f1d3c5803006fe0fcabac76337d21be42336a6df2d87a24fbca695`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:11:36 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Thu, 10 Aug 2023 00:11:37 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 10 Aug 2023 00:11:37 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:11:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:11:51 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:12:25 GMT
COPY dir:f24575d0fd9e2979f5a8010c202ec6d963a3eb3cd788517e3ab1d758c8e6ad81 in C:\openjdk-8 
# Thu, 10 Aug 2023 00:12:36 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ea9613880997b3ab2284a37c0c14a403553457b0c331b41c6bd6d1cc7838a222`  
		Last Modified: Tue, 08 Aug 2023 18:47:21 GMT  
		Size: 120.5 MB (120500677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3572ac06c9147f0946a40530f2197bb0101b82dd45b1defe04a8904a1c81a18`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e89764c10b44510903b32c7edd36c21e79b25d8b06469e52cc62eda35374a86`  
		Last Modified: Thu, 10 Aug 2023 00:30:45 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceecc9a97f51e72739327b08e944e807b59412c3371154cd1517a1076f0ff13`  
		Last Modified: Thu, 10 Aug 2023 00:30:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6af468f1994e77d29a4fd32c9af35ed9cbc560bc299dae24b1be570c72bdc3`  
		Last Modified: Thu, 10 Aug 2023 00:30:43 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccc203e63ce253cf5087832aef09390ce453c9142f45b40e6c69d58bd390157`  
		Last Modified: Thu, 10 Aug 2023 00:30:43 GMT  
		Size: 81.8 KB (81786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f95e202c688c9a7e7c6f0f9bf6b76f2160d7aa79897363a9d892edd174453`  
		Last Modified: Thu, 10 Aug 2023 00:30:43 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bbe066c65c91bff5723f12a782298ad14fd0e4d3afa17e3c625f32737905c5`  
		Last Modified: Thu, 10 Aug 2023 00:31:25 GMT  
		Size: 40.0 MB (39981094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5251cebcfabc8ebdf0f77e50189fdc648be1cd94aeece3bfb4c3aa9d5f987279`  
		Last Modified: Thu, 10 Aug 2023 00:31:19 GMT  
		Size: 62.3 KB (62313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:3e0878b3959e728c4bc7482ff3f3b858d280d940bdefe59dc8472276f2691958
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144581115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7589ca9dcd7c1266efad4498498943f68261caf7df7e1d47bf3b2765a40c764a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Wed, 09 Aug 2023 23:39:51 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Wed, 09 Aug 2023 23:39:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Aug 2023 23:39:52 GMT
USER ContainerAdministrator
# Wed, 09 Aug 2023 23:40:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Aug 2023 23:40:03 GMT
USER ContainerUser
# Wed, 09 Aug 2023 23:44:09 GMT
COPY dir:f24575d0fd9e2979f5a8010c202ec6d963a3eb3cd788517e3ab1d758c8e6ad81 in C:\openjdk-8 
# Wed, 09 Aug 2023 23:44:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8f22ce094401eee9fd7bea0c5d1203f90b87cc66ea6c456eff425ab5e2caba`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6dfebda60f17027bfd449bc9a1cebadadaa78a560f1ef282be0d1531c32377`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18743bf806484dab7219b47b50a8125ee4c152316714f5aa08761ce9405e165`  
		Last Modified: Thu, 10 Aug 2023 00:20:58 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8b1307ee9d95fa264e5683f552f4f0760f972e70cd9a47c76949b277224d94`  
		Last Modified: Thu, 10 Aug 2023 00:20:58 GMT  
		Size: 81.4 KB (81405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d92403cd6db6a3e7c5abec82455ccf5a5555cd0e2f03c02de349f2d5237d945`  
		Last Modified: Thu, 10 Aug 2023 00:20:58 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8611d3e52c582813e3a467e1fa33b2090a4e19407503e7b96da99ed4431b112`  
		Last Modified: Thu, 10 Aug 2023 00:22:11 GMT  
		Size: 40.0 MB (39981340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fd6b1ddcdfdc9af11396b4eeb57de020a939593e3b2125ae15da694a36fea0`  
		Last Modified: Thu, 10 Aug 2023 00:22:05 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
