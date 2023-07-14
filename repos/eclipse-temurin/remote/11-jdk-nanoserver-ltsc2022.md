## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9aeaba1e55182e700fa5f1ad968aea064fff743925bda2a1e7f5bbb56a570407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:2acf0f94ea9fba0a63b588cb73bb689e5a10c88b9f9a14249a16dee175b499c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313191288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dda92616895f83aa681fe0e070f229bccd4f982ea23ed4d3469c4278ad7459`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:12:08 GMT
ENV JAVA_VERSION=jdk-11.0.19+7
# Thu, 13 Jul 2023 22:12:09 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Jul 2023 22:12:09 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:12:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:12:20 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:12:33 GMT
COPY dir:aa85dc89894032bdcf98e5da06633e8de4813537c791ddbe3fc8bdfa8596f8de in C:\openjdk-11 
# Thu, 13 Jul 2023 22:12:47 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Jul 2023 22:12:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11750b624a775aa3c21a13406dfc54458855b8684e21efba5bbb9b27ee0b12`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89984660d577657926e73c66b7fcde177c4950f5025a6bf33df1b51c7941e373`  
		Last Modified: Thu, 13 Jul 2023 22:29:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358706f4b9d417c390fd1a356f6730ec6de76a5302e7c2f57398692c1b10d8d5`  
		Last Modified: Thu, 13 Jul 2023 22:29:14 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54056a08569abd48b6a54847eaac67709826a7ca7acae552af5b59bf4af84f8a`  
		Last Modified: Thu, 13 Jul 2023 22:29:15 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d968b25a111ee3ef2e094c8629b039007c792fa75dc90fb9dc8ee726e9bd6c72`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 85.4 KB (85378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe704e1ea918f25c3870438597179e08d0a4464642ae09ba8e7d80dd98dfd2e`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01178de7f214a9aa0811193cf117330e6a8d67c5d249d871253e3377e8eae104`  
		Last Modified: Thu, 13 Jul 2023 22:29:33 GMT  
		Size: 193.0 MB (192983863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09752d02dca5c17d4f16b31185e02821dbbffb487b31f09131d5930034b58da5`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 58.6 KB (58576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05ea1917ecc22df9a5aa16f6de76594544f74c2e227cfe3be96b07f6837f66`  
		Last Modified: Thu, 13 Jul 2023 22:29:13 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
