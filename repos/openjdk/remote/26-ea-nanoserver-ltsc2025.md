## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:8ac879fb556101f3e264914f44d3a20a803320289d631095607445a55f268000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:b2de8d70afa2dd3072077ceb7941c379dc161d000aa12ba9c858d463b1f38b83
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415494548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd168944a22f4e97a234b780660702effd2ef8821e768774cf2b7bd00a9bf037`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 31 Oct 2025 21:15:15 GMT
SHELL [cmd /s /c]
# Fri, 31 Oct 2025 21:15:17 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 31 Oct 2025 21:15:18 GMT
USER ContainerAdministrator
# Fri, 31 Oct 2025 21:15:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Oct 2025 21:15:33 GMT
USER ContainerUser
# Fri, 31 Oct 2025 21:15:33 GMT
ENV JAVA_VERSION=26-ea+22
# Fri, 31 Oct 2025 21:17:01 GMT
COPY dir:c90d7d97d7a92e44aebce14c599d37116856dad8a1bf4d9fcb77de537cf1c0aa in C:\openjdk-26 
# Fri, 31 Oct 2025 21:17:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Oct 2025 21:17:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058a353c2488f5ee182f90c36c5f683339a76ef6dca6089ad1d58e10e593bc2f`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2e48dfa4158c36bb6d22ea93a894cc958d7c0de9fb0cbe376e13623362cfe8`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574756a6681a7e7509dd222da5c8270e4263624a80ab28426f8b8ba042d6aff0`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b191ad5485c6707a4dd219f060de3fb5dad14366bb7025e461dc6b466762b8b2`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 71.0 KB (70972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72ee8ba120d678ddddd8e0704d914eb728a9646d1aac3164f08060fc28ebda3`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0bcdd1b4d84adf65b7c3ba5af7af01b02310230018db10a7f1acc0ea5bddca`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd0f3d24fadbd551bf8e484526826d62a9f67014fa431c962d90cac6a80f310`  
		Last Modified: Sat, 01 Nov 2025 00:23:55 GMT  
		Size: 221.3 MB (221284997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02213e244532eccaab7bbf907ee0f60c2ffc4923bf5278f21b85ada58c34c0a`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 102.8 KB (102758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d8be3c61cc2e4585ee47dca34bf7291c7029ae649779e1134285c52a12e71c`  
		Last Modified: Fri, 31 Oct 2025 21:17:37 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
