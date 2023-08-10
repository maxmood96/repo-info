## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:df676215e3d254488cbdbcbf4086c3751c38b30ff8deb6a49e1f03d9177cae50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1906; amd64
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.1906; amd64

```console
$ docker pull eclipse-temurin@sha256:08ebdb8f6f450ce9f7dfb20f651c6502c384a8450e5ebd2b2017ea0a9173ba27
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306375498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76726861bd9028512917c6db355301323973e5ec237fb1983da269bec815bf3e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Aug 2023 09:40:19 GMT
RUN Apply image 10.0.20348.1906
# Thu, 10 Aug 2023 00:11:36 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 00:14:04 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Thu, 10 Aug 2023 00:14:04 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 10 Aug 2023 00:14:05 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 00:14:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Aug 2023 00:14:14 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:14:30 GMT
COPY dir:feac886cbf24087a98a3b6290107e05d81c840e59da2a1e8e2f12f6e62993a44 in C:\openjdk-17 
# Thu, 10 Aug 2023 00:14:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Aug 2023 00:14:43 GMT
CMD ["jshell"]
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
	-	`sha256:19290aa2672dc4b3bfac6f7b2ed75863cf68e0fa65c755e75b4665237df814ed`  
		Last Modified: Thu, 10 Aug 2023 00:32:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bafcbcd5a5d937e101c985549a5f0f8f69807735436ec5ce1fe7e912c81395e`  
		Last Modified: Thu, 10 Aug 2023 00:32:24 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0527bda37ca6894a3d189404577b32a2c0e922df3b8cc46f2c189348d071b6e2`  
		Last Modified: Thu, 10 Aug 2023 00:32:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f411cc9b8761f9302991748f1340aa26a947f733562dfaa5b82f2405c749bbb`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 75.3 KB (75319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3456ed745cc7943cbf780dafae226451fdc70d166f5ddc6122ac173de5f00bf9`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b1c273ad60767ba95f896cc4efbcabdded57cfddd37b5d14c5ba6903b935a7`  
		Last Modified: Thu, 10 Aug 2023 00:32:41 GMT  
		Size: 185.7 MB (185731438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0114a08cf70e0914969501b108469a3891d21f7c0a154cb36b004538085e8f25`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 61.5 KB (61548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fca595b0340671312eb529a99e3b15ddf818cb393a0fb2acd4f3abdca90b53`  
		Last Modified: Thu, 10 Aug 2023 00:32:22 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:f48ee26e6ff3cb0c28b5f9943aff551209b5e801ec09ac1dd46718bdc7545003
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293929051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f13d8a3e3e17004b3546720b7c2ef33c809854723027512f67495e75ebbbf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Wed, 09 Aug 2023 23:57:43 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 09 Aug 2023 23:57:43 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Aug 2023 23:57:44 GMT
USER ContainerAdministrator
# Wed, 09 Aug 2023 23:57:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Aug 2023 23:57:53 GMT
USER ContainerUser
# Wed, 09 Aug 2023 23:58:08 GMT
COPY dir:feac886cbf24087a98a3b6290107e05d81c840e59da2a1e8e2f12f6e62993a44 in C:\openjdk-17 
# Wed, 09 Aug 2023 23:58:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Aug 2023 23:58:19 GMT
CMD ["jshell"]
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
	-	`sha256:73fab2f1b4b5e09c41470cd0d00203e072902c23b641b71da208238f61b643cd`  
		Last Modified: Thu, 10 Aug 2023 00:26:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64cd068bf728932114b596526f700e39bf1adf08dc098a246fb471844711d0`  
		Last Modified: Thu, 10 Aug 2023 00:26:26 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840274b640fa771b658460543d3d998f6108b82aea947d767547f134a58cde9c`  
		Last Modified: Thu, 10 Aug 2023 00:26:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab521faa44bc1c2679dadb5cb63cfe3f14765ce8ad500d87db87123477d7686d`  
		Last Modified: Thu, 10 Aug 2023 00:26:24 GMT  
		Size: 68.3 KB (68332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8f6a20e3efb2de4106bad4cbc6f284797b67b0e69462f1a417e4ceb8db7e5d`  
		Last Modified: Thu, 10 Aug 2023 00:26:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a498a14a389789229ffcd52e4252252fc95988dc9757d7b17ae9531f8cf2b2`  
		Last Modified: Thu, 10 Aug 2023 00:26:43 GMT  
		Size: 185.7 MB (185731077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7d1f6b90fb5bf75898e4ad5fe5d440724b2a93a4f7510a37e55fdce3e6abd2`  
		Last Modified: Thu, 10 Aug 2023 00:26:25 GMT  
		Size: 3.7 MB (3663890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b9b8d68ed4db8ec1130a335ab9d8c13fadd97c9ff025a64330c9498310f661`  
		Last Modified: Thu, 10 Aug 2023 00:26:24 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
