## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:bc4595f7d0f556c43d9d0c55eba37e9a5085592e7ed754024b2da5570d53420b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:c9c24a5b48a86f7bc97225ec387e7701b110b64a542c338ac1885b3f75e4b045
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169790108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d31e79a40d6bbe37041b79c374249537d6972effe525003061386742672b99d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:44 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:45 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 31 Jan 2025 02:11:46 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 31 Jan 2025 02:11:46 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:12 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:19 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Fri, 31 Jan 2025 02:12:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d22499dcc9c352a6ec26ca641122cdb711626f63047b3d04ba5a51e28afd84`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3841da0ccca959695459b9ded741437f70c4e517dbdfdb91c87c0ed0f1b6c5d2`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6efb22fa73b4fc8b9526bb2e7c63b7d72d8a0848a7808a98378eeee408abe9d`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be291acffb8f73982bc950f81a6b321ea4c2936c86480c32aacb6ebdfa9c91f9`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57586b44794f7cd457a2350990c31ad1bafa0ad54cf0ca5fe36b7eeeb8bb5679`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 85.4 KB (85447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cf750dfd785783d4d07a32a95980e75717d4771a60b9eba2d870218a267b56`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a580a1e5bb6e0c3a599ef8d4f9d9f4471601f474d87cdf4e7d0379c5bfc9b6`  
		Last Modified: Fri, 31 Jan 2025 02:12:32 GMT  
		Size: 48.9 MB (48940839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b0648a011c31967d604bcd1b2e195d42b3380e1081a7054b87901fd73dc9de`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 97.1 KB (97117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
