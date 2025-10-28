## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c42c88561c53625521a54ab8e00d3e4ed02bc398a5bf75e8478fc46dfc91969b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:e9d4d5578870e9775214cad34e9ddb50cc289e45f09da5ece3fab4ab0fc162a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395861849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cda4e297628c98b01b5d629e0ea273129f16cd41e503fb7ed55fd913438d034`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:21:49 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:50 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 24 Oct 2025 19:21:51 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 24 Oct 2025 19:21:51 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:21:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:21:57 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:07 GMT
COPY dir:a3fe1d88014e165c39b52565bb4587e5a787fc090e6660a0edced9167c6512ac in C:\openjdk-21 
# Fri, 24 Oct 2025 19:22:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Oct 2025 19:22:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a244dc001be4e0454ae27f00f44b291073cabf5a0264e5006c7274e56cb26c61`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e32720e37e05bb4222b4fa4ce67f5bb326fe2867ef4842097c2c7ba3835440f`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120cabee3a2f8cad2f6d40254e965ecf7959ba46b5a51648b32cbc3e34c20f7c`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecfbf7d7cad75a353f05ffd5e6e074e5e3331cded20b673c0488f56ed77e518`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5158d16ecb84e6bad865da9606c2a0a6b9003fac9fad3898444a6e2aa52afb38`  
		Last Modified: Fri, 24 Oct 2025 19:23:17 GMT  
		Size: 76.8 KB (76758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604f079dec1a3ed23cd565dfd129f7472001ad49672db54e240b7b85ef1550a`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebc09dc5b00fb76de016aa9f73e8f851dbffabda056cd69e2bb7a1f4ebdf51d`  
		Last Modified: Tue, 28 Oct 2025 10:19:45 GMT  
		Size: 201.7 MB (201671889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16c0ae93359a1846c2b298f41e8ae5f94fdf7390c6e0ec6b053c70d4d075cd3`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 77.3 KB (77319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093686225199d6a9e2f9634cea42adccb794d0f8af0d1396890c744f90adb3d0`  
		Last Modified: Fri, 24 Oct 2025 19:23:16 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:0617096e960a660d68af70afe6b65a93bfcfbe7670b4a083a87a5f0b52432947
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324547650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172ae6410b33ff471b19af29c6a19f20018681696ba70de2354a9b4e8aa0f7e5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:10 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:22:38 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 24 Oct 2025 19:22:38 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 24 Oct 2025 19:22:39 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:22:40 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:22:41 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:52 GMT
COPY dir:a3fe1d88014e165c39b52565bb4587e5a787fc090e6660a0edced9167c6512ac in C:\openjdk-21 
# Fri, 24 Oct 2025 19:22:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Oct 2025 19:22:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82b48116bbc9a2e910b540133b83e660486e482b11dfc8c0a08bbedb3698ce1`  
		Last Modified: Fri, 24 Oct 2025 19:22:16 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59a4bb784b37d8440f530f278c89bfd50e30f17c329e8c2b826f032ae7a2506`  
		Last Modified: Fri, 24 Oct 2025 19:23:25 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8996dc28147369caccd503dc9bdf372f22da9498b81e45f20b9d59c963fff22`  
		Last Modified: Fri, 24 Oct 2025 19:23:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7298067edfc6b9f5fd6739c884190645d2a1cad4fa331be0cdd5989740da92`  
		Last Modified: Fri, 24 Oct 2025 19:23:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db6295bfa0704db524938696cd30695b67dd42556459f3035fb084d4faf665a`  
		Last Modified: Fri, 24 Oct 2025 19:23:26 GMT  
		Size: 76.9 KB (76907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a411537963349fd261e317814be777c03c0a0467e6694450dd8e10b64c2318`  
		Last Modified: Fri, 24 Oct 2025 19:23:27 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8086a8e38b1b45c57d8d8ab02a6621852175543d5a39d35bcff6f76bc581d0`  
		Last Modified: Fri, 24 Oct 2025 21:16:43 GMT  
		Size: 201.7 MB (201672067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7355b887c35f8fac87bb9cbe250caee689e8b15dd73f5b0bc37e61944e1476a4`  
		Last Modified: Fri, 24 Oct 2025 19:23:27 GMT  
		Size: 108.2 KB (108250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce6dfa47ae3e0f7db28ac76262d0b40759a060b3acf267dfef673ff0625544c`  
		Last Modified: Fri, 24 Oct 2025 19:23:28 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
