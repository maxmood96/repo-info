## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:987187b67b52c902e217f82c6acf02e262369d31e1cff5bd582a1edb1963b59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:cbe79da69725ce3170d8b2160eb3334834ccb7b40f8357ae3de1f414620028d1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151357463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48c222770dbf6cd7007fabdf67cdd8552005f85b2f60cfc33d10ea4d9929b45`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:06:02 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 10 Apr 2024 00:06:03 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Apr 2024 00:06:04 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:06:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:06:15 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:11:37 GMT
COPY dir:a9fc3c1ff9b46f8bdbd24fa63859ebc78303825dc025dc6f7e000bebb5265b19 in C:\openjdk-17 
# Wed, 10 Apr 2024 00:11:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:3d519abe9c941ec0878800ce2579854ec7c358308f01ed189cd51b10801c105b`  
		Last Modified: Wed, 10 Apr 2024 00:53:05 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181d8191962de4010cfeb5b7808cceadf99cd9bb338f899caba71c526b18c70`  
		Last Modified: Wed, 10 Apr 2024 00:53:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8517840738d68f03aec494510f975ae348c05846fb627a0f1e44f467c955be0`  
		Last Modified: Wed, 10 Apr 2024 00:53:04 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e56832984d2d01ed3fc10ee3d8597b011ef322e5630f6c10532b28b8995492`  
		Last Modified: Wed, 10 Apr 2024 00:53:02 GMT  
		Size: 67.5 KB (67480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ac00c1b42ba4ff5cbd806bf91771eedec36ddab2bc43f7d8e368184fb24c6f`  
		Last Modified: Wed, 10 Apr 2024 00:53:02 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575699512a6dae655fb4ad351c72be0d3f2e8488cea0aed228ed1b1b9751586b`  
		Last Modified: Wed, 10 Apr 2024 00:54:18 GMT  
		Size: 43.4 MB (43420696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a1b15f37cd107f786ba08d86372ecca21e1409e32dd76a51a408b6e12f8cd4`  
		Last Modified: Wed, 10 Apr 2024 00:54:11 GMT  
		Size: 3.0 MB (2974394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
