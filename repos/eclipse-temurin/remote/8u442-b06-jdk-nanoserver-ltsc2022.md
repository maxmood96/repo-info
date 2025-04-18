## `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e97b9157b7b7a72b31de7008b0ab70184611b7949947f81f09788773f969531b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:d5c1d4f18c5607e105e68c2d13b6eb89f1aeef510be4ddbeb0482ff3f38d5b9a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225172795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f70f18a410556d1cf4fff4287f707d535125c4bf271214892532a38e4f90e7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:20:13 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:20:14 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:20:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:20:15 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:20:18 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:24 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:20:29 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6d43f47fff32a9dfeea1c9b7f43718fb8d0b89c2e7027a1e1df2a96034a997`  
		Last Modified: Fri, 18 Apr 2025 04:20:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbebfbdeb53f6a421b8e9a4eb1d4c60153b041db1ce95ee064d902478081f95`  
		Last Modified: Fri, 18 Apr 2025 04:20:33 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb9e73d07576ba55af247e47b4c985a6c8f361f07abf4405f6c50f141729f6d`  
		Last Modified: Fri, 18 Apr 2025 04:20:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4529f300859798dd60ee8f3c529a9ebb80bdd8746045b81ce40fdf17ec4046`  
		Last Modified: Fri, 18 Apr 2025 04:20:32 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3387a41a04c4448eadf13ec6a842754e3f5d70d2abb22d747863048462e395e`  
		Last Modified: Fri, 18 Apr 2025 04:20:32 GMT  
		Size: 76.8 KB (76838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31cce1e0e4fcba68d6981f66e6ea2deedacad7d88ca70642f481b9775db130b`  
		Last Modified: Fri, 18 Apr 2025 04:20:32 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16584afd89916bafdf0b33c3d9f8793d7037f957f26ed0fdfd6d4aa1394d3a5`  
		Last Modified: Fri, 18 Apr 2025 04:20:39 GMT  
		Size: 102.4 MB (102432711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e733bdfe01d36f146633148b5e9b3eea22730441bec256ba07a716d9ea08ca4`  
		Last Modified: Fri, 18 Apr 2025 04:20:32 GMT  
		Size: 119.0 KB (119023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
