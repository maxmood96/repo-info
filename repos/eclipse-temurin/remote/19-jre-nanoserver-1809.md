## `eclipse-temurin:19-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ccaaeedba8e997a7ad020a730c176f391dccd5ed080615f0ad84e4613c22f809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:19-jre-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:c8d3e5accd5e8957bf1aa05b5dcd408f59da2b75af11be55a4ff4f7be4f35586
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151636843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4f8942efc23ea5753e7edde66033cfde421355b6d5b3d0f2ae446dfc1c766c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 15:49:40 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:49:40 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 12 Oct 2022 15:49:41 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 15:49:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Oct 2022 15:49:50 GMT
USER ContainerUser
# Wed, 12 Oct 2022 15:54:03 GMT
COPY dir:941cb8f5f97f3f5d2a48807df827e977e3ea22f3a1de758e43d87dd2ec67a41d in C:\openjdk-19 
# Wed, 12 Oct 2022 15:54:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30097ca6d1d1e22585cebbc642cd4ef89dd3e2b6099e607d6273094d02e4390`  
		Last Modified: Wed, 12 Oct 2022 16:11:20 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e93472d5cae1a3796bc8611a28845b93f3fbd8ce1227629553340262f85530`  
		Last Modified: Wed, 12 Oct 2022 16:11:20 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaef6dce2ef28ca7e9d90ec78acf76ecd1b44bddc4483980ef93b559485616ae`  
		Last Modified: Wed, 12 Oct 2022 16:11:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab5cb4797cf8a3306503f588c34ee6b45e7c5568de6072b49e61368d6ce76cd`  
		Last Modified: Wed, 12 Oct 2022 16:11:18 GMT  
		Size: 68.3 KB (68329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17b04d0489735abb2f8e7028d93ec2ce99c5797854147065d2a8ee6f970e8cc`  
		Last Modified: Wed, 12 Oct 2022 16:11:18 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f2aa9aa9fb059115eb39867e789373e215f49f93d798bec47e5ba0f776ea36`  
		Last Modified: Wed, 12 Oct 2022 16:12:40 GMT  
		Size: 45.1 MB (45102184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848ac54dc28a4fcc1d48e7e183b7644934a07086fb11c2956cabb4e3620812de`  
		Last Modified: Wed, 12 Oct 2022 16:12:32 GMT  
		Size: 3.1 MB (3083292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
