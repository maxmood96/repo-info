## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d923406342fc93c0e034171cdda9215043e6606dfbaacfea22b3415a0b4fb865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:eec4d08388feb1ce63f4f54dc5a812d480b98a4f73801266eb5ab223302934ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151066156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020163f0e08e8a43c3d8f8884ec4c14b1645f56f78d0a435c731262b6a0375ea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:38:56 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 21:38:56 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 24 Jan 2024 21:38:57 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:39:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:39:06 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:43:35 GMT
COPY dir:a9fc3c1ff9b46f8bdbd24fa63859ebc78303825dc025dc6f7e000bebb5265b19 in C:\openjdk-17 
# Wed, 24 Jan 2024 21:43:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:08c499129f64a91355757a5df51fe1321c11b932a0a5e80011213119866a604a`  
		Last Modified: Wed, 24 Jan 2024 22:07:14 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40367a445cda9c710ad8265a4056068f53ad7062885eb54f62e63bec413b2e6`  
		Last Modified: Wed, 24 Jan 2024 22:07:14 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb62227560847f389da0902944a3fab348385cf80d7b4f5b80e3fe43e65d96`  
		Last Modified: Wed, 24 Jan 2024 22:07:14 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e870097bbec9d108c827ef762741942e0b263ab4982cc66a02c7a10debc8123`  
		Last Modified: Wed, 24 Jan 2024 22:07:12 GMT  
		Size: 67.7 KB (67659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089c7f8909528d9f067a21a311065a79e0d16d8edfc9047e9e6139812e4e7f24`  
		Last Modified: Wed, 24 Jan 2024 22:07:12 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64df5a4260e6229ecdd467bbd3f05a40dc8d1169a56ee7a576953f9ef3071c79`  
		Last Modified: Wed, 24 Jan 2024 22:08:28 GMT  
		Size: 43.4 MB (43420469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe526e5595325696fab7913556e6bfcb57d2c830238c7c9e7711676d5c3158e6`  
		Last Modified: Wed, 24 Jan 2024 22:08:21 GMT  
		Size: 3.0 MB (2980998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
