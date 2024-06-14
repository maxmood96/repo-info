## `openjdk:23-ea-nanoserver`

```console
$ docker pull openjdk@sha256:66a32287be76157462be38a96b67e3c871b117538648ba47d2bac2399644d67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-ea-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:bf05c64d51368a1d073cf17b720469135bac984b75f2f367b3a5b2ce2cf98259
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365265162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5a6a7d653600f5c8519248ce36bd3f82ceb93a2ff247fe826d3273f3096bc2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Fri, 14 Jun 2024 02:06:45 GMT
SHELL [cmd /s /c]
# Fri, 14 Jun 2024 02:06:46 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 14 Jun 2024 02:06:47 GMT
USER ContainerAdministrator
# Fri, 14 Jun 2024 02:06:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 14 Jun 2024 02:06:50 GMT
USER ContainerUser
# Fri, 14 Jun 2024 02:06:51 GMT
ENV JAVA_VERSION=23-ea+27
# Fri, 14 Jun 2024 02:06:58 GMT
COPY dir:f169e73d7f2a7998f4fb657e3232d5ec1075af5167a302f7459a0edc3b73ab60 in C:\openjdk-23 
# Fri, 14 Jun 2024 02:07:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 14 Jun 2024 02:07:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c45019bc20706be79e5662dc6903a6605ae56b97fc4fc0183afa73ef5d6037`  
		Last Modified: Fri, 14 Jun 2024 02:07:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec8f9e42f10bfba5d730006be258870b597f6a3632fa21dba11a858d9b6171e`  
		Last Modified: Fri, 14 Jun 2024 02:07:09 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f22d37ea194c0885f9e71a1b99998440a929e4aaa8ed23c6ec7094806e875a2`  
		Last Modified: Fri, 14 Jun 2024 02:07:08 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd248a9ba062cc1466bef19469fa6df3ecad32953c76dc60a9bb52bd3a08b5e5`  
		Last Modified: Fri, 14 Jun 2024 02:07:08 GMT  
		Size: 71.2 KB (71221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51d4b28dacddf45b4b2feb66b28038d1f85ca5bbed5e6f0cacc65433e10182`  
		Last Modified: Fri, 14 Jun 2024 02:07:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc657f5086e4058069a81d0e70c8489990c407406dec331c18ef8cf9957f89ca`  
		Last Modified: Fri, 14 Jun 2024 02:07:06 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c9a2cd22003d3fb7a1f12e0ce2f74233c4091f30fdff139c60c60379cc3e18`  
		Last Modified: Fri, 14 Jun 2024 02:07:19 GMT  
		Size: 206.0 MB (206041061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616db608258252b599bb448bea544adf27d80e1e7d65d836659b89ce9ff727dd`  
		Last Modified: Fri, 14 Jun 2024 02:07:07 GMT  
		Size: 4.1 MB (4113238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd8f6cc33ad7e61bc0af64b12b3f2a6ea61104f4998ef062384d8b1ab9836ca`  
		Last Modified: Fri, 14 Jun 2024 02:07:06 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
