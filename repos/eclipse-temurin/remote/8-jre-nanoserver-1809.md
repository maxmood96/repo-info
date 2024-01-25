## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:258701469ee7b36791076bc158a1b96e993e58cdc977b19584861b4ad8d442bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:5f2370ac79146b29388926440fc76703b57a19f55286e5aab316745731bb6f60
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144864382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfef19bb8843243017468fa957d7362a37ea652927b95a938b81261e59a086d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:19:51 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 24 Jan 2024 21:19:52 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Jan 2024 21:19:52 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:20:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:20:11 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:24:41 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 24 Jan 2024 21:24:51 GMT
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
	-	`sha256:903bc5f9b43cb057943f9039188b4649c9d793100527ab3baecd1ab7392e8ddb`  
		Last Modified: Wed, 24 Jan 2024 22:02:03 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd811e96e6a429ac10c64b48f4456224dea65509d2dade4123a68cf9bd68eda`  
		Last Modified: Wed, 24 Jan 2024 22:02:03 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9d1fd70089e92424c993da2b4648d7cb837c6d796b6c0e106fed58679b89c9`  
		Last Modified: Wed, 24 Jan 2024 22:02:01 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8c01d27c73d63005431f8cfe1289242313497076ebda8bc0bf6913b06f180c`  
		Last Modified: Wed, 24 Jan 2024 22:02:01 GMT  
		Size: 67.2 KB (67153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0871f39eccd4268560a92561806bcc18b963dc148b831fc86179cf5c14025ce`  
		Last Modified: Wed, 24 Jan 2024 22:02:01 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2c19d4fd0adfded2a27bc5ccfabd897976141da4e28093a27ed68ded10b86f`  
		Last Modified: Wed, 24 Jan 2024 22:03:06 GMT  
		Size: 40.1 MB (40113381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3f29b3600bb84597d9583e51e75aa1772d8d0b5e803556660583e4c5b0daeb`  
		Last Modified: Wed, 24 Jan 2024 22:03:00 GMT  
		Size: 86.8 KB (86830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
