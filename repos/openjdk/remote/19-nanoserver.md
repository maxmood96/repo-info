## `openjdk:19-nanoserver`

```console
$ docker pull openjdk@sha256:9b4b08b5a3b5c98a79fd6a632a2d984e5fb43f2ea15a7007ac047c24eaea1984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:19-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:3466fdeab1cfdf070f21cb5972b52ee1a0c600f8eb65bcc679b0d28400cf2b94
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (297988474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0a312829dfcb57a5d621f856edb0b2de8c3382f71e5faf8958c4cd2116e404`
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
# Wed, 15 Jun 2022 19:36:32 GMT
ENV JAVA_VERSION=19-ea+26
# Wed, 15 Jun 2022 19:36:50 GMT
COPY dir:7ccdc28c44be3fe41e9809c1da412b55b6d9ec339350d3150d2dc21aca99fe14 in C:\openjdk-19 
# Wed, 15 Jun 2022 19:37:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 15 Jun 2022 19:37:16 GMT
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
	-	`sha256:bfa9bfbac36a5a356247190b58ac9d5bcd3d1d2fad8154d8d70cd31c8af48d06`  
		Last Modified: Wed, 15 Jun 2022 20:10:06 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e362f11aa795f9c92235134afbf652f610f0889d01d1b972405aa128f64f8103`  
		Last Modified: Wed, 15 Jun 2022 20:10:29 GMT  
		Size: 191.0 MB (191043757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25700f88cd860d4bddf876dd021ba802d0ef7518103d4fad2f21e6f33a07bbf8`  
		Last Modified: Wed, 15 Jun 2022 20:10:10 GMT  
		Size: 3.7 MB (3715639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d644127775fae7be6866da0597ec2d9d8cee48a56f08133fd657c442c7ab93`  
		Last Modified: Wed, 15 Jun 2022 20:10:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
