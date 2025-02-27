## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1feb6900ecf713fe75e2dd71368dbcb00f647ff2bb4d2cefe134926e23b1c126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:53640ee1b997f6cb2ecbf20c21270153be19b2dda5d9a27b446c24b7c87526c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 MB (407542502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd01cda64cd4ffb446d4585df2a0829c301f134d6d9f315aa9c261b3a8a31d7e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Thu, 27 Feb 2025 19:14:33 GMT
SHELL [cmd /s /c]
# Thu, 27 Feb 2025 19:14:34 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 27 Feb 2025 19:14:34 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 27 Feb 2025 19:14:34 GMT
USER ContainerAdministrator
# Thu, 27 Feb 2025 19:14:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 27 Feb 2025 19:14:37 GMT
USER ContainerUser
# Thu, 27 Feb 2025 19:14:43 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Thu, 27 Feb 2025 19:14:49 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 27 Feb 2025 19:14:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f96d6b2b03e6c1728cbf070319dca1b0cf627dedb63a9979953fa657b58524`  
		Last Modified: Thu, 27 Feb 2025 19:14:53 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567dced4efb575e1b34f0fc8a603a539445d3ee26838ba3f15455fc6c7fe9b3d`  
		Last Modified: Thu, 27 Feb 2025 19:14:53 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25451fefa165012e43053d831d605c663b7682117365f24d0211460aa3daca`  
		Last Modified: Thu, 27 Feb 2025 19:14:53 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48921d7043c8a0a90dd075ffd0f472b1c5790b571436c53a96f8f7184f8a8854`  
		Last Modified: Thu, 27 Feb 2025 19:14:53 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6a933f59245cf19d79bfc38aa3cd95f7a46b8bedf77a09a0e2e02108df8a4`  
		Last Modified: Thu, 27 Feb 2025 19:14:52 GMT  
		Size: 75.9 KB (75929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced592016afafe3ae22d34ca16f2c2b5a681bb16f042914185cfe35fdb0b51ee`  
		Last Modified: Thu, 27 Feb 2025 19:14:52 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e4a0f5ee60baac65232f3e0747d12275d85505e170a9885c9aaf18c13f1066`  
		Last Modified: Thu, 27 Feb 2025 19:15:04 GMT  
		Size: 201.5 MB (201476201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e13f4e30b0bde786e75d5636336081117b389589343ca691123faca5f2254f`  
		Last Modified: Thu, 27 Feb 2025 19:14:52 GMT  
		Size: 93.8 KB (93807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c8063e10107264242e59dfd1cb350e3e95096a094cfe27199a67893bb70073`  
		Last Modified: Thu, 27 Feb 2025 19:14:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
