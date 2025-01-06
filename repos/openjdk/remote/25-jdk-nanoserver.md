## `openjdk:25-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:5f6f08fd597cd27057853e922bc8f4289487b612755cc326864ffcf4cadc95b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-jdk-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:ea8016fae82c424309f261a7b09b8ec2a2a26f9bb3b5eecd0b4fcef2a1e0ad78
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368262868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4085c6837aa0e902ea6f73f3d4bb3c436b57909b07bb34bb8416a19677011a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Sat, 14 Dec 2024 01:29:41 GMT
SHELL [cmd /s /c]
# Sat, 14 Dec 2024 01:29:43 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 14 Dec 2024 01:29:43 GMT
USER ContainerAdministrator
# Sat, 14 Dec 2024 01:29:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 14 Dec 2024 01:29:58 GMT
USER ContainerUser
# Sat, 14 Dec 2024 01:29:59 GMT
ENV JAVA_VERSION=25-ea+2
# Sat, 14 Dec 2024 01:30:09 GMT
COPY dir:611475bc46520ce853688d3b0fc5c2a1cde1b2fcd6618534d36169eaa0a331e8 in C:\openjdk-25 
# Sat, 14 Dec 2024 01:30:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 14 Dec 2024 01:30:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Last Modified: Tue, 10 Dec 2024 21:03:34 GMT  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ad4317688d178ca819600551eb2f526857aab7fb0941d7e27fad59f413aa59`  
		Last Modified: Sat, 14 Dec 2024 01:30:20 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563af09e1fc333a71178640611d5be65c525d31e57ca7fc315f6769ca6292cf0`  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bbf047bd95b7acc359e0aeddfd6bfce21001fb2ea6fa2d474973fefbd2f8b8`  
		Last Modified: Sat, 14 Dec 2024 01:30:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb1ec996a2ad6cb768340d1bdfecc69c99cbb85f765a02e71fcab2d012e2ae`  
		Last Modified: Sat, 14 Dec 2024 01:30:19 GMT  
		Size: 67.8 KB (67785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcf42859ad203f31b9e44daf9ed0dd0634ffeea9825d9f4b4ac5df6609d9d22`  
		Last Modified: Sat, 14 Dec 2024 01:30:19 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9b0707032626d911a3247189117d7a6aa850c2d16f545cd6d85538b947fb76`  
		Last Modified: Sat, 14 Dec 2024 01:30:19 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4e27b2d6fba7e9facd5705efe33e4073bcbaaf88bc8d18add372fcb7af45cd`  
		Last Modified: Sat, 14 Dec 2024 01:30:30 GMT  
		Size: 208.6 MB (208572759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03be6ad971be0f1ec59b38ef20b864510de98b598824408e6f4c21c6d9c76146`  
		Last Modified: Sat, 14 Dec 2024 01:30:19 GMT  
		Size: 4.4 MB (4384432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96773cd080f0f4e5d3841eb8c459f99ed0307f18033a39ccec6b96d2eafcfea`  
		Last Modified: Sat, 14 Dec 2024 01:30:19 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
