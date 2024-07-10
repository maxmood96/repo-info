## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:05a6f1f9a43f2fe68f8c58d0010a1094a93d0119b9e37fb7c71f5fb13d9bfb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:5fdc351a657730fc48b15ff089df4f79ae2f416282bf222fbc71329435c744f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207278101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae5b3c1b02e20a99e6357d68ee2d59e4ef8cc4fda91463e4bc9345fd895caa8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 10 Jul 2024 17:08:27 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 10 Jul 2024 17:08:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:30f19394ebdc28b233bb4fffd2856e2eea562ca9ba28019d8f7a2ace08643105`  
		Last Modified: Wed, 10 Jul 2024 17:36:15 GMT  
		Size: 48.8 MB (48758680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab8dc373e4494ff305d5e0987263d49476e033d99b40f48b704022fa31eda17`  
		Last Modified: Wed, 10 Jul 2024 17:36:08 GMT  
		Size: 3.4 MB (3365385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
