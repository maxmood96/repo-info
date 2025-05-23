## `openjdk:25-ea-24-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:c7b32bdabb2a9734fe90f0fb1e2de18aef4765f528618fa2691b6b007465b2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-ea-24-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:de92fc1744a65eeeddaff5dd95309b164c1876ff0c16fa5f4c1b6a8ab3a85c1e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 MB (400942552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7893029e17389ccd0f0012da311b6ab4eb842484f5e47253e4c73b7587e1cd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Fri, 23 May 2025 20:13:11 GMT
SHELL [cmd /s /c]
# Fri, 23 May 2025 20:13:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 23 May 2025 20:13:13 GMT
USER ContainerAdministrator
# Fri, 23 May 2025 20:13:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 23 May 2025 20:13:16 GMT
USER ContainerUser
# Fri, 23 May 2025 20:13:17 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 20:13:24 GMT
COPY dir:d32a1e622c307f990d42f1dfe6052e231c098d4b948c30b3def65fbe5914b454 in C:\openjdk-25 
# Fri, 23 May 2025 20:13:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 May 2025 20:13:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da2e7ca37ec8067c7ec8d6cab286ef187443fbf8625888ec227b4ba5ade1a36`  
		Last Modified: Fri, 23 May 2025 20:13:38 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f058980b6ff436a54f373d5a953732601b094d1a0854191a6e83688219214d79`  
		Last Modified: Fri, 23 May 2025 20:13:38 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53536315e774643720364354ae5d97d41bb1cb77e24755675149a4bb3672215c`  
		Last Modified: Fri, 23 May 2025 20:13:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc06808f8483b763ccbfd31d2583cc388c6af5d8c5579b159aaeae4167c4a57`  
		Last Modified: Fri, 23 May 2025 20:13:37 GMT  
		Size: 76.3 KB (76298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658021efa7f52f0a6ce0061ab2bd2c8d197d3266a56b106e48dacbc1f4b9117e`  
		Last Modified: Fri, 23 May 2025 20:13:36 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41233b75940eacf560efca8c2021a6b4e6d3a4a488185c116c9ab8b87b9a1a3b`  
		Last Modified: Fri, 23 May 2025 20:13:35 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe506b2a635fdfb165b908a45627c01f275d3599944542fd1eed695fcfed5ac`  
		Last Modified: Fri, 23 May 2025 20:13:47 GMT  
		Size: 209.3 MB (209333757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ef3dfe9796548c729b0cd1f6790b55b97ddc5b6c9f2ae15bfd2cf793a09339`  
		Last Modified: Fri, 23 May 2025 20:13:36 GMT  
		Size: 114.2 KB (114170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd4b37ba75fdeb73658e9f3c9e58541d4aa9fa0609f3dad9b38ee1f8afe6daa`  
		Last Modified: Fri, 23 May 2025 20:13:36 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
