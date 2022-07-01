## `openjdk:19-ea-29-nanoserver`

```console
$ docker pull openjdk@sha256:320f967351b7d1b9d614b03e4d611ea58a649f98c1add1fb7feffa6d68d842c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:19-ea-29-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:389aafa587b404426d8451e6f9be11b8c68da36a44888b83a8478b197b2ea88b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298139188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49a1526ae0237f3fe98c146ea73f9a16ba258019ce8ab98072f3cec2130ea4f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 19:36:19 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 15 Jun 2022 19:36:20 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 19:36:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Jun 2022 19:36:31 GMT
USER ContainerUser
# Fri, 01 Jul 2022 01:23:59 GMT
ENV JAVA_VERSION=19-ea+29
# Fri, 01 Jul 2022 01:24:15 GMT
COPY dir:73a55bf52d742b4f9dee417ab6b6dd38e9077c14e90a7aa56f05074616082dfd in C:\openjdk-19 
# Fri, 01 Jul 2022 01:24:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 01 Jul 2022 01:24:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b58c89b4b822d0d5d5f1bc8225f7a37f7dc8a316f92594090c400a34a1a51ff`  
		Last Modified: Wed, 15 Jun 2022 20:10:09 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb2fbbb0972907c5181cdfabed7833e7b033a86dcac9a55e84b1e6dc2861652`  
		Last Modified: Wed, 15 Jun 2022 20:10:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28327af37fa2c35b8687ad7e3ec93de3a24924e9504e2eaadb1ef6cd98728065`  
		Last Modified: Wed, 15 Jun 2022 20:10:09 GMT  
		Size: 68.9 KB (68857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266bdb7d76259c486b3300ec15922ed2162301ab3c50cfd1c9f8b1ed4ca95b1f`  
		Last Modified: Wed, 15 Jun 2022 20:10:06 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d74b1da9792601f36e43acc84acf89c50060034970ad60a68f03088f6bb7a4`  
		Last Modified: Fri, 01 Jul 2022 01:49:03 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14196c11c2254fd7469e3ed88dfad9a39b5918137caecba111daeb07aa3f2c17`  
		Last Modified: Fri, 01 Jul 2022 01:52:31 GMT  
		Size: 191.2 MB (191195333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201f0b0e263ffc4da6e37284888e6534407801064bf242a6a4ba3a9d88b3c41a`  
		Last Modified: Fri, 01 Jul 2022 01:49:03 GMT  
		Size: 3.7 MB (3714987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b4cad0567aaf143dff4c90d4e20a87995733aa507bff3617ed4840ace1fb65`  
		Last Modified: Fri, 01 Jul 2022 01:49:02 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
