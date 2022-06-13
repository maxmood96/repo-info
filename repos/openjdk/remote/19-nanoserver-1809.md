## `openjdk:19-nanoserver-1809`

```console
$ docker pull openjdk@sha256:2304086faba8c485e56d93aebf54679dc4972bc20bce971471137db04b3c7c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `openjdk:19-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull openjdk@sha256:f71a0a33de5c90013d7b9a380793edf64440c18041197c9331f0f6a3a94fd371
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297946558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab2995e1c9adb715a0e91b79a6eb0699556ef4ffb1e8aed642b59625b15b8a6`
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
# Mon, 13 Jun 2022 19:20:09 GMT
ENV JAVA_VERSION=19-ea+26
# Mon, 13 Jun 2022 19:20:26 GMT
COPY dir:7ccdc28c44be3fe41e9809c1da412b55b6d9ec339350d3150d2dc21aca99fe14 in C:\openjdk-19 
# Mon, 13 Jun 2022 19:20:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 13 Jun 2022 19:20:47 GMT
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
	-	`sha256:b9b984221cb7d6088047e143df16b33b66f37b69cd07a2cf8d2538707a9d3059`  
		Last Modified: Mon, 13 Jun 2022 20:24:39 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab07538707055500f977f814d3108c1d31d96aece4464fad259a83107ebcba7`  
		Last Modified: Mon, 13 Jun 2022 20:27:57 GMT  
		Size: 191.0 MB (191043243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceee529ee4ed5e34cb0ddc2233da679eaadadeac026c93222815580887bb8c3e`  
		Last Modified: Mon, 13 Jun 2022 20:24:43 GMT  
		Size: 3.7 MB (3688336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e549bce7eb695c255f42b7a090039b00beb4b9b692e215fd6bb17ba7638274`  
		Last Modified: Mon, 13 Jun 2022 20:24:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
