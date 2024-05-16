## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e3d548efda31ab287d92f669773b1a0b3295c1a4d4f57ce0abcdd2a5cbd21892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull eclipse-temurin@sha256:df226fcbc9f329a3521380843644bc6e55856832955e1033ddd16ee0077f14ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345449278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89311e6c8b48a6825ba432279a2d16a3b1726d05c0d96a511ce8d07080be906`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 19:42:01 GMT
SHELL [cmd /s /c]
# Wed, 15 May 2024 20:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 15 May 2024 20:04:35 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 May 2024 20:04:35 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 20:04:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 May 2024 20:04:45 GMT
USER ContainerUser
# Wed, 15 May 2024 20:04:59 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Wed, 15 May 2024 20:05:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 May 2024 20:05:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6a511fea8e874efc08e5058ac5b12b6433c36ba6570862a619dd80cfb0e190`  
		Last Modified: Wed, 15 May 2024 20:45:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da49c4b8012eb26cf69c376d99dd8f1cb1e3ca715beb7254db10e9807c4fc9f`  
		Last Modified: Wed, 15 May 2024 20:51:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80045ad85cfa6eab06f555a848b724489fc2aafccc21d8dc6ac3b9201980ff7c`  
		Last Modified: Wed, 15 May 2024 20:51:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d438955ec9000bd485218afe17f2d42614a0ce5ef330651ce4c2940273c187`  
		Last Modified: Wed, 15 May 2024 20:51:09 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c63495db38074e2cb31d8afcccbf3f3588fd25c298c3f82cfce36b2deaf2b39`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 68.9 KB (68939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49bc8a43e83602c3561ce59837b5348440e9d183f9f759da75dcee6267db095`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5738a714e59c4b1f12ea75f9464ba04edc60ffd95bda3b05f2eee986e1adc55a`  
		Last Modified: Wed, 15 May 2024 20:51:26 GMT  
		Size: 186.8 MB (186828072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f38da31e90682cc2a1244b437f26ec0258a2bd4b2d2e8aa66673f7a39d1baad`  
		Last Modified: Wed, 15 May 2024 20:51:08 GMT  
		Size: 3.6 MB (3603919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cb9a00375cf2fa691459cb646837cf9806aad37551772a6067afcb59c220a7`  
		Last Modified: Wed, 15 May 2024 20:51:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
