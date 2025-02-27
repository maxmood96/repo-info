## `openjdk:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:99b6cee73301f3d22bf0fcc2b67adc01331a32378b2e365f0ece9735ec6531ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `openjdk:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:3d1b55c7bfa365ce293613e064a32304ce07cc95e8171cadcf3456da6b1579bd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413636917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0cb7411327ef8d0a23f2397b0c91cedeec0a7683f21e1d4d84e49fcf4a64f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:53 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:54 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Feb 2025 19:13:54 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Feb 2025 19:13:57 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:57 GMT
ENV JAVA_VERSION=25-ea+11
# Thu, 27 Feb 2025 19:14:04 GMT
COPY dir:d106a0277e031719ecf57df75fb675ae173cc670fca8c773deb70f0105f67fe7 in C:\openjdk-25 
# Thu, 27 Feb 2025 19:14:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Feb 2025 19:14:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534f1f1e4b3f98e862c2b359fd7a1b9264a30762db873d86297a8a1863e06479`  
		Last Modified: Thu, 27 Feb 2025 19:14:16 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355667f688c9841e57eb2b5864e6f415d622297fca5960779aec83a06eadaea4`  
		Last Modified: Thu, 27 Feb 2025 19:14:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4157b417b660e2379f58164f0fc523e7bf75a3e7f3066424a5d2c594c8e6ff`  
		Last Modified: Thu, 27 Feb 2025 19:14:16 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66383b37e47965fa6009cce755662da2ec6e0119ad38bf5ced46850c4d7b5219`  
		Last Modified: Thu, 27 Feb 2025 19:14:16 GMT  
		Size: 75.9 KB (75924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a687ccfa52066ce031ef3d225fdeb2f97716b7fca77f5ce4ac5683a9c1c6b6`  
		Last Modified: Thu, 27 Feb 2025 19:14:15 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b69c0858ad2238a62a2126bb9273eb28f89d20bb55e9f9214e328933e7a628`  
		Last Modified: Thu, 27 Feb 2025 19:14:14 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337da06ef136a8e66cd8445f0c94b08ca3cbe2f51d530c720f923be531c3c1bb`  
		Last Modified: Thu, 27 Feb 2025 19:14:26 GMT  
		Size: 207.6 MB (207571420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11cc49f88acfa78c33c4bc20eedda53be7b560678799f1716814b2bd0a6bb7a8`  
		Last Modified: Thu, 27 Feb 2025 19:14:15 GMT  
		Size: 93.0 KB (92984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a4baa8ee1dce1dff47038b6eee927b993b1170b632b66d9585bb773630d0a5`  
		Last Modified: Thu, 27 Feb 2025 19:14:15 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
