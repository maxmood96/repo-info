## `eclipse-temurin:20-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:7ef29c46bc498d3f940f5ba0ff1130354fbf1ed6b833652f1d5e741f32247e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:20-nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:1e9340b621e9194037dd2de47744411c4aca442785accf376fc374cc5f435edb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303526841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1ef83f13cbe8992febafc25133208d7a4aedb1a1bf5064ac31a48ac9126989`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:05:42 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 13 Jul 2023 22:05:43 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 13 Jul 2023 22:05:43 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:05:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:05:54 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:06:07 GMT
COPY dir:f42e28541c92f419d16f8f9260ba58e12cc63ca253028a61fc42e8a28f91cd69 in C:\openjdk-20 
# Thu, 13 Jul 2023 22:06:20 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Jul 2023 22:06:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d62bdbae50ea5107e96f223e58acf04a48c5a1026befc163b868fc431635844`  
		Last Modified: Thu, 13 Jul 2023 22:27:04 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f721c84b9ba4db8a041679302c91e162147f18ca3473fe31aaf1ce195f2b561`  
		Last Modified: Thu, 13 Jul 2023 22:27:04 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a39db0679078c0ab19cb1d43aaba827ba9fc60421bd4da8150877c63745c0f9`  
		Last Modified: Thu, 13 Jul 2023 22:27:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09baeab2e9e0f9a703df99df66f102274cbd935494f12b4b140f5bffa5006215`  
		Last Modified: Thu, 13 Jul 2023 22:27:02 GMT  
		Size: 68.4 KB (68376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5aaebecb942512ab4f0d9f67a6dfe5688eed16185b0f9c8cc40d28f4514ab81`  
		Last Modified: Thu, 13 Jul 2023 22:27:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff74a9137f35ba2f811110f35513fe10eeef874b121e3c362e43bd767deb9c3`  
		Last Modified: Thu, 13 Jul 2023 22:27:22 GMT  
		Size: 195.3 MB (195275242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da448f8da4076d71be29f02026071bccbcc4fea87705b7599c8726c31a6b41b`  
		Last Modified: Thu, 13 Jul 2023 22:27:04 GMT  
		Size: 3.8 MB (3768065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ce93d6b5e6946e2750c44bb78f69244ebba1a3e6d102d8b30f0c08ba45a75`  
		Last Modified: Thu, 13 Jul 2023 22:27:02 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
