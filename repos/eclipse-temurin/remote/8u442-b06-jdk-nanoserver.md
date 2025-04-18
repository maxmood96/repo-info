## `eclipse-temurin:8u442-b06-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3e256e53bd6164407f23b4f9a1736da8c328eda84f214b966de0ffe40c2145ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:8u442-b06-jdk-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:750daee6b4b657a15583c333ed8ef1c8c74c9395263522a81044f7b0977f85dd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292775803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fd56d3d9fa492d2ec7cce0695bf6f9134d2cfc63ea464e1d54395f1df83170`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:15:00 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:15:02 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:15:04 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:15:07 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:14 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:22 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:15:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b846898af65c899215abe37a5261070d807f5348c3e51850e34f0763502704`  
		Last Modified: Fri, 18 Apr 2025 04:15:34 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95dfbad90b47c2abe7545417d06d636a04f30a9ec032930b4887f67c6b74cec`  
		Last Modified: Fri, 18 Apr 2025 04:15:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebf9c40498b67b8a218474bc61ee1466c06c16ea8e527d8600359af2b21d16a`  
		Last Modified: Fri, 18 Apr 2025 04:15:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcf0d3c09c0a915dc3ba93afd27a02a277abeb50e1fb8a9b45cf3baf0829b04`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba17b81f64738b28e3ec624a36694b1aeb44f1bb7113e98f27fb608aad175528`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 76.1 KB (76101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7976a261f53c7551d16b8ac722e8461af47657db6e1fece0704a36ab2ffe2f08`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6715f4303d46b2574aced974b9aab1db305cea9975f8b438f721b0320355c32a`  
		Last Modified: Fri, 18 Apr 2025 04:15:39 GMT  
		Size: 102.4 MB (102434476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1658310c618945bdc255331cfa5758456769351733e0ffba90c9c7f5c925b8`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 117.8 KB (117823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u442-b06-jdk-nanoserver` - windows version 10.0.20348.3566; amd64

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

### `eclipse-temurin:8u442-b06-jdk-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:c8768dbf6e508fcfad8a0b8baa573ec0e2d1a5f7ec64d02c2c6d85d6e5a796c8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211352484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220f192a24a5869b65e80568c51cd5fba456281c72e41926d55d63b801720905`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:11:42 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:11:43 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:11:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:11:44 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:11:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:11:47 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:11:52 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:11:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6cf7483a3034d01d420b750f53c1e61b7367c83bc60f2c0f1adf4d275841cd`  
		Last Modified: Fri, 18 Apr 2025 04:12:01 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db20f3c6f9805d6fe453f31a2c3cfa5258fb0c4d31d8963aa409bde60f008fda`  
		Last Modified: Fri, 18 Apr 2025 04:12:01 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c35a2b425dd3360dd9baeb7ca5f5878211cd2a2f69405c6a422e7ac7a3d9eb`  
		Last Modified: Fri, 18 Apr 2025 04:12:01 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245f12dbf5406c79a5e2c12d80a95186728f704082ba70cbcd6784a874a069a9`  
		Last Modified: Fri, 18 Apr 2025 04:12:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d78363dc8630ab0c4e9b28ff3c54d7c5e296487593e0b3cabeab0236c19cb1`  
		Last Modified: Fri, 18 Apr 2025 04:11:59 GMT  
		Size: 69.5 KB (69529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0367c778355db17b652bf920a74419bd7c09323d077f52d2445a6fc198a4b188`  
		Last Modified: Fri, 18 Apr 2025 04:12:00 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19be6c2452f194e7f923ba7e9866ede3f2acc07298d1438f9a1a03c63742e2d`  
		Last Modified: Fri, 18 Apr 2025 04:12:06 GMT  
		Size: 102.4 MB (102432706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b3b4cd0abb70fbc1cd2c18261421c3092e09930b6ff93875de8b050002ee91`  
		Last Modified: Fri, 18 Apr 2025 04:12:00 GMT  
		Size: 92.8 KB (92834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
