## `openjdk:15-nanoserver`

```console
$ docker pull openjdk@sha256:6088eaf30893e1406e44fb94e0be06e0833786fc0da2894ef9307d6ebca2a6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:15-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:bc45027d9b182a7a064a807da7cbe0b10166c9f895ea0a636aa4aafcb4400cb0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296325708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8af941572862882b6ec5aa7e4fb79ab3e3596b9b3d43e0f8a2c8c5b1a820e62`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 20:42:55 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 13 Jan 2021 20:42:56 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 20:43:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 20:43:07 GMT
USER ContainerUser
# Wed, 13 Jan 2021 20:43:08 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 13 Jan 2021 20:43:45 GMT
COPY dir:06640d856df66e65007611590cb3dd79cbf5545f6270e47800d01f33c3a3417d in C:\openjdk-15 
# Wed, 13 Jan 2021 20:44:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 13 Jan 2021 20:44:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b06e2760220b592d7223a535812762ce910e4e06c4b5c9d7a063dd227e80c4`  
		Last Modified: Wed, 13 Jan 2021 21:25:46 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05331d9e36f3b34b20230294798b851d181ef624007e98b2de364f49d828b12`  
		Last Modified: Wed, 13 Jan 2021 21:25:45 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2217464be837992891e2442451031cb999e6c2acee7eddc7bf59195c91acfd67`  
		Last Modified: Wed, 13 Jan 2021 21:25:44 GMT  
		Size: 66.5 KB (66517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec13ba6c204194c9ae26b5c4a1261c1de60235cb039258267fa4cc80c8ee84a`  
		Last Modified: Wed, 13 Jan 2021 21:25:41 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cccea86e4e88d0c9b7f17c95a6c6df62469703607276391cfa3137fd1aa989`  
		Last Modified: Wed, 13 Jan 2021 21:25:43 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cd9b46c49cb161f41794f5b8471f5f3aec952bffaa72a06a262f389522a11a`  
		Last Modified: Wed, 13 Jan 2021 21:26:04 GMT  
		Size: 191.4 MB (191390300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0926369f6360acf342fa170553426d4d660fbb1c1433c68261182f47cd8b0d`  
		Last Modified: Wed, 13 Jan 2021 21:25:43 GMT  
		Size: 3.5 MB (3523509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1627e8092f86752f53db80024405709ba8b1c4a44688a73f2b1b08df6a41945e`  
		Last Modified: Wed, 13 Jan 2021 21:25:40 GMT  
		Size: 875.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
