## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:78b2aea27cd2298dda8379733d9fd619ab3a98b007f80767e22088b93ae1bce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:75a87eddb121301eee74ee0bb4342ea225d75b829b10687f6c1b9191f4db1118
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316371462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143656d52047a9c3e0866b202503a7d110ec1b59d86d3d406ec558533377055a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:37 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:38 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 01:52:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 24 Oct 2024 01:52:39 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:52:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:52:44 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:52:52 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Thu, 24 Oct 2024 01:52:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 24 Oct 2024 01:52:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbc7d875574501db20ae968ffa3ca5e31c2dd961b9c1554fc1c5c3149ce8015`  
		Last Modified: Thu, 24 Oct 2024 01:53:05 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db40c8673aaec3622e8771c38b7a27950f142e4975f6d9c8ae2f548d32f6da27`  
		Last Modified: Thu, 24 Oct 2024 01:53:05 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e9331d14584d41494a7f6765bfe1473c61f13f2546050540952da5ff83b88`  
		Last Modified: Thu, 24 Oct 2024 01:53:05 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9da9910ec704e071a0d3445fc325e88761cd12225f504408227af65d8dc9fe`  
		Last Modified: Thu, 24 Oct 2024 01:53:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee46536d5c66dffce0ba022f900928149e2971d0b19b886f339708443bf159c`  
		Last Modified: Thu, 24 Oct 2024 01:53:02 GMT  
		Size: 74.0 KB (73984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d99766bf53f160451f4f8ca7fe3aecefc88b9d60cb4198337d79a53438950a0`  
		Last Modified: Thu, 24 Oct 2024 01:53:03 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038fee835c79333b7c847e03824de74914b720e21b1292c22a7344a0eeccab8b`  
		Last Modified: Thu, 24 Oct 2024 01:53:13 GMT  
		Size: 195.7 MB (195671989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbc41b6784057ba42b3806a5ad9180891c2034f2abdf5db8edffd4ed5a6ab41`  
		Last Modified: Thu, 24 Oct 2024 01:53:03 GMT  
		Size: 108.2 KB (108216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d608c0220fd8684ed4378f22965ccfa32213216ab6eeb19f0f232bb1375a09a6`  
		Last Modified: Thu, 24 Oct 2024 01:53:02 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.6414; amd64

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
