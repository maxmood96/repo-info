## `eclipse-temurin:25-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:aa4aedf3f1ef6482a15d8ad37bbb9177b5c86196ef940835fc1cc747cd1dddce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:25-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:e049fc242a6e422cceec32e30307e8125fcbf167ab11f277c377ec0f7248542a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337847576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e30c6439725975f385301e49959b8a527ee7db833491e79a81fac0d0ec2de98`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:10:47 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:13:58 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 14 Apr 2026 22:13:58 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Apr 2026 22:13:59 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:14:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:14:00 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:14:11 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Tue, 14 Apr 2026 22:14:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Apr 2026 22:14:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9283504e7a4dc0b9369ebeee673efd11bfea17126a3b7e1ef073687a6f63449`  
		Last Modified: Tue, 14 Apr 2026 22:11:40 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be03cadda0d2713a6fea128f4efcefde1969ed3cdfe66f3b7ccd0a66c0ff419`  
		Last Modified: Tue, 14 Apr 2026 22:14:21 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed69d2ca9eff4f117db808193249dd8c49e905b1c57206896d683623634d23d`  
		Last Modified: Tue, 14 Apr 2026 22:14:21 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80e9e570279b4c5178d0d7ffc02fe4c90c0beef9cb706d2be3a341b37a865c2`  
		Last Modified: Tue, 14 Apr 2026 22:14:21 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba30b6deed5e308f9eea03091bbf6c5778eb22570ecdabec93acbb7be9d09015`  
		Last Modified: Tue, 14 Apr 2026 22:14:19 GMT  
		Size: 72.0 KB (72026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5977097c4f1b7b64921b4f4e012e0362736a0e650296cb46cb437b97c2b1333b`  
		Last Modified: Tue, 14 Apr 2026 22:14:19 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee181f3cbfe5ed7279031b2753a87fdec807ada9b591653fb4567dac62fd55a7`  
		Last Modified: Tue, 14 Apr 2026 22:14:31 GMT  
		Size: 137.9 MB (137932032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593124170fe53e28c1a060b6f900c19802067e16adef5c38c6d8cb99da44cd54`  
		Last Modified: Tue, 14 Apr 2026 22:14:19 GMT  
		Size: 119.9 KB (119948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807fd53f0a03b5175f3693454b5a40464e60e1398282b64982863ca38fcf66f1`  
		Last Modified: Tue, 14 Apr 2026 22:14:19 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:fa1f86e8c48be40a5614ce7d488d9c74437a4dd8ba9ff7dcfa93fd5907ef427b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265087646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b6bd39586e3c0bc9b2c7eaa69a97552a175538c4b09972b68d1fcf3c88378c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:10:58 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:12:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 14 Apr 2026 22:12:02 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Apr 2026 22:12:02 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:12:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:12:04 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:12:12 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Tue, 14 Apr 2026 22:12:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Apr 2026 22:12:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca91647e48c8f734915ba8e1d5f9edea1563ca4c872069115650f0dfe102a26`  
		Last Modified: Tue, 14 Apr 2026 22:11:16 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec56a4af7de9d5e8d7bdac83900726a608fc74e0b205f2d0a94c559b1ca952`  
		Last Modified: Tue, 14 Apr 2026 22:12:23 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addc7341d22904bfe00235a1b52ec82a4f6e096deec858c9ccdb56eae6012a6a`  
		Last Modified: Tue, 14 Apr 2026 22:12:23 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789cde8e4a87268d023f1c97b5a3be06f20b63adb3b6c02b256cd53d3fe7590e`  
		Last Modified: Tue, 14 Apr 2026 22:12:23 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a956f1858f893d64b346315b656d28b7a5cf977da0cd559f98148e050a7379d`  
		Last Modified: Tue, 14 Apr 2026 22:12:21 GMT  
		Size: 86.3 KB (86256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98221cf466faabe6d4b94aba48a465548b0a81157ab444901d3e9ebf79af447`  
		Last Modified: Tue, 14 Apr 2026 22:12:21 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8396ae0ab23fa7e3aaa149c87d00cf854e3d55d3515e59f87f642d0dd00161`  
		Last Modified: Tue, 14 Apr 2026 22:12:39 GMT  
		Size: 137.9 MB (137932170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa834e696fcf3f81ebe9f048ec702f8d2fd194df6b8dec60accfe3c34dba2f06`  
		Last Modified: Tue, 14 Apr 2026 22:12:21 GMT  
		Size: 106.8 KB (106819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4767c9208f869296df65b90364dd4bf2ae0efa9948069755b7be77756fe9c142`  
		Last Modified: Tue, 14 Apr 2026 22:12:21 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
