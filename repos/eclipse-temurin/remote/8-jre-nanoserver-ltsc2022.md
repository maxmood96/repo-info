## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dcee8ee9a8c34e8556c9eede5acafa53b3d883bdb3ac106b6c62406f1e530f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:d9cf215ee40579ac3e875ecdc6cb6ac8130f08beb0ce6bec5d191646f4d95fb5
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157536109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3188341404e85fe6e9b3fed326f61b363eb481de0b640f8d78254c835be5696f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Jul 2022 17:25:17 GMT
RUN Apply image 10.0.20348.825
# Wed, 13 Jul 2022 15:22:06 GMT
SHELL [cmd /s /c]
# Tue, 02 Aug 2022 18:36:21 GMT
ENV JAVA_VERSION=jdk8u342-b07.1
# Tue, 02 Aug 2022 18:36:22 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 02 Aug 2022 18:36:23 GMT
USER ContainerAdministrator
# Tue, 02 Aug 2022 18:36:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 02 Aug 2022 18:36:39 GMT
USER ContainerUser
# Tue, 02 Aug 2022 18:37:17 GMT
COPY dir:9db60ee3ad3f16cf75b351ecd1309f1d56f486fa1a4d388cea2f63f8b51258b8 in C:\openjdk-8 
# Tue, 02 Aug 2022 18:37:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3719b23d309b17276277110a008a58133c9fc92465d2519f2f32c9961c39887d`  
		Size: 118.0 MB (118046090 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:569505cbc9e1bcad1fbbdd7edca170e5a914864bcad2f53e1fc5d5816ecc8aa5`  
		Last Modified: Wed, 20 Jul 2022 12:54:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589515435cc74b16ecdcca85063c8c5a3e52b45ffebb06f73aacf7c70fc999e`  
		Last Modified: Tue, 02 Aug 2022 18:47:12 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098a92f594e84ecbbb8cd69a3dbfbabe32eac918acd2a16692ac4e13cab38b32`  
		Last Modified: Tue, 02 Aug 2022 18:47:11 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0cded47c0b33befaa67a297688be13eadaac8604b6562999d34f4bafc9eefd`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f52bbe4c2d6aa576880dfc7f24542be14e2379fa604502078a17de5c963ada`  
		Last Modified: Tue, 02 Aug 2022 18:47:10 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5ff650044ea148647cc2fc894105075f8dda748117560fb3bfd2457ff9663`  
		Last Modified: Tue, 02 Aug 2022 18:47:09 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f852610aeecf09bf9810470d2cf43c6b677c7dc215b8a4979dc74cb2be66099`  
		Last Modified: Tue, 02 Aug 2022 18:47:41 GMT  
		Size: 39.3 MB (39316634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fd39ff7bf4bb1074d952bc312a9a0718102b01d2937a70b467bd5c059b2bb`  
		Last Modified: Tue, 02 Aug 2022 18:47:34 GMT  
		Size: 68.7 KB (68747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
