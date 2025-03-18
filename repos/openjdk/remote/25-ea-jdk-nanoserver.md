## `openjdk:25-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:ee56f81b415a0420a57d2b855220ad1d8e13c61bf79b8961a9339c46e92dbbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:601d70bf5f747be83a35f776652bb7d94d051e4631757e20b18fd5d0b710c816
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (413979123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f8734c3c75bd9128834cf07da7ac1b0f6608a21313fe260dcdefb0f7e7e9e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Mon, 17 Mar 2025 22:22:13 GMT
SHELL [cmd /s /c]
# Mon, 17 Mar 2025 22:22:14 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 22:22:15 GMT
USER ContainerAdministrator
# Mon, 17 Mar 2025 22:22:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 17 Mar 2025 22:22:18 GMT
USER ContainerUser
# Mon, 17 Mar 2025 22:22:19 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 22:22:27 GMT
COPY dir:3bbdecdaf44fd794a45fa39cf7b31efe4cc2d91c5e3e7c4c5333407317959149 in C:\openjdk-25 
# Mon, 17 Mar 2025 22:22:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 17 Mar 2025 22:22:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ae974e71c7ed6ed32b3b9148a32449b4e9e025d7ee33295e7bd082f8f79e3`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11303ce1488b9b0ac7ce4243b34267067f6a0a545dfbab43128e6aa576ff908d`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63523ba142d168932523fc2a23dae1145b3c1e6709d3a54db5f4ea9bed14d98b`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aca364136771e9524c8408279d4de4514fa0cfde1e0b5cbc00e778d04dfd9a1`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 76.1 KB (76098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a78a8e6e2549ac32bae8276a7c43a8fed69851a985659ef4c0bbda471d7a917`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f71c25076f272f3bd6008f431f9d5125320e3d8fa1572cfd74e194a3b1d98f`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ccb08a91ea6e6944f12190b891774cada5bad79ce67bbc52ec570f381a94d2`  
		Last Modified: Mon, 17 Mar 2025 22:22:51 GMT  
		Size: 207.5 MB (207470546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1954fff5b0ba549a590d4de6007f14311a0b9b27c5eb6db7ee021a4ee22f4efe`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 123.9 KB (123886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9d2ce3bc1bda95aeabf9b1221a3f21f99d6231221cad8e644e2659f1432457`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:c77dbb3053fb47b73f9731046399d0489984ea983bca79fa673131e950bb39ea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328356691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7870d05b6185e4472da52f0dcb479b9d19cd290e19b2f7eebf4173eae11f387`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Mon, 17 Mar 2025 22:24:28 GMT
SHELL [cmd /s /c]
# Mon, 17 Mar 2025 22:24:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 22:24:30 GMT
USER ContainerAdministrator
# Mon, 17 Mar 2025 22:24:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:34 GMT
USER ContainerUser
# Mon, 17 Mar 2025 22:24:34 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 22:24:43 GMT
COPY dir:3bbdecdaf44fd794a45fa39cf7b31efe4cc2d91c5e3e7c4c5333407317959149 in C:\openjdk-25 
# Mon, 17 Mar 2025 22:24:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d56818458d0087e4b37795636958615ab9394e7ae440b701fe494df5f72c06`  
		Last Modified: Mon, 17 Mar 2025 22:24:56 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd0c7d30d7e41d27ba9c6e225f08596dfb466b767e9ee422763d030a09833ab`  
		Last Modified: Mon, 17 Mar 2025 22:24:55 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2117d53188dda548dba210953c298809c8030a7cc4d29c07d43296581b00b68`  
		Last Modified: Mon, 17 Mar 2025 22:24:55 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ce3d0bcaa9bb541698d77e9b873eeb2e07fa7e64a8602cef452d9764c050a5`  
		Last Modified: Mon, 17 Mar 2025 22:24:55 GMT  
		Size: 78.1 KB (78136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b173a73312a2a4ba227df7bd5f7bfeeea243c6f40b79518909c50eececd36341`  
		Last Modified: Mon, 17 Mar 2025 22:24:53 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e9d21af0e47e5724fc827df149dcf485282a9a1c615b4ab115113a3c980d2c`  
		Last Modified: Mon, 17 Mar 2025 22:24:53 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf593ddf7ee51a09389814b30562662aec6d4383b582ff6c3e877191567d373b`  
		Last Modified: Mon, 17 Mar 2025 22:25:05 GMT  
		Size: 207.5 MB (207469416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe50f2590900ffcf1afc6ece81affcd587b6b68ddc54c340efa81c06eb6a646`  
		Last Modified: Mon, 17 Mar 2025 22:24:54 GMT  
		Size: 107.2 KB (107153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac09d8e0f0d5ae5926ae0811524df6530f8e6c58d572e59f164139806ef9294`  
		Last Modified: Mon, 17 Mar 2025 22:24:53 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-jdk-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:bce729c42cccc08b156e61740ae68e0d9a923cfe715a50229bd6b847a65e1869
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318882861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195d580572429bd54dd50b1a521fe345c8ca1ff139c4243b7dbb561f811a2fb4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 17 Mar 2025 22:24:25 GMT
SHELL [cmd /s /c]
# Mon, 17 Mar 2025 22:24:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 22:24:27 GMT
USER ContainerAdministrator
# Mon, 17 Mar 2025 22:24:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:29 GMT
USER ContainerUser
# Mon, 17 Mar 2025 22:24:30 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 22:24:38 GMT
COPY dir:3bbdecdaf44fd794a45fa39cf7b31efe4cc2d91c5e3e7c4c5333407317959149 in C:\openjdk-25 
# Mon, 17 Mar 2025 22:24:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 17 Mar 2025 22:24:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d092fe629d718380947d24acac5383c7cf7ff4acf0ff66bad60144f1b50b5f`  
		Last Modified: Mon, 17 Mar 2025 22:24:50 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398195166db260660e3c046850c8220bf8b0cc9ad5651f3c0f1a26e87cc464b8`  
		Last Modified: Mon, 17 Mar 2025 22:24:49 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d4815f02e9dd52421d238b3b0238e78d462229d3ba722a6bff3a36d622c520`  
		Last Modified: Mon, 17 Mar 2025 22:24:49 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e535147cd0916d53a51400fa36e43b0704112704bcd958fab9caf73735f3a2e`  
		Last Modified: Mon, 17 Mar 2025 22:24:49 GMT  
		Size: 68.7 KB (68666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d35055e45c1c777718d278258806e7c7dd442880920995cb61e404fc27d6b0`  
		Last Modified: Mon, 17 Mar 2025 22:24:48 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fca2129a31eed04da43d86f3b211d4ae862409b425ec16155b874219ff91e1`  
		Last Modified: Mon, 17 Mar 2025 22:24:47 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae266edb8e048d818618639a49be880a0875c5d3da1bb14ffa566d57fd62da`  
		Last Modified: Mon, 17 Mar 2025 22:25:00 GMT  
		Size: 207.5 MB (207469646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833d018d62c4854a8fb40641363de6df9248b49e7070bad1136e8913ecf62fe6`  
		Last Modified: Mon, 17 Mar 2025 22:24:48 GMT  
		Size: 4.4 MB (4430628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6e137b9515d90e6b98b1760548a809b67690d1db02ffd11a5fb50614e23897`  
		Last Modified: Mon, 17 Mar 2025 22:24:47 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
