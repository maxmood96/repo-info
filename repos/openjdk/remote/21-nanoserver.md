## `openjdk:21-nanoserver`

```console
$ docker pull openjdk@sha256:3aa528281ba4bc77b7c81e542562dc78f9ad5a2e432a1aa76733e1b842b89483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4010; amd64

### `openjdk:21-nanoserver` - windows version 10.0.17763.4010; amd64

```console
$ docker pull openjdk@sha256:e15877f785aceb1277fba9f0904ba6d7a8aeb0d51c30c6f2c35401f2b2ea3cec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304775957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478800a02ccecd79ffff7d99f28a9b6e9f013462e798227c158c028abbcf54be`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Wed, 15 Feb 2023 22:46:15 GMT
SHELL [cmd /s /c]
# Thu, 16 Feb 2023 02:20:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Feb 2023 02:20:17 GMT
USER ContainerAdministrator
# Thu, 16 Feb 2023 02:20:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Feb 2023 02:20:27 GMT
USER ContainerUser
# Tue, 28 Feb 2023 01:23:47 GMT
ENV JAVA_VERSION=21-ea+11
# Tue, 28 Feb 2023 01:24:04 GMT
COPY dir:8cbb4e4470b838f1188d1e0e669a26921a7d9fd01e14af3a535fbc50ca86719c in C:\openjdk-21 
# Tue, 28 Feb 2023 01:24:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 28 Feb 2023 01:24:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185f49bd9e9c2d18b1dcf8f1f67123b4146383e07a158cb4623d96fb2d18c05`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b040b2f53926e6a02088ae0173e36f1f01b75c581f435607dd2f86dfe095f4a`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0134c2e5e080e208ed0917cd948446b60048729433bf731850e4165e426977c`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf352af9ffad203bc10ae043af50fee20ca5c0e02a370dcc2b040c702c9d48f`  
		Last Modified: Thu, 16 Feb 2023 02:29:16 GMT  
		Size: 67.9 KB (67900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58adc24996cad294b1ceeed12449ee5750c4442dfcc5e3135984239942ba8503`  
		Last Modified: Thu, 16 Feb 2023 02:29:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfc29ce16e17c5da493c74e28ff8a48e196d450b4af577df6dc0c6024929c35`  
		Last Modified: Tue, 28 Feb 2023 01:27:51 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae5e177bfcac7e08add07de3eee2aca803cb2955b5e5cab6403200aa025d060`  
		Last Modified: Tue, 28 Feb 2023 01:28:16 GMT  
		Size: 194.2 MB (194224977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00feee8636f076d3e3393008b2688135ba746b90be801a68a1753fbccb20332`  
		Last Modified: Tue, 28 Feb 2023 01:27:53 GMT  
		Size: 3.8 MB (3801339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e204d417219075f0403a1726b73a4305d02fa8f409eda054c3451ec0ec2941`  
		Last Modified: Tue, 28 Feb 2023 01:27:51 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
