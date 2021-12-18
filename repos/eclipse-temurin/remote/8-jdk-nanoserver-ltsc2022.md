## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c41e76e599234940ef6d83a124a8a6ec9dd6bcf4a194fe2dd53a7b323757e97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.405; amd64

```console
$ docker pull eclipse-temurin@sha256:3a23ad659519f7a3217bc7da776c65cba34a71b8a3ead7134999c47412c1058f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217571090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5e9feecd296a9da0800b7e97a232f26fe7b0e8fcd508348482012c46e764bf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Sat, 18 Dec 2021 06:03:19 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 06:03:20 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Sat, 18 Dec 2021 06:03:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 18 Dec 2021 06:03:21 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 06:03:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 06:03:36 GMT
USER ContainerUser
# Sat, 18 Dec 2021 06:03:47 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Sat, 18 Dec 2021 06:04:01 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:29e118c52df9d671b57a04fe35f79f686c3a7038ccd41c5bf5ccfac737426ab6`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5b7a5eecd506c47a57cc6739d84cb5c60af0d1380a2d5f957caf673b1bbc77`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6bcb7659e28871ad274e216b2bdcb65931330524d33dd748c004f29448c475`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaae7decf72e8787f9547385a4d83910f4ce6a5082571946b9ceb524c792c181`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb638b1165f6be88df12dba00424796a95a755cb648664a1f955668b299b27f`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 87.7 KB (87709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c0ec7254dbde449fa61bb0d02360f1eb3022551679da0f71fe1dd1decf410`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae35fdac781e82ee82a059718dc8dbb1fbc3e5e52e950e0ce68301f15203a48`  
		Last Modified: Sat, 18 Dec 2021 06:43:17 GMT  
		Size: 100.2 MB (100190916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e68f0562a07681d687ff5a5d70b53305bded9500dbe1cd1ffd3379be6259a9`  
		Last Modified: Sat, 18 Dec 2021 06:41:28 GMT  
		Size: 60.9 KB (60882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
