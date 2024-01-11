## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fe81bf34ddbd094e7f865776d50561633bcc37b53b155d4ff0c16acef32d9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:e27204c4f9baeb3131dce18954db59b70fba47762138b326d8a02f3d1bf313ac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161052442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d277cd3289b7c00e300a3acc236458d40133e721c412cde41ecff1f75e744a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:17:07 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Wed, 10 Jan 2024 23:17:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jan 2024 23:17:08 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:17:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:17:23 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:18:05 GMT
COPY dir:dbdf2dd9ed9894186d74b75beac1320724c73c6994b00118f04985f0ea2b3067 in C:\openjdk-8 
# Wed, 10 Jan 2024 23:18:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628ad7aa058ffb12fa3ef62904fd96d1ef4b84c45f7b942775a6ae02a830eb7`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b604f3ee0869ea0719f02c17eac778b3b2e716757ac449ba79ea5b654ddcca7`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8240708d47924cf34a43fb95c84a9f970eb54178ae1825f974cb9e894e03f41`  
		Last Modified: Thu, 11 Jan 2024 04:18:55 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650656b3a0668e024e51fca51fc22124e405ce5a0090747a36498c399156a918`  
		Last Modified: Thu, 11 Jan 2024 04:18:55 GMT  
		Size: 94.2 KB (94221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59fc61beb41f45677b64051f9a23fe2b986c84b8e9014b2162ffedae722ed1`  
		Last Modified: Thu, 11 Jan 2024 04:18:54 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dc4886fb8d6c36fb22c2fb3f32e4a9a3838b1cd602c9685913a48159e54895`  
		Last Modified: Thu, 11 Jan 2024 04:19:26 GMT  
		Size: 40.1 MB (40110899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7d7f5f17641e5bc447eedc9abe8ef980a6291898089b25cab5e2d35ee6def0`  
		Last Modified: Thu, 11 Jan 2024 04:19:19 GMT  
		Size: 72.3 KB (72285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:05f414b2bcb421ff75484a05c639c51e9736796bb2d4020a891c43628a6763ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144860066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c722e257f595973e28cc2b1587b4235390d388b6dfb6953851079f6fd4caf75d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 22:41:07 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Wed, 10 Jan 2024 22:41:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jan 2024 22:41:08 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 22:41:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 22:41:19 GMT
USER ContainerUser
# Wed, 10 Jan 2024 22:45:41 GMT
COPY dir:dbdf2dd9ed9894186d74b75beac1320724c73c6994b00118f04985f0ea2b3067 in C:\openjdk-8 
# Wed, 10 Jan 2024 22:45:53 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec88c6fd1d0cd14082069642ccb3b0dd5a7538a4b8b0c2d430549f345d8fd53`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a70ce583d963a632ef35f9621118c53550bfa3e2ede770446582b854c282042`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b458c740d49612fd593af7fbdfabd3958245ad1931a748d10694f35e9a23f5`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f8ab83b9667552a30989b2807670e54d43f9fd8c43e433f52d7bf74ce674f9`  
		Last Modified: Thu, 11 Jan 2024 04:09:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a79de0ed29ea826956427092d73b26807e20d9d636513da4988cf310828211`  
		Last Modified: Thu, 11 Jan 2024 04:09:19 GMT  
		Size: 70.5 KB (70482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24989b19b1c3828ca50012cebdcb8afc9928b3289edc89dc539a013fafd72539`  
		Last Modified: Thu, 11 Jan 2024 04:09:19 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40572e128dd57bf39fa265385fa3b1b9d66533a594f0e1d71b61e05281564c9e`  
		Last Modified: Thu, 11 Jan 2024 04:10:22 GMT  
		Size: 40.1 MB (40110917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549b8538b0c505e60cccf1f895b103464e5efde35c137f40a7315f26d35b554d`  
		Last Modified: Thu, 11 Jan 2024 04:10:16 GMT  
		Size: 81.7 KB (81723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
