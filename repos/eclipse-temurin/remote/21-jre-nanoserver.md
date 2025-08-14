## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2a7ad8d9f16ce46bb8531f0c10a9bb4979a3fe61389e8fe73c7852c779f0dbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:9d3bc78098349373abbe1b35a34e384ef25092c7b66b4c68bc1a969381c1da2a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242657685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202691df172d83087eeb1706c864c6f1f46ac4343b4550dddfa1ad5a2491d52b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:13 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:14 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:50:14 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 12 Aug 2025 20:50:14 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:16 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:20 GMT
COPY dir:c21dbe47d2de1b48c1d9f92222d71f88b5c065d2194c2f26a7fb8e303259e21a in C:\openjdk-21 
# Tue, 12 Aug 2025 20:50:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cd7903c58f17384f40faf3bb0a5dc583db6cc3eb7be6b1fd5a5fc8e1667997`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f554b82243d6f76b06266b0041c96aac01bba1f29e85fb3b901188a50b43190d`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eea5dbf744d71e86ac17e6bf16d3ae9d3019799b4f7116551f40d5d21ca0820`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f979a56fb98584cff3dec2fd540fdd324669c18ab663974933592a269ad4c1e`  
		Last Modified: Tue, 12 Aug 2025 21:16:55 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b196546fa4e2d0c50ec3a1972197bc8a60ffdcb096fcb94fcb00e4686cc5256`  
		Last Modified: Tue, 12 Aug 2025 21:16:54 GMT  
		Size: 75.7 KB (75692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367a0eda1bdbfc75675db9f2c177df03f2fec6c2f72ed808958dbc3e7f349ace`  
		Last Modified: Tue, 12 Aug 2025 21:16:55 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e242cbeb7349bc9620293c4870d77c487ddf4e862db8d6a689e40cd726c5510e`  
		Last Modified: Tue, 12 Aug 2025 21:16:58 GMT  
		Size: 49.0 MB (49011114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f96eb2a768023a1dd02808c00c904ee112e58f88ab40005f9e68272563f0b2a`  
		Last Modified: Tue, 12 Aug 2025 21:16:55 GMT  
		Size: 96.1 KB (96074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:2c6d5f70fb856378869f7c6d0e44dd7dd60692e8a1961ef674863ecc66305056
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171853798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c59e9ee2d92cd098a47ebf122c2540c7c80d2ec9294dc378e21b39c10b7c7b7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:32 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:33 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:49:34 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 12 Aug 2025 20:49:35 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:49:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:49:39 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:49:44 GMT
COPY dir:c21dbe47d2de1b48c1d9f92222d71f88b5c065d2194c2f26a7fb8e303259e21a in C:\openjdk-21 
# Tue, 12 Aug 2025 20:49:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97ef17430283c1167cde09f4da8f6d2ea6d44be202557eaeb5a7f1c3d78deb`  
		Last Modified: Tue, 12 Aug 2025 20:50:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1aa4fbceb3dd70d1e7e179f2a104a4bfd69e31dcd9b7d15e19928dd9c50c03`  
		Last Modified: Tue, 12 Aug 2025 20:50:35 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d677af76c11d1fa786dd3add30f08096a0bb8c8236ff62f0c499534c0b75da`  
		Last Modified: Tue, 12 Aug 2025 20:50:35 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32788969f1515ab3035c2f1974022499c9172e7b740bd2d35a3786624e9a328`  
		Last Modified: Tue, 12 Aug 2025 20:50:37 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159037af763cce38f478e554aa627f23476616f6f9c84255b762b9c03926fa99`  
		Last Modified: Tue, 12 Aug 2025 20:50:34 GMT  
		Size: 76.2 KB (76202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da3a3c0c951b9f2882f1b77321edc4a92293b770693158726861610385d1f5b`  
		Last Modified: Tue, 12 Aug 2025 20:50:35 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9c09b8ffac427d17710b0be4f88a22a9ed7a4cbb5cd8c30ef117bb792f7257`  
		Last Modified: Tue, 12 Aug 2025 20:50:39 GMT  
		Size: 49.0 MB (49011356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcec88bfc459665890d17b9419e9c1f6ff41a35f87aae03285705a4ae19421`  
		Last Modified: Tue, 12 Aug 2025 20:50:34 GMT  
		Size: 100.8 KB (100753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
