## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:9b9c61b68e57cab6a713c016b052620d32cbe6590af166a028c74b103c8bed28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:04aed2599f401ce668e22d440b6f117b70752c6cc569d32293dfa39525e11ae0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330311687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb71343c4a79c914a36696213d3ed541c628fbbc7ecfbbad08b324f1f430dd0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:20:48 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:20:48 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 04:20:49 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 04:20:52 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:53 GMT
ENV JAVA_VERSION=25-ea+18
# Fri, 18 Apr 2025 04:21:00 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Fri, 18 Apr 2025 04:21:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 04:21:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971116681bc5a412624e3675fed90ba346c532e8f8ecf0a3499e75f70e906750`  
		Last Modified: Fri, 18 Apr 2025 04:21:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2173b849b2cc48e171f6dd62c52fee1d459354f513868476e9fd9b607fc020`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356828e71f6c7a6fed76e22b4eea3c78f889237e2ddb8b09bb8b410da8b4744c`  
		Last Modified: Fri, 18 Apr 2025 04:21:10 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520235c58ac1751f677a943e6e6f9d1d4030b5158fdd05c57a130927b7b52dd`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 78.6 KB (78574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f3761ed34dd20da76c57dabd27cbead6161e2c5b13b0f6a823c632aa096b2f`  
		Last Modified: Fri, 18 Apr 2025 04:21:08 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd8b5a63e6faecc493b33219bec94fd4b909a448a294874dd90ac58911d02e4`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf56b06ae546ad25f292d8835a191b64a18de2a110eb64349dc50f0da9cc7330`  
		Last Modified: Fri, 18 Apr 2025 04:21:20 GMT  
		Size: 207.6 MB (207580721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6dbfa0b5d96247cfa4ac77f3b097a214aba6a67c9b61f0dae4a3d929d52d55`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 107.1 KB (107106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5391cc228baae84dda5bbbe553c4b329505c9d8c9652604689032700074b8`  
		Last Modified: Fri, 18 Apr 2025 04:21:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
