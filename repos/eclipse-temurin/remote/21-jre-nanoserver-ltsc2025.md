## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:6c73da654c3bb853381b6d237ba84ca4e1c4b82c286c2a30f664e97b4746f55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:786f8c8ade8cbae76011875ddc0768ab360d4636b448e1b785d9f8b762c29df5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248958797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1409c2467253925948b05d887bbe506101716fe113a78e07d70551578fc76612`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Fri, 08 May 2026 01:16:28 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 01:16:29 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 01:16:29 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 08 May 2026 01:16:30 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 01:16:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 01:16:46 GMT
USER ContainerUser
# Fri, 08 May 2026 01:18:35 GMT
COPY dir:4940aac187beb0c950977243d0b1d703fc0231f7cabe77dd307cf1e9c831ffc7 in C:\openjdk-21 
# Fri, 08 May 2026 01:18:37 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc78f0e0bd2cb417d9b8cc2243ad6d30282bfe576edb32de92827596f7fb434`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518e83bec2c2b502449068a542133968952663aabad8d09dafc07fff9da4ed01`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9866dcc5da18c5d58b28a08dff2abe8b6e364a1cd54ca5546368b896fb0d80f`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eebd44ca877d43befe65b8bcaeef8254920747b13e1a231656d0d70a6be7df`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce34f502e8ef07d7bce3a1023378be60e55efc37832697e14e3f00021696e06`  
		Last Modified: Fri, 08 May 2026 01:17:47 GMT  
		Size: 69.8 KB (69797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0528f043046898446172dfcc24cb5c88f556fe4aafe528d8c86de31978220fa3`  
		Last Modified: Fri, 08 May 2026 01:17:47 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205b106a6a7f6c9f00926f4b7f101d0f06c0b894e36ae2e810585050744a997e`  
		Last Modified: Fri, 08 May 2026 01:18:48 GMT  
		Size: 49.1 MB (49082850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4639358f9bbce8ee9293ac8e4d4542bca9f7436f97e897eae8bf5d77012aa2`  
		Last Modified: Fri, 08 May 2026 01:18:41 GMT  
		Size: 83.7 KB (83675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
