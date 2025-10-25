## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:65545d2dc7d89047aa1a7323d3c89e3cbe5d553738b0552ac3b12ddac44e1cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

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
