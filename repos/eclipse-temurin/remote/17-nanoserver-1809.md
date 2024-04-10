## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3e08b35bfb44849b18fbff32406669ce82a5bd716bc7308f2f47ee54254cf14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:2f5b229103a96b117bad671551878c29f795b1689d006e06974f9bfea446abd9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295296126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1e5beba67edbdfc90cf11715e9edbade8dc3f24b19e59ad3cbb3bc50545e49`
-	Default Command: `["jshell"]`
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
# Wed, 10 Apr 2024 00:06:29 GMT
COPY dir:7333be24703ce46ff700c9b5bb2dfb5bd5b8a7a43d54ae48c80af36d6e10746c in C:\openjdk-17 
# Wed, 10 Apr 2024 00:06:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Apr 2024 00:06:44 GMT
CMD ["jshell"]
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
	-	`sha256:079cca75f4c307ca4c004702ab268fa0a843a916e7694bd86af7947a756bf576`  
		Last Modified: Wed, 10 Apr 2024 00:53:21 GMT  
		Size: 186.7 MB (186730651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6ab8bafca1278fe5d58315e6687ab2da1fb6fe658da063d20bc559a6da3393`  
		Last Modified: Wed, 10 Apr 2024 00:53:04 GMT  
		Size: 3.6 MB (3601979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ed730f650ca9fb4b8140744833d15d82924d3917d28bf8d5f1ab8699bf834c`  
		Last Modified: Wed, 10 Apr 2024 00:53:02 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
