## `openjdk:24-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:4be4b9eb56286ee127e2f2af2b79aef97fa7921e65f5e8c474cd550da5fbff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-ea-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:7eefcb0a6d2b7ea1d1c6a6a0e800b034f67ac54d5f3367eb31803997bfe29e2b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407763395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6e775fb32ff3effc10fecd0739bca1c99933ac5a232822531712194ad63a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 23:31:45 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:31:45 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 31 Jan 2025 23:31:46 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:31:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:31:49 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:31:49 GMT
ENV JAVA_VERSION=24-ea+34
# Fri, 31 Jan 2025 23:31:56 GMT
COPY dir:0417d4640b3e9898160c754927e6892a89119d4a6294484281d02c0d6a35e95f in C:\openjdk-24 
# Fri, 31 Jan 2025 23:32:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:32:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1533284ea2cfb38d5f1a798e284206322419ca11840e8403b3bd020b477b889`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19f50bb503a8d32b57fc8982a846c29e7d9c3e0a32f5a4cbaaeb7523aa9494`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8efef181910acf74810f2561b8e91db55f1ddce1d07306721e501f4b1851e7f9`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b26247b8ed4e361a61489ed13b5857fcea91f87ddee53f5b0904a0c5d54bd7`  
		Last Modified: Fri, 31 Jan 2025 23:32:07 GMT  
		Size: 75.8 KB (75828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a56ba5193300ad96e37ec759681bf710597919f2fa7d8b155589b52b80c667c`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5949c97eb7b095f3ef8c6519e2c86aff72060a053c2bb0f949fc6e1508df787d`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d04dbc1086d65bd9a5986f45c05977482b603c1b64a3b4a8a1dfd3c8db83d4`  
		Last Modified: Fri, 31 Jan 2025 23:32:17 GMT  
		Size: 208.5 MB (208534184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7219f4f081190d565794a456555fa9277e77f4af8341bd5720567fdf7a151bdc`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 92.7 KB (92738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1231ac63740ff9464af912aba0861c68827b7d04895aeb382a0af4eb3eb6407`  
		Last Modified: Fri, 31 Jan 2025 23:32:06 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
