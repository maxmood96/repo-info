## `openjdk:26-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:04470579646e407ab45890cc7e10a312a1480e8c8b03f8d8c27253ee0bc08b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-jdk-nanoserver` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:d7ff00ae2773e537ac170c20da0c61c30dbcbf9aa08440eea8e410e01e774ec4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.4 MB (415434951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57b56e41796f89a5ecebbe0d54dd8fb960181667c17f7580eeb5fe6fd6e90a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 25 Oct 2025 00:14:47 GMT
SHELL [cmd /s /c]
# Sat, 25 Oct 2025 00:14:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 25 Oct 2025 00:14:48 GMT
USER ContainerAdministrator
# Sat, 25 Oct 2025 00:14:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 25 Oct 2025 00:14:54 GMT
USER ContainerUser
# Sat, 25 Oct 2025 00:14:54 GMT
ENV JAVA_VERSION=26-ea+21
# Sat, 25 Oct 2025 00:15:09 GMT
COPY dir:75f3cf006fed87c0bf0323991c1dd3aaf526a74e8f52d2d9c31e5201bfab4b57 in C:\openjdk-26 
# Sat, 25 Oct 2025 00:15:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 25 Oct 2025 00:15:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abdd3259ab9c7000d11ffa489904bda4fe616fa6c9ba76dcbb3d913393377c8`  
		Last Modified: Sat, 25 Oct 2025 00:16:17 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdee297a2224d4761bdb7fcedbaf4ac5002ab0edeb7926b840d4fdf09eb4745f`  
		Last Modified: Sat, 25 Oct 2025 00:16:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efac6ec08c1e6a0706f064e0495f23a052f45fccfb4585d6a37796e6ae40a94e`  
		Last Modified: Sat, 25 Oct 2025 00:16:16 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb1ee24c838e1f1886976c5c477c39a9ecb8da76750ee7525793cf471884e6f`  
		Last Modified: Sat, 25 Oct 2025 00:16:16 GMT  
		Size: 71.1 KB (71070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7999b623cb73f515940e5a31bcae64608073a0e7aa7109c5d5405b9a7a2090e`  
		Last Modified: Sat, 25 Oct 2025 00:16:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb14162c98762b551de14fb341ed7bf4c24e4d27ef1e994a0d44d739e2c0fcb`  
		Last Modified: Sat, 25 Oct 2025 00:16:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c3103b2f9b3d96e15b04f15ecf45777e6ecefdcab9811471f95ed0bc6387fd`  
		Last Modified: Sat, 25 Oct 2025 03:24:28 GMT  
		Size: 221.2 MB (221224622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f49bb411781e8194abed3626d5dc5578cdf49e0be23c63e0db403cf97acec2`  
		Last Modified: Sat, 25 Oct 2025 00:16:16 GMT  
		Size: 103.4 KB (103444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b30c1791ff0c517d6ea5c303214eebd30727418bd4b86d0690be4a32a85c7aa`  
		Last Modified: Sat, 25 Oct 2025 00:16:16 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull openjdk@sha256:e7beb397a3c48d237f96b8ed7ba8fd0c67e74738d4fea0682e6952a5a404cdbc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344156734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a666bce5957323f4beae04f9de5acc32f9d53ce9030d24a71cbcbb983868db`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 25 Oct 2025 00:13:39 GMT
SHELL [cmd /s /c]
# Sat, 25 Oct 2025 00:13:40 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 25 Oct 2025 00:13:41 GMT
USER ContainerAdministrator
# Sat, 25 Oct 2025 00:13:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 25 Oct 2025 00:13:47 GMT
USER ContainerUser
# Sat, 25 Oct 2025 00:13:47 GMT
ENV JAVA_VERSION=26-ea+21
# Sat, 25 Oct 2025 00:14:21 GMT
COPY dir:75f3cf006fed87c0bf0323991c1dd3aaf526a74e8f52d2d9c31e5201bfab4b57 in C:\openjdk-26 
# Sat, 25 Oct 2025 00:14:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 25 Oct 2025 00:14:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e12ba7359130451ec19d8074136d5508a9431b8cd4239a67495b0975ada9e8`  
		Last Modified: Sat, 25 Oct 2025 00:15:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8f72d0cd2fd9d09d27db1fbcac62a937a8b9546b4ce2fffac1d295ce434eca`  
		Last Modified: Sat, 25 Oct 2025 00:15:16 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d939870f18e5956f4ad19c9d1e1be04688f89ae7f303cb8b7ee3905110581bd6`  
		Last Modified: Sat, 25 Oct 2025 00:15:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfae970fd140a93f4e0670fa54b7b736021715fdc37392cd10dd293743d0562`  
		Last Modified: Sat, 25 Oct 2025 00:15:16 GMT  
		Size: 96.5 KB (96494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2867763bb6b9add2bf870198f45165a186aafe9d52852825e7e36d49f02380a3`  
		Last Modified: Sat, 25 Oct 2025 00:15:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f667a16e21eec0d0a5af880b5ea6bf3f4eb32867fec43304ffaddfef1f11596e`  
		Last Modified: Sat, 25 Oct 2025 00:15:16 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf30a4e41569061ddcdddcc27fae1010f5adabd755775162544c201211bfe18`  
		Last Modified: Sat, 25 Oct 2025 03:24:20 GMT  
		Size: 221.2 MB (221222663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85a3943db4d814ed5ebf692cfd60d35569d7434106b29829d34c336a2d302a`  
		Last Modified: Sat, 25 Oct 2025 00:15:17 GMT  
		Size: 147.1 KB (147111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee7eb0da3a176ca99a31b32dd0b48bceba68e41cf2c7110a441deffe5cfd4d1`  
		Last Modified: Sat, 25 Oct 2025 00:15:16 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
