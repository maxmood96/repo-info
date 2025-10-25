## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0a58fad38de71088445ab70ca4b32f991ce9dc6f54e1e5e2198f2d1d0a081e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.6905; amd64

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

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:2fa76132b4708437ef54783b1e6a1ff9ede164f8691f2c22862fc4942d17f3e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310256594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b3cb7eb8cd0964be3212a319a5c5e6f6e3cb99b22ba71d0bb4e880cd0c979c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:19:18 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:20:42 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 24 Oct 2025 19:20:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 24 Oct 2025 19:20:43 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:20:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:20:46 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:21:10 GMT
COPY dir:75620c5ae31b24727a476334c04df62052433150d79cd2f45de8191a02ae0b2f in C:\openjdk-17 
# Fri, 24 Oct 2025 19:21:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Oct 2025 19:21:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde8d3892490c03c6867f198f3dc45e69fe1049b2d63e6fc8a4a21f54095e87d`  
		Last Modified: Fri, 24 Oct 2025 19:20:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9581df62aaaf2a6a24830901fbfc0bac2faa74046ee41e8b9da720538647aeb`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03290cac1f030e1eedde31a38d5cb12f78dd8b0a60078b719dcea75100524c3f`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe8f0ed4aa237a5f1a4785841a222a9ed1e197475726bb88704851892893cbf`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33febd4530edf0a14d178e5dcb80bbe021598e635ad30f7add8e3ac3314fde37`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 76.7 KB (76684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7e5d60108d2a76abe3bdcddeece786acaf05cf3ca918cfbd60c901aed18e6`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab91ad86c4ca47af7e5ef43f1a930586e86cfe1f4427a776e113eba5968b2910`  
		Last Modified: Fri, 24 Oct 2025 21:14:41 GMT  
		Size: 187.4 MB (187353782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca6191a1d7cb89f9a964784d7d2af488567ad5cd43d14d7b6c517ebb77e8988`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 135.7 KB (135672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84680271c5080fa59d5bbdcf6dd08d217c13a3e4b9fc7c794021a879cb047f19`  
		Last Modified: Fri, 24 Oct 2025 19:21:40 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
