## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b15cd8e56c26f35ff8bfec93086464af176919548e4d00c6b0b16e50bcf9fbc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.5696; amd64

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
