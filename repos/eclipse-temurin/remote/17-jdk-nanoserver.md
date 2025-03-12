## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6298303d5803878ebe2e3b7100f1a4d74a994b919f1fc1016886efb1e09afd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:353dfa348294b1171402730022f8263300e82d6515b73fa210a010f8abf7e109
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393734170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7022e7d31f70829efd8a585759333b0cae33fadeec6ac40925845e345161aa9c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:16:25 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:16:25 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:16:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:16:27 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:16:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:16:31 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:16:37 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:16:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:16:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf03bf4dcb2b8dd659bee7bf147aa24762f3a0cc7e2aa33adfddf0047d79215c`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088269d513fb9983c4d3d983f4bcc662da1ea5f24b41d82deae65a87c00ba370`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e892b7a0401538b74eb744808f4b9d416b3af0714905798af57f740b3de431`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2f9daa939c353416c3abf677bf4b5fcc8bea82a0b3e2ea3b0813195156b57b`  
		Last Modified: Wed, 12 Mar 2025 19:16:49 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c5157d939e30c4c6d70441f9a00b2c348fe37fccc153781df3720e8b4f36cb`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 75.9 KB (75891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6881ab3a5e042640bdc83d950d08a2e11d911f2dfc24294a70f90468ad053a`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac3fec6e039209f3433c3148a973582252598ea93e30702222f518343589763`  
		Last Modified: Wed, 12 Mar 2025 19:16:57 GMT  
		Size: 187.2 MB (187235416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff621f45c77b0095a2b12ad443e732b221d7e9a054a83f8f4b1a1d5c69515154`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 114.4 KB (114395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb20823de1cff5151ed66c25ed14cd36154d9e2214a11b89891c220a3b9f4eb0`  
		Last Modified: Wed, 12 Mar 2025 19:16:47 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:17155b3c0849868ba2bf899fad662235af09ba9975dccdf34301920e406ffa46
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308121580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b99f4c9b4046e49b8c8287049de87d0f9c4a8bf92d25937cc5092c888a77fb1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:18:38 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:18:39 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:18:40 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:18:41 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:18:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:18:44 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:18:51 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:18:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:18:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b328139370a196fd32643d205d7cae2a59d0d0a767ebd444eb2ac8f36c3f6cce`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed1bff0c8c0431d3fc37b1c454c9235cc57ca654efdfabb2fcf9d02699bca76`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df91f22df2297ab58bd6db3381891731a5e6a674bd56753ef111cd89ecdcaf3d`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74619840efd21987a2480a08cbd3a641231fd6794d2e0cbc0f078f9d99cd81be`  
		Last Modified: Wed, 12 Mar 2025 19:19:04 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57890ddf75c9c00498b54243a54f996f8be7d3fed807595ddc60eb54c1b7dc26`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 78.8 KB (78773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366b8c090a41c7c11c4360f7f4e4da23982ee47a0b85fae5453ffc1aeeaf70b1`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a928294aeb039a3bcb66660e12d52aa22a43dbbbdafaad25d4f4790aeb6248d7`  
		Last Modified: Wed, 12 Mar 2025 19:19:13 GMT  
		Size: 187.2 MB (187233811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a3b39c01ba6a8f97a37ab80eb9432a2ac14d3bebf9e3a2d7f69cdd677e97d4`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 107.2 KB (107247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d21002906a9730ebba0223789b644b6738e517433d7a98daaea55e56780a44`  
		Last Modified: Wed, 12 Mar 2025 19:19:02 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:5781bff5bf816d006fdf018e8a30d805b89d720d1f282fc5235b2a047772b768
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297843428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8cdc418919092d41011876fa4cddb8d322b50b550bf22c14948fe7fed2b2d5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:15:39 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 12 Mar 2025 19:15:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Mar 2025 19:15:42 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:15:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:15:45 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:15:53 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 12 Mar 2025 19:15:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:15:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294bbf52e270ab816d64354fff14480e82044563ea516cfe2445c5752f0917e8`  
		Last Modified: Wed, 12 Mar 2025 19:16:06 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45d7d0c8a26f9a9fbb260891940d19b7113b90a6b8619af63234387f5d425f3`  
		Last Modified: Wed, 12 Mar 2025 19:16:06 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34032e84939bc7494ecd3353b22a0d3e3f65676930a072dae27d8427c495d64c`  
		Last Modified: Wed, 12 Mar 2025 19:16:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46860f768eb968b93f75901082396b49ee09bb3c0895adebf8ef5ade288b604b`  
		Last Modified: Wed, 12 Mar 2025 19:16:05 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc3cb3447e237cf506088adc1a73b0f666d0be9ecd752abbe18084e782c12f`  
		Last Modified: Wed, 12 Mar 2025 19:16:03 GMT  
		Size: 73.5 KB (73478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199f81bfc1dbdc528506dd1a3f47c6c9def7079d1dd2949844e434713d49f5b0`  
		Last Modified: Wed, 12 Mar 2025 19:16:03 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66306db801092627164406ae79e63a0be134f362000e4c1c736cd00e45e9861`  
		Last Modified: Wed, 12 Mar 2025 19:16:13 GMT  
		Size: 187.2 MB (187234969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22fa28e36d3030d8518cf061f52830c60a6c328eeb526090c6332089219a9d1`  
		Last Modified: Wed, 12 Mar 2025 19:16:04 GMT  
		Size: 3.6 MB (3621041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a503efcfb8c3585d2ec404571b6e6a1f46c9a44c0b0328950cf46be0ce837a4`  
		Last Modified: Wed, 12 Mar 2025 19:16:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
