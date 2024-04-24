## `eclipse-temurin:8u412-b08-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c416bbd6141a12ffcac75b80fe5d5552b0dc4f6f25058f18fea39f9bc6e843b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:8u412-b08-jre-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:fc14cbda97ce2efd60acf69433d62157766f726bd7c710fd29a34f156a2ac9ef
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161263976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394e9f94609f1b552ddd7569d0f9420b02b4d17619f016614192ed072947787b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 19:22:38 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Apr 2024 19:22:39 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:22:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:22:55 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:23:37 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 24 Apr 2024 19:23:49 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a568162a8db2139c9b7f50bdca7e6de2f6e46f3a23196ccf7b33d019ad6c3f4`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76150342796de52322a78b1675aa420817cbf16aa69b853f3213c97193064da1`  
		Last Modified: Wed, 24 Apr 2024 19:46:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d61c15b18ab0fae7ccb0fec0d9464105deb40fe2b2e29d96c6d93975524297`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792f549969d948ee4d8765477e3d71b4a2d4fa9c0c89daec775697ad31d12ad0`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 86.3 KB (86274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c5d1ba740a169c8c5fabb77a7268e210555e1c13d639548d947228a4f7d950`  
		Last Modified: Wed, 24 Apr 2024 19:46:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a138370e43b7219d7ce691dec52305825c312df34e0e0ff0a470544a32997a`  
		Last Modified: Wed, 24 Apr 2024 19:46:34 GMT  
		Size: 40.1 MB (40117772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb7f347f4c25ad39fabe032d57709fb516f38702f27580f71a5753a3609492`  
		Last Modified: Wed, 24 Apr 2024 19:46:28 GMT  
		Size: 61.0 KB (61012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u412-b08-jre-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:c4c4d209af2d1af87c9603b2b02c2e570b46c7c7d3e8d3ac65b215e9a1daee24
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145155245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b23dc866f70f2102c9688dc2397514689c6108ca465595122f2b185967aed70`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 18:30:04 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 24 Apr 2024 18:30:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 24 Apr 2024 18:30:06 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 18:30:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 18:30:26 GMT
USER ContainerUser
# Wed, 24 Apr 2024 18:36:06 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 24 Apr 2024 18:36:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1aba89d9ebacd4f1369cd48d26d09c1a19c37a1bb267bca108af48fc1aab5a`  
		Last Modified: Wed, 24 Apr 2024 19:33:30 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66a02d1909bba7585a63ed513f0c7c5bbd6364e3a52b3b363b25890a8bfa166`  
		Last Modified: Wed, 24 Apr 2024 19:33:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e870db953193353980429b04bed7cc708680f15d0c432e2aa6f6dda4ea88157`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd079869a94c991c70a1182afbad7cc1fc3ab25e82ead25390f279108d4344cc`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 65.8 KB (65774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef74b03f97dccf54dafc9c09e7fef7c0f6b60eb15ed9450d9f147aaa750ae0`  
		Last Modified: Wed, 24 Apr 2024 19:33:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d017b44b9bab4d068b3128a3df7dd16bde33da14c81fd9fe993fc17e430fe0ff`  
		Last Modified: Wed, 24 Apr 2024 19:34:32 GMT  
		Size: 40.1 MB (40115155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2947ee204c0722d62ff3fff6c69eee2a1da681e105e26b0f0250f9cb9c2b64ff`  
		Last Modified: Wed, 24 Apr 2024 19:34:26 GMT  
		Size: 79.4 KB (79376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
