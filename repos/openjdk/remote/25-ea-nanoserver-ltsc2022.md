## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:a6c733f15b41d18213c9d3c07a7bc66882f282d1355dcb4d9876c17fd8406a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:cc2194d087e8d45cac684d470abc1c135b2af56fe43bf45eadde33c5fa5a82ad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330392505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dabdc2b508c77be52c2f9a0cb62982d88471cfbc9145e2f194bb96111df1171`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 19:15:39 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 19:15:40 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 19:15:40 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 19:15:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 19:15:43 GMT
USER ContainerUser
# Fri, 18 Apr 2025 19:15:44 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 19:15:49 GMT
COPY dir:595a9046aeb360afc9a03339cfcb9f80b8fb3559c4a1bfb194a0956d7f6a1899 in C:\openjdk-25 
# Fri, 18 Apr 2025 19:15:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 19:15:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cdbef5435a340fb1d050ba5b0a3356c1518f343469934feac1c9d02da59771b`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff61de1813c64920e820ae5460a370233054b727d5802a26fb9929e79305a838`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebf1dfca46f7e4517f42c261921bda04589effb49a65542ff0e77cd97940607`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc7cc45c0126996a3e9b8d1d4f603b15ba3601142d12746bea8e9418f9127c9`  
		Last Modified: Fri, 18 Apr 2025 19:16:01 GMT  
		Size: 76.5 KB (76488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3971570ac6d76a804f3248153fff257a562a6508c4fdb499d64a299366620`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a399bee3edf4573bd6efef28192266f5e235d365cea713ae9d7f0f8ae99d33`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214611d07602322b9b16c90671e9704ec48532a8230429c9a54a29e1d9e17ea5`  
		Last Modified: Fri, 18 Apr 2025 19:16:11 GMT  
		Size: 207.7 MB (207663846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e2ef10acc6d0e0c27450cefc183234f4a3c37418d490ce371cabcf598cc9ee`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 106.8 KB (106826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67aae121f2ba10f6cc9250a0e29081984c92462433fb455b9e90ce7d59298e`  
		Last Modified: Fri, 18 Apr 2025 19:15:59 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
