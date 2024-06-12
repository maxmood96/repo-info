## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ffef74cc354cd85bdf873849b26fe772f97247b17a384c41cc952c322e1b0424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:4a9eba0b99feca20972aeda410248c5790320e97f5b62bbdb1e9de6e6e9b0ea4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349255212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3d37b6caf4369e6e0f0053a40a73275046aefc512b0217a68c7cc22844d9e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 17:51:03 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 12 Jun 2024 17:51:04 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Jun 2024 17:51:04 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 17:51:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 17:51:13 GMT
USER ContainerUser
# Wed, 12 Jun 2024 17:51:28 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 12 Jun 2024 17:51:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 17:51:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77f119d6104e3c8342435b5ecf20e3d87fd794b0b9d432c754d791dda070c15`  
		Last Modified: Wed, 12 Jun 2024 18:43:26 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb3afe9e4bf592bc5953d90b42d691e67c1bd6e2e85f763440a46e9af8a279`  
		Last Modified: Wed, 12 Jun 2024 18:43:26 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06259e7480cb7dc7229ee508752a310efbcc003e7cce59426c878fe97b66322`  
		Last Modified: Wed, 12 Jun 2024 18:43:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8b43aaa845da9fc8d7216df2a9485bc92264455f05123c47b9c198f5359e67`  
		Last Modified: Wed, 12 Jun 2024 18:43:23 GMT  
		Size: 71.6 KB (71646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d564193114d887c543c571d7eccefb26d886f1092038aaac0050df32e66ad2ff`  
		Last Modified: Wed, 12 Jun 2024 18:43:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a0ef37d7f1b173e65444b9fa2ff4266efebca26c93d7d8fb78a378418f9f39`  
		Last Modified: Wed, 12 Jun 2024 18:43:41 GMT  
		Size: 194.1 MB (194084597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7fce39f8d007e5cf4fdbae852fd0136a0d5406c7824fc4d3badf9275a078b0`  
		Last Modified: Wed, 12 Jun 2024 18:43:23 GMT  
		Size: 58.8 KB (58760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e389ba1178e24086751d64b9e3bd4b17dd96d66252bc240b1a8e06fd325893`  
		Last Modified: Wed, 12 Jun 2024 18:43:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
