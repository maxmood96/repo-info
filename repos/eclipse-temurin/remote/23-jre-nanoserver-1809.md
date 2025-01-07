## `eclipse-temurin:23-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d142167463bee06f0a1a81767eead4852b5ed981326ca30dba76a230e4b06f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:23-jre-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:a6e084f192ff5c47ae1c4a3b328474621fa13002f002e09256d8d48923977d15
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208549165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43aa7ab158acb59b9b10281c42468928430d106ab4aeddfe07ea261f1ffb0d3b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:47:22 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:47:24 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 11 Dec 2024 21:47:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 11 Dec 2024 21:47:25 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:47:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Dec 2024 21:47:28 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:47:31 GMT
COPY dir:d9adc234ed2c06cd6b72c0beb8933c6d824941dbd1cece41e4fd2578b0632fbd in C:\openjdk-23 
# Wed, 11 Dec 2024 21:47:35 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b948df5f30a2e028f90b0c5faf8bbe2d5570718294d940ea55611b1b3702be8a`  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b4189483c1d6eb664b7f3d8bdc302642d172f2d1a6ebd214699c51d43ecc1b`  
		Last Modified: Wed, 11 Dec 2024 21:47:39 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09128048c2297c5ff63aa8bbd68391a3745389ee902b22725134f4603c706010`  
		Last Modified: Wed, 11 Dec 2024 21:47:38 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68416578ece746f41aed130d4b195e6b3b8c7125d856d9548a4fda5a4188cd7a`  
		Last Modified: Wed, 11 Dec 2024 21:47:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6a800dacddf9a6c06b480a87330c94b19bc0095e598d711e2b323f1b78c22c`  
		Last Modified: Wed, 11 Dec 2024 21:47:37 GMT  
		Size: 83.9 KB (83855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb54dbceb8d314b26993bdee55cdb336c2c8963470e099c4806cbe6b6832111a`  
		Last Modified: Wed, 11 Dec 2024 21:47:37 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae07ac44a1dc02463f5b13e6b9b1d54b029ad22a5ac1cd1fa200bfc4febf571a`  
		Last Modified: Wed, 11 Dec 2024 21:47:43 GMT  
		Size: 49.6 MB (49609900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48855304b0f9a66ec4b26169118f5405820021486ad0577c906ab425376b17fb`  
		Last Modified: Wed, 11 Dec 2024 21:47:38 GMT  
		Size: 3.6 MB (3618561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
