## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f3d39e05576a54467b3045b3eb09fde725556aaa5aad26e7eb79351f04e7dff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:658f2f77229f075f71c224bfb3c33b9e970ad524ca2f5ed8c4f2ba2e27879714
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295000839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819009ac0ec3242142b101728e33b5490afa48c58dcacaf7d011f84310ad0728`
-	Default Command: `["jshell"]`
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
# Wed, 24 Jan 2024 21:39:20 GMT
COPY dir:7333be24703ce46ff700c9b5bb2dfb5bd5b8a7a43d54ae48c80af36d6e10746c in C:\openjdk-17 
# Wed, 24 Jan 2024 21:39:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jan 2024 21:39:32 GMT
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
	-	`sha256:665eb27ea808c82bbc38fe1ebdf4e89566ba2599312f6da76f86171209b48904`  
		Last Modified: Wed, 24 Jan 2024 22:07:29 GMT  
		Size: 186.7 MB (186730806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5aa0565369afcdb0b890b5946dfc51cba04e6a202fe4db408605507ad52e5b`  
		Last Modified: Wed, 24 Jan 2024 22:07:13 GMT  
		Size: 3.6 MB (3604191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bbd33c6653e69375db077d5a05a98b56367bcea9a0311813f57bc4f97c0820`  
		Last Modified: Wed, 24 Jan 2024 22:07:12 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
