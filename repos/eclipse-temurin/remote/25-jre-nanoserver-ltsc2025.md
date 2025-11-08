## `eclipse-temurin:25-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7322b2e9f406013f473155dc97c767bd0e684fe90b4ad2d8ecf8a5f791e8d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:a00a085f9b8724dbf07e50ac9bf961c51c0e22f952abec51ff2cdc8946b230a2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252780534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e0d143b670c6256b3c8cd95927b5f36cee1f743f8ab23063a4956d1730cdb1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:19:04 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:19:05 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 19:19:06 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 08 Nov 2025 19:19:06 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:19:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:19:14 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:19:26 GMT
COPY dir:38f2d146da8b2d45f6309f76e3864fba66a43ff9541e6e5522e91b15798552e5 in C:\openjdk-25 
# Sat, 08 Nov 2025 19:19:31 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ad08b48baea3a56588296575c4bc12ecca12973a8209373e99b8d6f493f923`  
		Last Modified: Sat, 08 Nov 2025 19:19:50 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2aab27ab5d34f6185262bcc35ea90563c3f8cb04c2688666b93c92737de3166`  
		Last Modified: Sat, 08 Nov 2025 19:19:50 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d961d2a738cfd06011b88fb3a333cefe2cf156d347b7d43ad173f87d209a4c`  
		Last Modified: Sat, 08 Nov 2025 19:19:50 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480e0f89af26cd26b61dfb7c4d6e725a93402fe44fc7f391a9f830027e4f38dc`  
		Last Modified: Sat, 08 Nov 2025 19:19:50 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683d45d6e92d7e363e53dff9d87ec91891b5151a843954f801102a25c0987e0a`  
		Last Modified: Sat, 08 Nov 2025 19:19:50 GMT  
		Size: 69.8 KB (69781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50deea7238f462072b95239656e26d7c772b435982efa8cf749135bae0c2a52`  
		Last Modified: Sat, 08 Nov 2025 19:19:50 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33a12ad606ec1497b3afc60e0fc08273afaa84a1c362618f7558c47a2a46b70`  
		Last Modified: Sat, 08 Nov 2025 19:19:55 GMT  
		Size: 58.6 MB (58563770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c3e7ba40f57086fd2c61c67a3c7b6d225c9805553261977258f71df1257b4`  
		Last Modified: Sat, 08 Nov 2025 19:19:50 GMT  
		Size: 112.3 KB (112300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
