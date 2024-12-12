## `openjdk:25-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7e4dc6438811817d091f1fcd15cef9325a99470d96f3ec0b0265d3dc67a61f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-nanoserver-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:207025adf9b338e46e679098cd9a2b1c4d4677590a6b114c1fb4619848ca7ce8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368252200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423a7be60a8dd3404d8a32621414735c4c320a68403d11b82c2aea10a3ec4e75`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Wed, 11 Dec 2024 21:47:25 GMT
SHELL [cmd /s /c]
# Wed, 11 Dec 2024 21:47:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 11 Dec 2024 21:47:27 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:47:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Dec 2024 21:47:31 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:47:32 GMT
ENV JAVA_VERSION=25-ea+1
# Wed, 11 Dec 2024 21:47:38 GMT
COPY dir:2e6cdc7f1b1fe8d940d6b4a43862b3e1f54bcd94c04e6589c6d482f98b5321b1 in C:\openjdk-25 
# Wed, 11 Dec 2024 21:47:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Dec 2024 21:47:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dc9d84ffc07d82acb00ab2637a6fffc10925ca72afe7e427489e228fb52b74`  
		Last Modified: Wed, 11 Dec 2024 21:47:52 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b07ded41c73fd9a09f308aaf5ddf2a4b65591c8c3f8d6e10a48dfc21a5ea20`  
		Last Modified: Wed, 11 Dec 2024 21:47:48 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a010935a2705941da67dcb56dc278413df06a907c48014afa9feb8a0abd7cdb`  
		Last Modified: Wed, 11 Dec 2024 21:47:48 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f1923bc76db6f4ae8b82f0c9751604ecb3f670ccf40e9fbb2552a0fe81c6bb`  
		Last Modified: Wed, 11 Dec 2024 21:47:48 GMT  
		Size: 71.6 KB (71573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc4e24b4111368d8818c05f27da560a93460411d0274e24d456141e084123fa`  
		Last Modified: Wed, 11 Dec 2024 21:47:47 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed1ef09307ec3cced13082b188288916be9c6db4c782494fbf940133384a85b`  
		Last Modified: Wed, 11 Dec 2024 21:47:47 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2889c127879e229c9aab49177c255b6e67aafcd4a2306328c8c39017c3494144`  
		Last Modified: Wed, 11 Dec 2024 21:47:58 GMT  
		Size: 208.5 MB (208548917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306d3c8ea1e5af442524b25ec3b88d86aff7492f32d283c8e719195a293e0938`  
		Last Modified: Wed, 11 Dec 2024 21:47:47 GMT  
		Size: 4.4 MB (4393667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450609a6e574ddfb96db658b2ebc68ebba43bb22bd01e35920e3c692691a763d`  
		Last Modified: Wed, 11 Dec 2024 21:47:47 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
