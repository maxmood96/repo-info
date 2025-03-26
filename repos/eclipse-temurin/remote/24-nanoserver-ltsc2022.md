## `eclipse-temurin:24-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5091e5aa8b8d23feda406dbfc2299c5675851e2fbc8de9198121a77ee4a192a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:24-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:2cbe404936e80155ecaf3135b01939efc696094863fb080be573a51e6a275d4b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258240422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0239db6d1a7f0faf196fa548bbe5ed346063dadc6fa1bc463c22a7e640d19ac2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Tue, 25 Mar 2025 23:26:04 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:26:05 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:26:06 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:26:06 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:26:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:26:09 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:26:17 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:26:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Mar 2025 23:26:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e6ffb79d9315b5241076ade3856244a705c31f5a7c9c10b6149df1a4900dc8`  
		Last Modified: Tue, 25 Mar 2025 23:26:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfa1056b3ee7b5cd69c2fd29bd1dccefdec46ed40b06dfbbfc7b68674db4f5d`  
		Last Modified: Tue, 25 Mar 2025 23:26:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cc68a6758888000a724dc3285d7b8608e683e1c8851881246e3ab0840ab094`  
		Last Modified: Tue, 25 Mar 2025 23:26:26 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7f122edb834b8b41030c868a6b1141cd281d07713b99c03c152da51b256c82`  
		Last Modified: Tue, 25 Mar 2025 23:26:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9ca459ed970ac5a9099526af76c8dded05e1c73288d3d6bb9becfb42870c91`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 76.2 KB (76216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf301c0b506ab9d65210d6ccd31b711383a07f30f4350e6066ed2c3711b35`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f33d8c8e01c272b34b89f56a48461754b6f24604457fb0c37fcf3f6e0c49f9`  
		Last Modified: Tue, 25 Mar 2025 23:26:37 GMT  
		Size: 137.4 MB (137355283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30debebfd983b79e2baddc283eaa90bf33a4eda5ae3e3ca28223045a2d4d7d1e`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 107.2 KB (107174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d1ef7b604437a77cabba7e9d072260146eba0b4a4acb4ecb3533cd7c5d1903`  
		Last Modified: Tue, 25 Mar 2025 23:26:25 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
