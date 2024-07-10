## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:97b53b4e817e034e19840921d4c3cd4a9c89a247ca8d6da141937da168ab1916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:3edb85271f4453bdb45da430c03030a0fb9e71520299feafdf8691bdaf6e7e50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321784997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc304c02c7b2d6c5763a1c0990ed04ba59766bc472de8835128d37c40360dcea`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:20:41 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 10 Jul 2024 17:20:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jul 2024 17:20:42 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:20:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:20:51 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:21:06 GMT
COPY dir:23b4ead9c2036754f644b00182bded9da6af0a8e5b9adaf18f46a103fb435a07 in C:\openjdk-21 
# Wed, 10 Jul 2024 17:21:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Jul 2024 17:21:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ad1a124fbd90523f5c17a2b76fa73394d844f86941264af090f155024cd16f`  
		Last Modified: Wed, 10 Jul 2024 17:40:52 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2d8886c6766a53c0b8e4d19f8642de7bca3a9bd424376eb402f4a33468096a`  
		Last Modified: Wed, 10 Jul 2024 17:40:52 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cec8f8ac15d117d4376079b1dc4f9f2f0373062b79b7a28deaac6ddc84b962`  
		Last Modified: Wed, 10 Jul 2024 17:40:52 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0d89c8324c507c3efbe6f90dcd2f22c20e5b212f48aa548db6be2a451bc5c1`  
		Last Modified: Wed, 10 Jul 2024 17:40:50 GMT  
		Size: 77.9 KB (77897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d78b0917266f1cb72cd484428a1816a6124940f8113629dd4f56cece113b2`  
		Last Modified: Wed, 10 Jul 2024 17:40:50 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea492950f57aea933e0bdda61b303ac51bf0a2e8307c9765766453708e4d104`  
		Last Modified: Wed, 10 Jul 2024 17:41:06 GMT  
		Size: 201.1 MB (201148393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f814116c0f951bd9febfb261ec0254c7c282b63cbb83b95f450923c5bc86e80`  
		Last Modified: Wed, 10 Jul 2024 17:40:50 GMT  
		Size: 61.4 KB (61402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a7f649f0d2c334e28d1d30e786ce0d2c724421424810aba7aec54afa4c7fad`  
		Last Modified: Wed, 10 Jul 2024 17:40:50 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.6054; amd64

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
