## `openjdk:25-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:f6b516ae8f4afcc269af0d76cc7df75822abb8a3484a8eb836ac45d0d47b647c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:b3c5a529289e1521ff10faa8147cf2c920d7613c4b96f20c13c591f1bf973054
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 MB (397924933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6371399bead54ce7ffeac9995775b6dad7b2207b45b431cf54ee0327d7ee120`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:50 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 04:14:53 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 04:14:57 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:59 GMT
ENV JAVA_VERSION=25-ea+18
# Fri, 18 Apr 2025 04:15:06 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Fri, 18 Apr 2025 04:15:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 04:15:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af37f8ec4ce4332917e40bd09ce21423c309e44af78f581aab39617a99f28d4`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb22ef40406d0c0f5f3d054550d9479aede7a89791285369897a587dc091892`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b53bfc286c6381f55eaec0263fbb79ae7f0e2a943f810904755de466dd1c2b1`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bed770423a284d4616929e06e8c18504476d7d560630d489ca2e764c8b7bf15`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 76.4 KB (76352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbb188c4e58ee41f4b07bcd599a547d6b265892fc1cd9b88929484dcee03d5`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce946e80764c13f027343f994c15dc99a9f428b86aa8d90ae0ccd520ed29614a`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feed1123be70f61eacd9a02360d8928ef497253ba59c69a27908a8eb62988248`  
		Last Modified: Fri, 18 Apr 2025 04:15:30 GMT  
		Size: 207.6 MB (207583705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3b21258869107c64db35c9d1c7881a74a1cf9a95c1ef975f2d2aa8f8cdbd85`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 116.5 KB (116463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0265cb58d1c222e06fcceafb74de3a959a8d3a0401dcd273c69a81c6b0513e6`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
