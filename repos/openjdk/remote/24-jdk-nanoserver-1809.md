## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:cb39df82fcdb9d150f9fc91c5008da7a8dcbf794f3bb2ba1830325e0b5109621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:63c784d1c9cceefc7bbdd2d4839e01162ba0e84c26c5b399c486830166ecade3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368244466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e270a5da9a491497a4ee5269ffde61d98ad8918f6a78f573f8b347a2913b9288`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Tue, 11 Feb 2025 02:08:32 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 02:08:34 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 02:08:35 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 02:08:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 02:08:54 GMT
USER ContainerUser
# Tue, 11 Feb 2025 02:08:55 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 02:09:10 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Tue, 11 Feb 2025 02:09:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 02:09:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48998653beafd11420a55fc0354d945e0c558381d8516b68032d995bb16ef644`  
		Last Modified: Tue, 11 Feb 2025 02:09:21 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd6fd09e15e797aa235dc19f6f408d3cd2325905e7743fd538c66b87e3d13a`  
		Last Modified: Tue, 11 Feb 2025 02:09:20 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49121cbe4ebb8f43191f829e05c4a52b994641d2053ed0bd6ad5c01e6daf8491`  
		Last Modified: Tue, 11 Feb 2025 02:09:20 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4dabc869167399a65490e0004e0b2bdd93ec9f8993e791caf68276905906d5`  
		Last Modified: Tue, 11 Feb 2025 02:09:20 GMT  
		Size: 67.5 KB (67454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f673638d6fff94a86f19c9334b7dd3816cf81bc5785c62d4cf512121ef5826e`  
		Last Modified: Tue, 11 Feb 2025 02:09:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3922e157442242e5683bb927c813e9ce65d21c20c687847f6c81e57d719f7c3e`  
		Last Modified: Tue, 11 Feb 2025 02:09:19 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b426371be59ade1110a0ee5d6704592c5414334309a02905958852245ec47bfc`  
		Last Modified: Tue, 11 Feb 2025 02:09:32 GMT  
		Size: 208.5 MB (208527384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb999fac7b86565850559cdcbca24d6bd5c34827d7d40eb1aa2024236eec8975`  
		Last Modified: Tue, 11 Feb 2025 02:09:20 GMT  
		Size: 4.4 MB (4375775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090584256921484d56cdd2abe00cbb9bb7bce131cb975b0796a769f2b85e13fe`  
		Last Modified: Tue, 11 Feb 2025 02:09:19 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
