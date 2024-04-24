## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e74eff1110c89ef1b417c0ad645d518ae2f42597bb3b581faf8a2af7abfe1409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:bbafba9eae6b3b698bee10bec184122c37bd3e5b68e3b0f8066a73c0c54cfc30
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157079184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65c84a914a08012075abdc6bc0b5d21980dcac985fced7380a0beeed99ba234`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:05:16 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 24 Apr 2024 19:05:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 24 Apr 2024 19:05:17 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:05:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:05:28 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:10:47 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 24 Apr 2024 19:10:59 GMT
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
	-	`sha256:8dcf091fcbebbebeea32531bf662cf81e86b1fcb615435e409da811c0f478220`  
		Last Modified: Wed, 24 Apr 2024 19:41:36 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a6fcfb47ceb8b4eb2308c3ec1e799ad906c69b94f3d90599861bf994fb6ed2`  
		Last Modified: Wed, 24 Apr 2024 19:41:36 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48af84976cbb1708013331be6262b5a5b8d6aca50c6e24793cf4ec1910152194`  
		Last Modified: Wed, 24 Apr 2024 19:41:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5c1823c2ef5030c4e9fc741157cd268455663bdfbc1c10381b61d3c6e4d819`  
		Last Modified: Wed, 24 Apr 2024 19:41:34 GMT  
		Size: 66.6 KB (66564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8ac211f89ba3fc2f98c74bf5ca9f06f2b84fd4526df1b6e01e18394a353264`  
		Last Modified: Wed, 24 Apr 2024 19:41:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4665deef0832d476d0f11d63fa78ed0128f34b1f7c502ccec9d6c24624b91cdc`  
		Last Modified: Wed, 24 Apr 2024 19:43:00 GMT  
		Size: 48.8 MB (48757297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0495d030ef4498951eb142c844e5af716c65ab9cfc53a83a64fff1016187b6e1`  
		Last Modified: Wed, 24 Apr 2024 19:42:51 GMT  
		Size: 3.4 MB (3360792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
