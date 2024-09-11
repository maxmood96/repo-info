## `openjdk:23-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:39ed04c51e5d4f01b423c5b1f3b33dc91f47e84330936dfa192214d468ccaa3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:23-jdk-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:a40640ad0390e95741d1afe5a77ba744b6d1fcc3f6f019a243a430cd2c844906
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365317396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2199f6d7e620af1390ada34595627233daf1b43f057496f9a9eaad00796f7451`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:07:23 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 02:07:25 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 11 Sep 2024 02:07:26 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 02:07:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Sep 2024 02:07:29 GMT
USER ContainerUser
# Wed, 11 Sep 2024 02:07:29 GMT
ENV JAVA_VERSION=23
# Wed, 11 Sep 2024 02:07:43 GMT
COPY dir:7241c997b61b8182ab926524436a25e2a4c14ad587c6199f728ad06ec7b46fd4 in C:\openjdk-23 
# Wed, 11 Sep 2024 02:07:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Sep 2024 02:07:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98a2feaccbec0905ab1c77a1ce5f404a004bee1c5094640793ab09962b849d6`  
		Last Modified: Wed, 11 Sep 2024 02:07:54 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e068bf18dfac8fb254b68a657c34ddccd980094db23e124ebc58625150e944bf`  
		Last Modified: Wed, 11 Sep 2024 02:07:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2eaee7efabecd6ebaa6dfc5b07341f55c2183149fb1445c0862746101f570a4`  
		Last Modified: Wed, 11 Sep 2024 02:07:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02882ff07502ee2ded7a133a2f39cc83c420e7ab19ecb801c397cbccdb32da85`  
		Last Modified: Wed, 11 Sep 2024 02:07:53 GMT  
		Size: 70.3 KB (70324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08c2254a7c25260012ab75e5b20dee6ccf168306f2fcb258f68f7e1f3c0dd40`  
		Last Modified: Wed, 11 Sep 2024 02:07:52 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20635b657d8cab035c3025f748e88eb3b0096d4fe691e623b1f914d566bee881`  
		Last Modified: Wed, 11 Sep 2024 02:07:52 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de156868a1cd57dcf763f5e0ef72bad8bbe5fa467fe6067942d83011125c9c2`  
		Last Modified: Wed, 11 Sep 2024 02:08:03 GMT  
		Size: 206.0 MB (206041257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba940c7af78ec75cead78ef5e6ef17e2db4d41c2b64a676eef3fe32610a98cf8`  
		Last Modified: Wed, 11 Sep 2024 02:07:52 GMT  
		Size: 4.1 MB (4118744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a59c24516668b29de70c42af1ea7cec07a5c79c2913e8b7f1ef1779bab4c512`  
		Last Modified: Wed, 11 Sep 2024 02:07:52 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
