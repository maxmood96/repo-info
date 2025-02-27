## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b3b61366ca952588f355826c171d3943c97f117f1445972631bc41864e000020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:74fed05de50ba27c63d2a0264c31c6f0d3149c9c00209f63a41638b0eefd32a6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.6 MB (400635597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42eaf281ff32e130bdec2694929ba18fa8dd1f4872ea643411361f7a742b24c0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:13:47 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:13:47 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 27 Feb 2025 19:13:48 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 27 Feb 2025 19:13:49 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:13:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:13:52 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:13:58 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Thu, 27 Feb 2025 19:14:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 27 Feb 2025 19:14:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6a9404db65d497a492e7c61c24164b0c394a0d2a048fd934b8b4add3f401b2`  
		Last Modified: Thu, 27 Feb 2025 19:14:08 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07164d534b2010d7df248484dffd015dc9a7088dd5955ca12851b7b23bebe83c`  
		Last Modified: Thu, 27 Feb 2025 19:14:08 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8ff781d3a42dc4007e60fff70325b2010bb31b1b1842c415c0e7d44c0a9633`  
		Last Modified: Thu, 27 Feb 2025 19:14:08 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182b7115d11d8cd0b58cce82efa1e3d2aa1efb948c9779522b100022acc41cdd`  
		Last Modified: Thu, 27 Feb 2025 19:14:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc40cdad1c17fdf6d3a780d3a6e2e25b802290d874554fd393b47cfbe8dd3b9`  
		Last Modified: Thu, 27 Feb 2025 19:14:07 GMT  
		Size: 77.3 KB (77257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d20644ca211962ef55a0c2400be5606bdf42816d97f6388bc2d0bedd295e9b6`  
		Last Modified: Thu, 27 Feb 2025 19:14:07 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5015f2132b794db81782f3077fe50bce033f44b960fc6bd87969ef30e547b616`  
		Last Modified: Thu, 27 Feb 2025 19:14:17 GMT  
		Size: 194.6 MB (194557008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3950b104783f7955d871062fc48f6363731ea584ec1670782a693b5c508d267c`  
		Last Modified: Thu, 27 Feb 2025 19:14:07 GMT  
		Size: 104.7 KB (104694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7806ba3dd940e0f7c3bfd2aee38bd1b94aa7e4b22d92ee68c67d0cb906c4085`  
		Last Modified: Thu, 27 Feb 2025 19:14:07 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
