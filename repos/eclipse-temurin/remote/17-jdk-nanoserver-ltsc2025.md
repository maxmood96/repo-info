## `eclipse-temurin:17-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a8355585c9b75901ac79279264e7a1fa6bed4df938117332e34d78431743bb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:41cb2b639e056b47f2745d79874af57eac40f02049eaefb3d0f6b504a2ed6bcf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381584993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e34b7fe4af24153fb93d7b2e0354460f17d90895e57759e6ee877d52cb7255`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Fri, 24 Oct 2025 19:21:55 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:21:56 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 24 Oct 2025 19:21:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 24 Oct 2025 19:21:57 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:22:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:22:03 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:22:16 GMT
COPY dir:75620c5ae31b24727a476334c04df62052433150d79cd2f45de8191a02ae0b2f in C:\openjdk-17 
# Fri, 24 Oct 2025 19:22:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Oct 2025 19:22:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9257a1db65b7b020b863c0fe5c3fa83adf37315ef68be2789d5bed12ed380cec`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4ebe1ca8b215bac67349b51ad7e9c2042eb2a4b561ca6d4df2144e16d0ab70`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d512133711f92e8c11b58fae2a0f68c5f343312f48b36869d7698288d9e717e8`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb1c3a9eb2537aebb49b6dc96c730545bf7ee8126b4494ddfb7ab556e347d5d`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27655d07c27f670ecd1c33bf96281fdafd724ac3c8b4c7614325d2fe9b5862d8`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 71.7 KB (71693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a787c642ac05689f137c1ccb954193ab1007552bc368e40e7c76d7a900dd88aa`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45c258c5c290bedb8140341eff9a409571ce4e81f3c80900e633f71e04899d4`  
		Last Modified: Fri, 24 Oct 2025 21:14:50 GMT  
		Size: 187.4 MB (187353603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55137c5d81aee5fbe0ab7a83e496044c82195a11e285f9d551c1ec9e332c7a8`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 123.9 KB (123851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecea091c21eef7545ef53ce4a6c615013ebb2f4b260451343a093e6c74bd144b`  
		Last Modified: Fri, 24 Oct 2025 19:23:20 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
