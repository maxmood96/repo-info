## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1750f57fdfd43fde4d62d455455bf77977687df8328cee3e859089cf1f0e87df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:aa0ecc64d163c2e096febfc8d62efc759ea54475c8b26bba6e33929ccffdf87d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323428991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d433eb0603906cb500451182f7f121e90d4b4ddded570d78f72ee9f7dd738f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:03:50 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:03:51 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 18:03:52 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 18:03:52 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:03:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:03:55 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:04:02 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Wed, 15 Jan 2025 18:04:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 18:04:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396c99d0aa317706c66b94d5c540590d514e7126261ee9233696fa2701de3b4`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0f7dd8e71d0459702acc384f502eba5d97fa4496f654c1031f0f87030bb77a`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e040b932910a377ac9f8a2cfce3996da68478d51303296fc1cd26890b9596f80`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22e89e8a4b0e085a36a131f5b1999728304fdb5af41628e8097c5f6b64e42ee`  
		Last Modified: Wed, 15 Jan 2025 18:04:11 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d406ee34f8101211f624c423ec04c27359e3dbbf40ade69629caa9ad83421c`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 78.7 KB (78669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f33156a3c636330d331451bf7b731cdc029043be60d540250ddcf3f04cce96`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49916c855bda31956cf602ffb7df7833af32a1b1c5c03181073c5f2e7392b332`  
		Last Modified: Wed, 15 Jan 2025 18:04:21 GMT  
		Size: 202.6 MB (202575611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9890f46b2da0e27b50366f145b05cc82fe92266a47118fbac472df33271bae40`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 107.0 KB (106971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631b9a9d46a269eee51df0bfdd9909d254f21b503d04358a8dca7dcf91892e37`  
		Last Modified: Wed, 15 Jan 2025 18:04:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
