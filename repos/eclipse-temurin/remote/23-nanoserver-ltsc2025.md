## `eclipse-temurin:23-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:fff8f8fcd4ca6a3fbc4754b5f9fb16adf71c47055471ce2e54788f93fd9464b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:23-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:62638293d16643ceed239c0c8251e64474423a545bc4ff7f1253541b680b31f4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.3 MB (409336052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddc8d5cd794313834f79e6bb0625d00d90dc14bc9db4932ab8389ae3fcffe7b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:52 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:52 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 19:34:53 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 22 Jan 2025 19:34:53 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:56 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:35:03 GMT
COPY dir:997f391ddfc9feaa4d1b725e1babc077a76dd78201dd489cc8f03fe767c19cd0 in C:\openjdk-23 
# Wed, 22 Jan 2025 19:35:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Jan 2025 19:35:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d22ecd46f907c71487b358f1e7d6fdb118b99254fff2017c48e61923db7c43`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959b8753e08fefc422949e00dd50b69f12c7afc4f060e21d7cb328ef830c498`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9959b6a28f6e9c73a01ee70d1ee9b0e7ed9ad79708632222bcbbbac0d2f93f08`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d36961fb2b2a4da0b87e5c0cbb97c32776539d2bfe4f28f22747b73bb7c57d1`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5693ce293f450a7ba0fbeb3c56865d93923063a156bbf7f64174ad43a505a4c5`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 76.2 KB (76154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60977d3727568d8efd30a6a9de0c8bcd64d32fc03f8ef85f71dbba7d26af278a`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cfc20225b7c5f4a37236ec25a8157146b0cd17334e538f7465fc712cb40d3d`  
		Last Modified: Wed, 22 Jan 2025 19:35:27 GMT  
		Size: 210.1 MB (210105881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5d455da88e3829365d95908eb5ee60f8e23d9f46ae39133bb281580db5cbaf`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 93.5 KB (93476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5840a3d7243ce114e16b8cc74811d09ca9a1843792f8028b06e6ab1b5c57402`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
