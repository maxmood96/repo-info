## `eclipse-temurin:21-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ea53db672230a49c5a59731e1a38378d0dd92b42b8d755dcc442b40fe2a3ce82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:21-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:7cc5671ed003aa2fe67f530a3db7342e0f72d056dcf91968701820b12b8a2aec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360128229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623e9d27437f29f411720e5a8290076a317650480f0231567da95a4cdf09319e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:04:08 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 10 Jul 2024 17:04:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jul 2024 17:04:09 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:04:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:04:19 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:04:32 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 10 Jul 2024 17:04:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 17:04:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aabadac1b5e8483dd0ae114f714f10423b6947f765a9dde2c2c6d731513597`  
		Last Modified: Wed, 10 Jul 2024 17:35:07 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fcbbd57410aa25734b68c59c6ae804fd136d1f505eb7e01e5324081af58f06`  
		Last Modified: Wed, 10 Jul 2024 17:35:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9078f7dbe89c925f6ae3f302e728969d791fccb21aa0e35eb541a30a028f1e61`  
		Last Modified: Wed, 10 Jul 2024 17:35:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887d113cf376f063e8fba98477195e8a9d5b2768bbc11bc929ff28828558993`  
		Last Modified: Wed, 10 Jul 2024 17:35:05 GMT  
		Size: 66.9 KB (66918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea31cc61a3c1ac32f5bcede5a330efc719315ae087ed5c5202ce3ee843b7d2`  
		Last Modified: Wed, 10 Jul 2024 17:35:05 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28491676ed49be3bb0473f9d84347086df6f97aad948d66464df8171b97722e9`  
		Last Modified: Wed, 10 Jul 2024 17:35:22 GMT  
		Size: 201.1 MB (201148335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfac83f81b690a912ec2a3669fb15fb5aa667a35d42245b3fbde8a04b529342`  
		Last Modified: Wed, 10 Jul 2024 17:35:06 GMT  
		Size: 3.8 MB (3824704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e07872d6715b97f2e0a1bdddf4acdc822f3d90ec837a891085ab15c819dd953`  
		Last Modified: Wed, 10 Jul 2024 17:35:05 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
