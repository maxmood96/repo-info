## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4b9d1d096bc2ab202706ee237bbdcab6a6ee1bb16d859a8a4cf9f8b0377a208b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:8f807e98aa19ee85b04e98cff5d7c179cc05131e7dc18a5390c4921395522082
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309471353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae94031f1497b5e4d9b003ac9f6f0ffdddaa566df843d7cdbfac1c390a90f900`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:10:51 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Wed, 10 Jan 2024 23:10:51 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jan 2024 23:10:52 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:11:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:11:01 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:11:16 GMT
COPY dir:fd62014fea6b5cd8b6f3d34ff8f9c5e95aa0ce969b7fd9201e979e77a3abe050 in C:\openjdk-21 
# Wed, 10 Jan 2024 23:11:28 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jan 2024 23:11:29 GMT
CMD ["jshell"]
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
	-	`sha256:f947371f94db731a429f4924c1019dfb90d38824515c071ae72e2702280e1346`  
		Last Modified: Thu, 11 Jan 2024 04:17:24 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d892e630c4c0f35f6788ffb8a704125d58c321345db1b7c8791c9ebed5059732`  
		Last Modified: Thu, 11 Jan 2024 04:17:25 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b04b0717e07a5207a948e72f23afeb6ff8181055323dccf5d42cc5384b003`  
		Last Modified: Thu, 11 Jan 2024 04:17:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90639508c1f7fda55369ef3c64d705b2b78a1e6432b3388792c64439b2e7ace1`  
		Last Modified: Thu, 11 Jan 2024 04:17:22 GMT  
		Size: 68.1 KB (68146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684573824819ca2de63a1a5e404e5a3f1aeb486e8a4388ef7963668da307a88`  
		Last Modified: Thu, 11 Jan 2024 04:17:23 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e73b685919a18a44548db10085b2f8763b2db2d03c4fce6a1050bcca600947`  
		Last Modified: Thu, 11 Jan 2024 04:17:42 GMT  
		Size: 201.0 MB (200994327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e153c6a71063e7d19b21f1e32a8b9764b0b211fcd3881cd7545da03e0d5ff71c`  
		Last Modified: Thu, 11 Jan 2024 04:17:24 GMT  
		Size: 3.8 MB (3811200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2fcb9388aa3e9960cac830c73940e1395fb1185d667aaac856e504d949a5d6`  
		Last Modified: Thu, 11 Jan 2024 04:17:22 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
