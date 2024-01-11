## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:37e8e645e36110aacf635f6907699b298070dc4fdb199b53b5119c349a5ea01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:b6ff0e97822286fd912f9dcc32cec58b96ead354869d130d51ae6d750609dfe3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151042164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fe958d2c01aef1cc091c938982172cefac6bda136d2a06b160e7f529dfa3b9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:00:41 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Wed, 10 Jan 2024 23:00:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Jan 2024 23:00:43 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:00:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:00:53 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:05:51 GMT
COPY dir:d3f692ac99669197443250e31cbc5c2f5282787fd78589cc9b6c2e91236738f4 in C:\openjdk-17 
# Wed, 10 Jan 2024 23:06:01 GMT
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
	-	`sha256:3b9a8e48f7b70aa846fef8e327633ae99125eb19c526878853e593722a8ba3a1`  
		Last Modified: Thu, 11 Jan 2024 04:14:30 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4513b07e88feb2d57c2a828ef36ab915ec9709d1b366536c51a467f0ca10c89`  
		Last Modified: Thu, 11 Jan 2024 04:14:30 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f370b3a10a26cd8f157043e5b466fc7dea7c7701e6dee72deab1fb552d43065`  
		Last Modified: Thu, 11 Jan 2024 04:14:30 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bdbe4e627e68c427a64000883a86d59fdc0a52b5d44d690d6549defb11ec1a`  
		Last Modified: Thu, 11 Jan 2024 04:14:28 GMT  
		Size: 70.1 KB (70113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359123382e7ac5b343abd17864aed991729b9ef0e234b893bbfacbd3836e2a8f`  
		Last Modified: Thu, 11 Jan 2024 04:14:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b979db86e9141c2ede17b0d46cd9b95bd760b284f40423fab882b04d1d5237`  
		Last Modified: Thu, 11 Jan 2024 04:15:49 GMT  
		Size: 43.4 MB (43396492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c63a6fd790a91240367fb5c1ffd73f3c3ad6828593e88a1b44f7ee0f815c48`  
		Last Modified: Thu, 11 Jan 2024 04:15:42 GMT  
		Size: 3.0 MB (2978470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
