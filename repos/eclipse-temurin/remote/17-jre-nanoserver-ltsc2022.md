## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c1764fb7243562efa3b79aa0032f797a44224182b2b0a34d8d417f25590dc84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:349e3d4f82cc8f88a56ad24ba80eedb2507b07082232ca4ead8e4dd96399fe50
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166609279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe0ed4cf88c0ba122471c37c84d7198f27477de0fab71db23d2904fa4c260d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:13:02 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:02 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 14 Oct 2025 21:13:03 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 14 Oct 2025 21:13:03 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:05 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:09 GMT
COPY dir:f06eb607ed2664f134ec9f1021e1b4f935a771c666407ab724ddde53439bca46 in C:\openjdk-17 
# Tue, 14 Oct 2025 21:13:12 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4226706e0401da499c61310f5ec16d5fa115af9bef4407ba81bcfd4d0dbd6f37`  
		Last Modified: Tue, 14 Oct 2025 21:13:29 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16810e6516a360964a701247e5f4662d65590171f3f0a656fa4762635374cc12`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55df45846a354856b134f9215e04d351af66eb5fcd0aa106ec705eda8873423e`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a39ab7c7ab14465981b45d52394153452385b7d0a3358311c3f45c33b5ff02`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131a707cc69b69ee9dd88aeefea4aee08146c9625cd66119f0135e12352d58f9`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 76.6 KB (76572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e335e17d209b023531e3f2b8bfb13a266c242a8b79e39fb226e5d70f4223cb`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e12e90035e490760f05717ca998a219e22d720b1b8d97df88d57bbd9b75855e`  
		Last Modified: Tue, 14 Oct 2025 21:13:33 GMT  
		Size: 43.7 MB (43748278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a862f0e18c2d055337364328f23d0da53663a0b805a61100226fed3c1c7cd7`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 90.1 KB (90148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
