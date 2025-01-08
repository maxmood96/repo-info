## `openjdk:25-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:180240528f49eda50b4eba4e785c41769508cf033a960896174019c3317a3d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:7d5ab709b667a1789bd4d9f9f42be07f4a3db31b78cf4514403dea41ec612259
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368295818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0fee2ab2af883221710f012f3294f87c53a2a2223e3632b12c5ad1258f2b3b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Dec 2024 04:54:21 GMT
RUN Apply image 10.0.17763.6659
# Mon, 06 Jan 2025 21:08:12 GMT
SHELL [cmd /s /c]
# Mon, 06 Jan 2025 21:08:14 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 06 Jan 2025 21:08:14 GMT
USER ContainerAdministrator
# Mon, 06 Jan 2025 21:08:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Jan 2025 21:08:31 GMT
USER ContainerUser
# Mon, 06 Jan 2025 21:08:31 GMT
ENV JAVA_VERSION=25-ea+4
# Mon, 06 Jan 2025 21:08:43 GMT
COPY dir:bd755498dc37eb6f6d0c16ba16700b0bf6fe6206c66e8b5ad8211bd16b5d8261 in C:\openjdk-25 
# Mon, 06 Jan 2025 21:08:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Jan 2025 21:08:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc1cdf36537340b1875b5d6573a58a268fc20b63dc54a780f9070e51cf9eb9ca`  
		Size: 155.2 MB (155231618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9bf71641221294c3320865177381508ad77c97af6475beffcd81401bc64ce0`  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17a69b32898a9e013cdf928f09a894e232cb509e58044fbe0f756af1c200080`  
		Last Modified: Mon, 06 Jan 2025 21:08:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9378b64f1660bc036436e789db7f0ecdddc0a685bda472e4aa26eea4ff54dcc`  
		Last Modified: Mon, 06 Jan 2025 21:08:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c5746443515af850f96fe4a35565fdb321b7035a843d54f8ad165bd30cb25`  
		Last Modified: Mon, 06 Jan 2025 21:08:53 GMT  
		Size: 67.7 KB (67698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf1fc601adcb3dc3072780558d3ccedd5787cb5b533fb48d67adceb216b17d3`  
		Last Modified: Mon, 06 Jan 2025 21:08:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2c274f74d26dce6c5e79677486cfccbd5d27d91b525bbfe65469a9340b9eb8`  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef227b627dee2095a7b2c5db7f8a519fc5d7dc2b83641ef07d82b9d848d5de98`  
		Last Modified: Mon, 06 Jan 2025 21:09:04 GMT  
		Size: 208.6 MB (208615149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311cf653d3415bc1b2ce854cc0ff39bab4823d3451e577ccf161118b29ff7ac3`  
		Last Modified: Mon, 06 Jan 2025 21:08:53 GMT  
		Size: 4.4 MB (4374977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f08b1f471a2e753746f41ead0b798415346f6f528545ea7ae092905161a90`  
		Last Modified: Mon, 06 Jan 2025 21:08:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
