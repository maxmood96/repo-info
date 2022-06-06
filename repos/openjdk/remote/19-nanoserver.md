## `openjdk:19-nanoserver`

```console
$ docker pull openjdk@sha256:f87d813a4fbd556de37e75325dbfd6622eb7b520115fe490c50dd1182a40b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `openjdk:19-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull openjdk@sha256:15a032f98b9d3070906b9abea69f564ed28e948e0870e997fb3df6c515c2a599
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297606227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f804baf8d5c6ac210003726634f489ff6bcbc6633151a667b818adeeab0ca61`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:49:49 GMT
SHELL [cmd /s /c]
# Wed, 11 May 2022 15:33:35 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 11 May 2022 15:33:36 GMT
USER ContainerAdministrator
# Wed, 11 May 2022 15:33:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 May 2022 15:33:48 GMT
USER ContainerUser
# Mon, 06 Jun 2022 18:22:49 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 18:23:05 GMT
COPY dir:f00fcd7f11e3b5d5f4307de4f31d1dcb2f32ff6f18a43af035daea84ae82abc7 in C:\openjdk-19 
# Mon, 06 Jun 2022 18:23:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Jun 2022 18:23:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5592374182790eb41396d922d16be86f39a125562f29ea3ed221a94aeec2af45`  
		Last Modified: Wed, 11 May 2022 16:00:35 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27258317e27e0cfabcf779836e0e38e0809f5ba5b2e2ce61b0c4761494eabf2f`  
		Last Modified: Wed, 11 May 2022 16:00:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90f575ce9dbc595a6266a2d907de169473af97a71414d6a81d122bfc9cd5e39`  
		Last Modified: Wed, 11 May 2022 16:00:33 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40175500d750084c8212d8ea8f70d757ec3255fcb2fe588e2663c8a405187094`  
		Last Modified: Wed, 11 May 2022 16:00:33 GMT  
		Size: 74.5 KB (74495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d665e0106401630d154ad3a944dc128966740b1e1b21d2fbeab345b8da177a`  
		Last Modified: Wed, 11 May 2022 16:00:31 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd761b7147761e7d04d6f88bd953df81e55d79d2ef94128ed497c1ed936de8b`  
		Last Modified: Mon, 06 Jun 2022 18:33:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03eea51aec72da9dfea6e45cefc27637be1e3ea914983d6b6847945b922d50e4`  
		Last Modified: Mon, 06 Jun 2022 18:37:17 GMT  
		Size: 190.7 MB (190746124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32e94d7e9b5c6b1bf3d5b080a4ff9b68c1c439017cdb9fcde6f4f1d4daa8852`  
		Last Modified: Mon, 06 Jun 2022 18:33:53 GMT  
		Size: 3.6 MB (3644840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6347c79da87eec926abf812530ff611620a50f2760d5f4f7baed4ddb9e05baa9`  
		Last Modified: Mon, 06 Jun 2022 18:33:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
