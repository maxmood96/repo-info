## `openjdk:26-ea-23-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:34413dc15cd237192b9fdcf04299d58d40bb4aceb7e3dad60181684abeaaed42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `openjdk:26-ea-23-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:2b87a4a9b0740511ff4ab06b819e1ab06e0970bd6f9f840eff3860a60e2de311
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.4 MB (419445249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ebeec2fec1a4ed9d2cd66d73980443734f056e328400789c7604d7beaab2f9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 11 Nov 2025 20:11:08 GMT
SHELL [cmd /s /c]
# Tue, 11 Nov 2025 20:14:59 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 11 Nov 2025 20:14:59 GMT
USER ContainerAdministrator
# Tue, 11 Nov 2025 20:15:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Nov 2025 20:15:01 GMT
USER ContainerUser
# Tue, 11 Nov 2025 20:15:02 GMT
ENV JAVA_VERSION=26-ea+23
# Tue, 11 Nov 2025 20:15:16 GMT
COPY dir:caac7c3daf5c418f731b855ae37dd48a49eef4e9ccf593b019be40c369c65420 in C:\openjdk-26 
# Tue, 11 Nov 2025 20:15:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Nov 2025 20:15:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6194cd77702c569004d9457e0c06be0662b8256bcd8f00c1d770f01827ff09e`  
		Last Modified: Tue, 11 Nov 2025 20:12:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1257b25cf52c5ede2032b927bc5f1342c450c20be32bbbc4d6aefe8357bc514`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45440e2d56525b8b61f06079e41237c5d32db826dc6a5b6ec80ffd49e669ff3`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca352de405283e15ac0a8e2b4f56ce7ab10396e432d99adfb942705c8d4756b`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 72.0 KB (71961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e64c7b80e1865bd7b4331e807018e3fef5c04ad5c3454011782881336a03e1`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b858af93df5546ff052de0b25fdeba592d6bca73f7d39db7806f5422fb6010`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044bf286e691844ac398f4a9b2d0b5d56447b20e230d63c32acf1c89ba8ad296`  
		Last Modified: Tue, 11 Nov 2025 22:23:52 GMT  
		Size: 221.3 MB (221318054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1f597aa25978e3b820691a4cdb262e4db4b17f890f72a75047037e4d1eedbe`  
		Last Modified: Tue, 11 Nov 2025 20:15:51 GMT  
		Size: 112.4 KB (112396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837124e314b72377ab5ceb7f9b21a5258292afca60fd0b35244d945eeb6753df`  
		Last Modified: Tue, 11 Nov 2025 20:15:53 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
