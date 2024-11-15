## `eclipse-temurin:23-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:29e593ecba8d8c095db1e49a93f4257ab711e5188a71c1c43d158918470f1160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:23-jre-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:d648904309bab55a0e816995b9538743376a42d259831bf6c0d1a3f847235922
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170399288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4ad9d9b5855129a8771410a4034ca97aa1ef5f28d1a3ff6b0eaf2910b994c4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:16:25 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:16:26 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 14 Nov 2024 21:16:26 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 14 Nov 2024 21:16:27 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:16:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:16:29 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:16:33 GMT
COPY dir:d9adc234ed2c06cd6b72c0beb8933c6d824941dbd1cece41e4fd2578b0632fbd in C:\openjdk-23 
# Thu, 14 Nov 2024 21:16:37 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5bad70ac60cdf1823472d69956966bc7968a3e23889675599edecdd1e0c9a1`  
		Last Modified: Thu, 14 Nov 2024 21:16:43 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6004507875b1e8a594af0ec58b7de8f8144d666e6258b7cd1f2a428645b79993`  
		Last Modified: Thu, 14 Nov 2024 21:16:43 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0e2f4ecab2a33d892f0dc20701a612ea8958b740d8206951191299ecd9261a`  
		Last Modified: Thu, 14 Nov 2024 21:16:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c3d94f9158c0f82211ff019bfda0f8409b674b21e7c21eac48abc0efefb166`  
		Last Modified: Thu, 14 Nov 2024 21:16:41 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7780c172e3bbb9ef6ca0b72420a7cf93447d051348be88f7c578a5f0bd0eedc5`  
		Last Modified: Thu, 14 Nov 2024 21:16:41 GMT  
		Size: 77.5 KB (77480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e351cb28a36e9dc86bedcbf29372111e547b41a5063df8e4d6bc5905f1d8f735`  
		Last Modified: Thu, 14 Nov 2024 21:16:41 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311961a94c081450c7b09c824d14a67c2079b7a6c20fb0c92a0bc32085599713`  
		Last Modified: Thu, 14 Nov 2024 21:16:47 GMT  
		Size: 49.6 MB (49610138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367fa0e997cb5dd68cbb128287abe4247b87b6f773b5bd3c433a5be13b7b0e12`  
		Last Modified: Thu, 14 Nov 2024 21:16:41 GMT  
		Size: 101.3 KB (101348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jre-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:3bd514918c990a61946375eaf991291a74c54892b09eb433df184c598ec1c9b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208534680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2af15e15cfcafb019135fbe7fce53974aeb1a6649d921f15dd1f1bbaf529dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:21:41 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:21:42 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 14 Nov 2024 21:21:43 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 14 Nov 2024 21:21:43 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:21:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:21:46 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:21:50 GMT
COPY dir:d9adc234ed2c06cd6b72c0beb8933c6d824941dbd1cece41e4fd2578b0632fbd in C:\openjdk-23 
# Thu, 14 Nov 2024 21:21:54 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e3b19ae54bd848681f2284303cbabd026a76a133faadadadd8c6e9d7648188`  
		Last Modified: Thu, 14 Nov 2024 21:22:00 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f278e9e3deb6563fcb0784df110f71b4f0df2bee0c31ad1f820d8206cbad7d`  
		Last Modified: Thu, 14 Nov 2024 21:22:00 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f166b5f6d9613066aa308243bc7978c1e6762155d0d8d1689d7593af122d0cd1`  
		Last Modified: Thu, 14 Nov 2024 21:22:00 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dc08b4accc00c8334f2153753a0ab56ad006ee22236cf0782e1d33f06bed12`  
		Last Modified: Thu, 14 Nov 2024 21:21:58 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59038b0f532e20eb639c4dda5ac33c5f2f8c8545e6060b1fe115b19362e59246`  
		Last Modified: Thu, 14 Nov 2024 21:21:58 GMT  
		Size: 74.5 KB (74457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3201e3a1255e2bd0cf3a32e8baae990b6ed2b09ebef71124e937a584ffe9a3`  
		Last Modified: Thu, 14 Nov 2024 21:21:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fd231261257da4a683d82edf8bb904c8c3125d8a08c301a038c52b95abcdc`  
		Last Modified: Thu, 14 Nov 2024 21:22:04 GMT  
		Size: 49.6 MB (49611528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5d25226509347bfd1a92f8c47522cbfa907d8786b686f9aa7eeb1684d093c5`  
		Last Modified: Thu, 14 Nov 2024 21:21:59 GMT  
		Size: 3.6 MB (3628926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
