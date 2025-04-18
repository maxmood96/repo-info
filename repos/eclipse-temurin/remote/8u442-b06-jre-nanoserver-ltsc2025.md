## `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:afa6d7158f7702aabc53effb9e095fac721a5c1a336adb828631e54b2bd09ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:c086fb65cadd30ad3648255c288253936087fa7791d3104545df0600896af468
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230871628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d0b64ed1e8fa0e32951194058e118ef35f15de482b76b879f96b647e2d2f0a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:17:11 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:12 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:17:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:17:15 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:21 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:26 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:17:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b2352202160345b8d24370a5c8b6979c17edd474a58cc34b583c607e8f401`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d83647f952f5e831c597de15465c8e2af9162bf229505a766d60737a35fe1bb`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14951b2adaf7fc0394c4b602a328b26dcb984fd7b51203a150015a4185147423`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c002918b74cd6710d2a6e3e3caa26fde517d88af44050c1e15f240d095682cb4`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638d75622150c5c83138fec9d917d9389df3515e9b6b7feb1a7a9609a8a13f99`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 78.5 KB (78540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba615f9f70690cab3cb3b0395e771bf31a2049b473e42aea2ebea1b1c56c932`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349b3b48f600d984770f2c6a4f449a33257d8cbce2d48577ab7ff10c243f4ecf`  
		Last Modified: Fri, 18 Apr 2025 04:17:37 GMT  
		Size: 40.6 MB (40552726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3ee4b2297e79195d5d3062572cbf30335fe760b60b86528002a9fca84a1ab5`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 93.1 KB (93086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
