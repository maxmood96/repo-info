## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3ece3c5ecddeb1d40fabfc47e4b0b6eaeb80cb399bde8723df8fde697e438e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:71d34db30e8aca79724c71295b87d26837c3d3c8af2ae7b7089660759923b3a7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.2 MB (310233479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e14eff0e6a8416c86ab80d6f9ea5b7dd01d69d6b89261458d2f0362e1b1cd9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:13:03 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:04 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 14 Oct 2025 21:13:04 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 14 Oct 2025 21:13:05 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:07 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:14 GMT
COPY dir:75620c5ae31b24727a476334c04df62052433150d79cd2f45de8191a02ae0b2f in C:\openjdk-17 
# Tue, 14 Oct 2025 21:13:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 14 Oct 2025 21:13:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f1e119dfe09d5adb40d4b3db9bdd1593373dd9757473e2d43212478f29a903`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337531f6c68edac8bdb57fa1d5ffd26e3a1f75aa5b3461f4266ba31ceb7da46d`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19edeb40dca34d55ebdbf2e3b128a6fd1b323c80a85bc2699d1aed5593a3bfbe`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3967b94c469b8799eadd83229d5d01a94d4db1be596c42fada766f45ee8c56bc`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a1d0f7a38f11a9fccdbb81deae69056077776e709bf89d831a09393b03dda0`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 77.1 KB (77146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c12339a1c82fac7e9a3b37cc334bd67413bfecfbd77f212fd332cd07bb053a`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994b5db2d33eaa86bd6d4427a97066862d829f699f7a7ae4cc04f368fa361812`  
		Last Modified: Wed, 15 Oct 2025 00:14:42 GMT  
		Size: 187.4 MB (187353700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2d835c5714ab1eb6b37324b7499f5d4a1ade4793cb0ae3dab315715fbc5206`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 107.4 KB (107375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec50f571f585911789a895ff5861c931a736a3e5aecd432835daa6c0b9841d9`  
		Last Modified: Tue, 14 Oct 2025 21:13:43 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
