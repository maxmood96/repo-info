## `openjdk:23-nanoserver`

```console
$ docker pull openjdk@sha256:3e18c7b864a34b8170b10f797c737737743d8376afaeac89f9f5b07623a0ed8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `openjdk:23-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull openjdk@sha256:c9b2ad595b9852ae77e1515fae03cec6cf3f1b7f90723808db145f1db51458a1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313175912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fe887a18d2c7079d1604e78898c176733c2a3a26cffd060544c9f4776df56e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Fri, 10 May 2024 01:49:43 GMT
SHELL [cmd /s /c]
# Fri, 10 May 2024 01:49:44 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 10 May 2024 01:49:44 GMT
USER ContainerAdministrator
# Fri, 10 May 2024 01:49:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 10 May 2024 01:49:55 GMT
USER ContainerUser
# Fri, 10 May 2024 01:49:56 GMT
ENV JAVA_VERSION=23-ea+22
# Fri, 10 May 2024 01:50:04 GMT
COPY dir:7b3c1c136106da79beeeffd37c21e2a06ca76287054566b14288aed4c2dc0808 in C:\openjdk-23 
# Fri, 10 May 2024 01:50:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 10 May 2024 01:50:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3e0a192d6fd479933caa81190184671bf1f66c7cca352e4376c28ead81a0b`  
		Last Modified: Fri, 10 May 2024 01:50:18 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f712ddb60f21dca29b806a2e1d72ccf815dd327ddd8c4e414a53c35afbf1ebb`  
		Last Modified: Fri, 10 May 2024 01:50:18 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09aeac54484cd2ee900ce464f112b89c5bd305da315212ec658e7b4992dd633`  
		Last Modified: Fri, 10 May 2024 01:50:17 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d4adc5a6908b1da41c5b766d8535d28505f15aa54cc06fea331dbee4326e7c`  
		Last Modified: Fri, 10 May 2024 01:50:17 GMT  
		Size: 65.9 KB (65897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9c04624440c6bbddd024ebe59f12c2b81e58f6d3db8a83b86b78b0056347c7`  
		Last Modified: Fri, 10 May 2024 01:50:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42611f8e46a5bbeb0b1ee8105ea9bd536ac197807ab36cc39d7af0cfdb8e0bcb`  
		Last Modified: Fri, 10 May 2024 01:50:15 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b350f0894052f21d5325abc563d88b8da55e7dd9e410b55529b25b7606e7f51d`  
		Last Modified: Fri, 10 May 2024 01:50:26 GMT  
		Size: 204.4 MB (204408811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725537292eeaf66394a3a0747d076bb3413124bfeeb82acdbd6616a327349157`  
		Last Modified: Fri, 10 May 2024 01:50:16 GMT  
		Size: 3.8 MB (3805894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4d1dc8949b71bf8f4dff21df7af91fe070a0f9da186c511cb98d19d6283c26`  
		Last Modified: Fri, 10 May 2024 01:50:15 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
