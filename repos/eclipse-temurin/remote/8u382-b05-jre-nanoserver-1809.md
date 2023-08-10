## `eclipse-temurin:8u382-b05-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:2053a939d61561907c36693717a3c516e7a025e3762b88ac2afd084de4bc3faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:8u382-b05-jre-nanoserver-1809` - windows version 10.0.17763.4737; amd64

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
