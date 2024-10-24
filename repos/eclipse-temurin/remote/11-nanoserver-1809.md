## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ff71da765896aa134ffa6b615f0e166893d8dac6316b4345313efec7b6f92546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:e8894914c9ed9f84fca0de46fad95e796bcfce9a8110bfa7b0ea2fca016b6f69
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350911849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4604cc2b75d0f91eeb35aa11b3e3f21a86dc50770c57a86f539b4c9df36901c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:52:57 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:59 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 01:52:59 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 24 Oct 2024 01:53:00 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:13 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:23 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Thu, 24 Oct 2024 01:53:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 24 Oct 2024 01:53:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8386ca84a42a5a00fddee6cd9b31d86a697cad61d9b806039c893a23bf8ed99`  
		Last Modified: Thu, 24 Oct 2024 01:53:34 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662b6b53e02149ac18379612f31485a295ea2583ae209479a7934a14e984dd6`  
		Last Modified: Thu, 24 Oct 2024 01:53:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21884acf8e5472336d275be39ab7780c14512b4f63fa59f320b0e5eddf41c6db`  
		Last Modified: Thu, 24 Oct 2024 01:53:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4a3e4691b37f0521901d53e02358be48600b5cd9829b5d6ae16af9be58a392`  
		Last Modified: Thu, 24 Oct 2024 01:53:34 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110d9b4954de45d99d87226c4ab6634ee7e49a95f49230d29caabaeee81ccb87`  
		Last Modified: Thu, 24 Oct 2024 01:53:33 GMT  
		Size: 65.1 KB (65109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e3f232025838e738f1d4f58468041fbc00c9850a99abb2683813a3182c1733`  
		Last Modified: Thu, 24 Oct 2024 01:53:33 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c3f039af6f20a9702888ac2d3b7e4c2287301c280b1f68f979de027847b67e`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 195.7 MB (195672627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ad1b18f4d92465877cc467d0b4d5123f4c8ad662553bb882ae77ddca0e68f5`  
		Last Modified: Thu, 24 Oct 2024 01:53:33 GMT  
		Size: 74.2 KB (74189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed66ac941a9dec591284b2dbb6df34f9c2a8903749ed72c54f566c8f99f6d78`  
		Last Modified: Thu, 24 Oct 2024 01:53:33 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
