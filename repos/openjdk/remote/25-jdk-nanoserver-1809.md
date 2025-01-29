## `openjdk:25-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:64849f808a61165e4f6b404656569c6c1eb6a9b765aaf05abc731cb4a564459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:8a2d9deb7058b9d74730ccdd8ecbc172aab786a419a797472155ba8ccb59a24a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367100234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d686867f0d25554729fff7b2bd3f4a1a2ff580d30a43ffc041b3c88f65878e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 29 Jan 2025 01:27:24 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 01:27:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 01:27:26 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 01:27:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 01:27:39 GMT
USER ContainerUser
# Wed, 29 Jan 2025 01:27:39 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 01:27:49 GMT
COPY dir:8eaf4d943fad5808ffdf3732eba720fc3864b955a0e8f89e481534183a904eb4 in C:\openjdk-25 
# Wed, 29 Jan 2025 01:27:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 01:27:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea67f5cdc1f2758c05b742b3e18a51efe2bb84d95020f59547470834df302c2`  
		Last Modified: Wed, 29 Jan 2025 01:28:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5937f73c9dd7e7eb0aa74ae847a39230006b8697b79a0f09a78698cdede31f7`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f8853451649bf457a5f4f9043c782fdd7978834cf0d58090be6e5dac8fce11`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45bc0e37a6c5e649bb725fb45bd7ecd7a9ab5a414b9970c174aef2b6683543c`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 66.5 KB (66519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de981d3231be646cbb4cd007372432f5534c9c5a5948cecada4e1f088cffac3`  
		Last Modified: Wed, 29 Jan 2025 01:28:00 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0436519f0d5ec3a6f647f52718f47ed632aecbc02aa3c293b32463edea63f0c`  
		Last Modified: Wed, 29 Jan 2025 01:28:00 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ecae1a982edbfcd9cee7c3887b2ce1f678d08fb4132fb25e7bb49863bee5f4`  
		Last Modified: Wed, 29 Jan 2025 01:28:12 GMT  
		Size: 207.4 MB (207391618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022c92a76b53052181e80c34182885f10d9221b588ae1f624f89deb302dd8fdc`  
		Last Modified: Wed, 29 Jan 2025 01:28:01 GMT  
		Size: 4.4 MB (4368034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d63d72b7a2d42347486dbe865135ecde74dfba96ed50333208cfaa18e695fa`  
		Last Modified: Wed, 29 Jan 2025 01:28:00 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
