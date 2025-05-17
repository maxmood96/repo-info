## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:fd0ffea741e8fa3dc79bebce329d45aa5fd7ae3f295e388b0692019ebb0bc387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:dc927bbc6cbe29661fe2892c22969453d2af5d1997cbbe08ab60504154c9fbac
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331682287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cbd628d27984fe41d8646e56b275fcf4f77de677aa881df4d630fd37209960`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Fri, 16 May 2025 21:11:45 GMT
SHELL [cmd /s /c]
# Fri, 16 May 2025 21:11:46 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 16 May 2025 21:11:46 GMT
USER ContainerAdministrator
# Fri, 16 May 2025 21:11:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 16 May 2025 21:11:49 GMT
USER ContainerUser
# Fri, 16 May 2025 21:11:49 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 21:11:57 GMT
COPY dir:be99341787be1c3f0d565e6ac1d9202629ef201376adf519d795dfb5baaa83fe in C:\openjdk-25 
# Fri, 16 May 2025 21:12:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 16 May 2025 21:12:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adbe9ed8706c1c699d1ca44b8411effc72d88e948840b6a1211f4e007cc5b95`  
		Last Modified: Fri, 16 May 2025 21:12:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889bb7ed8caac1ecc5809484a9d82082cd5823575c13429fad97e87488484947`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed751f159ba3c09fffb9cc49e66ce46e2f14b4d9dcfa0d19b12b7d52627fc13`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024cb9d3e7b662f33cf7a51ae4987db0f8b5f2e45188ba289c16ff53ee29a71a`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 76.5 KB (76470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10ccfeb81cbfe8491ed7f40d9d9e019a9e520efe9cfb073d0398f76d7b187d`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dca2042cc5a5f000130e062ccb965ed20a01c0ca8f6a0f6df04f8502b5631a8`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed4226f120febb09227d11b848f25646fb3d1424823804c5970d4d6dcedba93`  
		Last Modified: Sat, 17 May 2025 00:24:03 GMT  
		Size: 208.9 MB (208915406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41366ce39d24109a6f497442bfae6809c344d1d61e77dce5cbb061c389f71666`  
		Last Modified: Fri, 16 May 2025 21:12:45 GMT  
		Size: 107.6 KB (107591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe232b14acad8d95efee54346dbaeffa8976ba7c37b504c0b1f648d6f1972a8a`  
		Last Modified: Fri, 16 May 2025 21:12:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
