## `openjdk:15-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8e3eb8bccf4365418902aef6e03064f0027b436a5eb2f6d07f97d7439ae48c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:15-ea-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:e97a12c73498370e3ef1d974c08753bf5b29066287bb5e49bf72f826390d6ef2
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298543914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7d6087bca841880a9040b6ea105b886a9d353da200d5a8da931ab7fd4ec024`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Thu, 19 Dec 2019 01:29:02 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 19 Dec 2019 01:29:03 GMT
USER ContainerAdministrator
# Thu, 19 Dec 2019 01:29:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 19 Dec 2019 01:29:16 GMT
USER ContainerUser
# Mon, 30 Dec 2019 23:28:31 GMT
ENV JAVA_VERSION=15-ea+3
# Mon, 30 Dec 2019 23:29:36 GMT
COPY dir:a224fada1120850ee6a031094783ac6433704ad0afb1a3833c8c69de7b03c838 in C:\openjdk-15 
# Mon, 30 Dec 2019 23:29:56 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 30 Dec 2019 23:29:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:163d55b77f49371136083ba8066ddbec4afad6e1f4fbba77fa4ffebc99a8098a`  
		Last Modified: Wed, 11 Dec 2019 20:01:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63bb05b94288d5ea0447e7c6b75a854704f420c56d3b13acab4d9b2e03cc3f4`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 914.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64927380268ba75b4d8445c6eebea564ad1af3f6ffcd0ab9856b348138b44532`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca8bce76a22921ecaa2f6065834a3d494b61f569022c5b64bf0c9fa9c5bc63c`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 71.4 KB (71377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b95fb661adc21f04050381ea3e21b42927fa5df24d3b78a394b6e71e7992c12`  
		Last Modified: Thu, 19 Dec 2019 01:38:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7011998865111aa514da071ac9a4333311c7b4e50f0d729462c446a60e654e05`  
		Last Modified: Tue, 31 Dec 2019 00:16:03 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06cbc13940d350077b6bcd38f715094bf5f0f29b4f3b9b7fba43d083f8765ce`  
		Last Modified: Tue, 31 Dec 2019 00:19:11 GMT  
		Size: 193.9 MB (193916148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c310450bd9342c0b98661b3650327f2eb25a37952d38c7b23afa8a81f7e7552`  
		Last Modified: Tue, 31 Dec 2019 00:16:04 GMT  
		Size: 3.4 MB (3444679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd35035654ab08a166221de1bc5083edfacd59465465322326cc4e871732d7bb`  
		Last Modified: Tue, 31 Dec 2019 00:16:03 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
