## `openjdk:24-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7e270118eb1d2ad1776c1f09816261f8b0d4de5ced843d42669c1bba65d219fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-ea-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:948ec1af7af4bc7cdad3babe81f28682c948d5325f28dfee281ff9029f0159df
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367300402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f670f298d6e5f4824185548fc10b69c346a5dff1bd6cb9d46e3066f7a2ee4955`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:07:35 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 02:07:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Sep 2024 02:07:37 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 02:07:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Sep 2024 02:07:40 GMT
USER ContainerUser
# Wed, 11 Sep 2024 02:07:40 GMT
ENV JAVA_VERSION=24-ea+14
# Wed, 11 Sep 2024 02:07:56 GMT
COPY dir:4f2970b6340f2cfe63b9e3f11a70a1b094e6fbb8d6435dc5c9906911ec8278a3 in C:\openjdk-24 
# Wed, 11 Sep 2024 02:08:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Sep 2024 02:08:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8d05c579ad606574e853c93204d8bbab2b84ae484b6102e6a282a7c8db6e45`  
		Last Modified: Wed, 11 Sep 2024 02:08:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc22cebe32b4b72e7d58a568c42aef5c48a8682ea127806b06332931495a2c88`  
		Last Modified: Wed, 11 Sep 2024 02:08:07 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe8405ff9d27f8f43933f19cab8b9ea2d90c820d48d4b4ac2937b285c3f3d8c`  
		Last Modified: Wed, 11 Sep 2024 02:08:07 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709e2cc4354c104ff92608fc55405debedb8c7bd77176830e4bcb67e71849b44`  
		Last Modified: Wed, 11 Sep 2024 02:08:07 GMT  
		Size: 72.1 KB (72086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624ffed886fb93a21bbd5f6afb24dd898f2f9ff651fb34ededf74f077f8c907`  
		Last Modified: Wed, 11 Sep 2024 02:08:06 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7dbbe8038a5e8d8cb2eb226da36627c50f172d9554ef2bda872d8adc0e13dd6`  
		Last Modified: Wed, 11 Sep 2024 02:08:06 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def990a743c41f627c985263564585cafd40aaa3699d26f29754527c0e50ca9`  
		Last Modified: Wed, 11 Sep 2024 02:08:17 GMT  
		Size: 207.6 MB (207617818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbe421cf647ac6094a4fe187defdecd5748ce0a997e2c04cd82abac55e00a15`  
		Last Modified: Wed, 11 Sep 2024 02:08:07 GMT  
		Size: 4.5 MB (4523409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae947aec0eb6d11788f62f1d71151945244818a657aeef024d6129b27fccb47`  
		Last Modified: Wed, 11 Sep 2024 02:08:06 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
