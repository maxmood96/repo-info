## `openjdk:25-ea-20-nanoserver`

```console
$ docker pull openjdk@sha256:151bffd5562e3205d1b5f0a054d827d78f6df73fbf8f87a53b6d1dc64f9058dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-20-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:b20ab4a597f7b08e791a6d7fa55ad618a28986f79528107566436987828b5609
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398040733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99728cd51c65c618edef6e9f46192ea40a72f6bf46206035abba983c50147d2c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 25 Apr 2025 22:14:47 GMT
SHELL [cmd /s /c]
# Fri, 25 Apr 2025 22:14:48 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 22:14:49 GMT
USER ContainerAdministrator
# Fri, 25 Apr 2025 22:14:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 25 Apr 2025 22:14:54 GMT
USER ContainerUser
# Fri, 25 Apr 2025 22:14:56 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 22:15:04 GMT
COPY dir:68bac63248f06b5a3c6e48fd170d3fc54c730eec81f70554d15d79ed34fe2288 in C:\openjdk-25 
# Fri, 25 Apr 2025 22:15:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 25 Apr 2025 22:15:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409753cc488778a144ea889ab925b5f1dff516978e08fbe9c52d81982582d6d`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0f99f9f47d40ea27110b026a8d73e0f1430f52d1d4434cb962039d03da16f9`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead629dd28e5e2f8ddeaf6ae93b77d89b654633e389c29ce8b89bc7ab70a9b2f`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa9addc5c1eb495649cc807749c979bd6aaff2c92c06018bde9242cc11f9039`  
		Last Modified: Fri, 25 Apr 2025 22:15:16 GMT  
		Size: 76.5 KB (76458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cd81e099bdc16f2b5929df8cab02ce0e664658e3b8e7a64cd6aeb39e7c842e`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f2aa70ed50683ef643947a4548209b9cee999c8dc764bd7c8a1561253bea8e`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155e71e7f9e46ec99067356184c56b796230bc429a09d6a19fbf76c863f83d6d`  
		Last Modified: Fri, 25 Apr 2025 22:15:26 GMT  
		Size: 207.7 MB (207700888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4486d3da245c08502bb741757a4e7e1f7569f2336b933eec5e1bc726b7f072`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 115.0 KB (115016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2854f7f82e74fb6da9c502068f8ed90419e2f48232870fa4f4c05b793ed449`  
		Last Modified: Fri, 25 Apr 2025 22:15:15 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-20-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:7590750fe75adad48d7e868b8685b0cee72c3f76928234540af7d64ba69bc6eb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330406836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372efeb6ac181b2662ca3d4e1b6edaab30a3931af7521cbb5e7992c5bea710fd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 25 Apr 2025 22:17:38 GMT
SHELL [cmd /s /c]
# Fri, 25 Apr 2025 22:17:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 22:17:40 GMT
USER ContainerAdministrator
# Fri, 25 Apr 2025 22:18:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 25 Apr 2025 22:18:04 GMT
USER ContainerUser
# Fri, 25 Apr 2025 22:18:05 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 22:18:13 GMT
COPY dir:68bac63248f06b5a3c6e48fd170d3fc54c730eec81f70554d15d79ed34fe2288 in C:\openjdk-25 
# Fri, 25 Apr 2025 22:18:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 25 Apr 2025 22:18:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e05e297e8ed2009fcd69b67d982c8b8f4c4385ee29e281cfa10cb04543cfd9`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aec49f736c308cbe381bf2fc6415cff88e17dc2e607551ac7171c76614c767`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c7a0816d3c5ab9daaae4419402bd9a202720d4c502d2248834edf750daea77`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8281d9aa4cb23b895af0113dbba423e846c2a4bccd4ffbab5a8d460435d5331f`  
		Last Modified: Fri, 25 Apr 2025 22:18:27 GMT  
		Size: 72.3 KB (72314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1ab1b8f67e8389d42b606f3702188f27d096f22a912097d17893d30c76ea30`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f15b31a8db2208fb66f1f08ac72c12e6d2dbb74e75564adf2f526babb0940b`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63324c1474e13803e8f64d0a0779f446efe8b73824293391aff1108b8354c96`  
		Last Modified: Fri, 25 Apr 2025 22:18:37 GMT  
		Size: 207.7 MB (207700807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dc5cdf3ac63db31398210e9abd7d12eb8799de63e584b619328b724fa3c9e6`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 88.5 KB (88452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b056dbe8f46591a25b812821e0f61eddf0aeb401bbaa85ecb8dce98e74e42a49`  
		Last Modified: Fri, 25 Apr 2025 22:18:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-20-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:c422d62d23a367e3db494571eb42614bcf4f9f404619a22a6991a27bf729f3f8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320886455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da393a71d1888952b8e5b00dc1a53674ec2a297d3767046b9ef0af5c4cc3e752`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 25 Apr 2025 22:16:38 GMT
SHELL [cmd /s /c]
# Fri, 25 Apr 2025 22:16:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 25 Apr 2025 22:16:40 GMT
USER ContainerAdministrator
# Fri, 25 Apr 2025 22:17:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 25 Apr 2025 22:17:01 GMT
USER ContainerUser
# Fri, 25 Apr 2025 22:17:02 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 22:17:09 GMT
COPY dir:68bac63248f06b5a3c6e48fd170d3fc54c730eec81f70554d15d79ed34fe2288 in C:\openjdk-25 
# Fri, 25 Apr 2025 22:17:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 25 Apr 2025 22:17:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4124e28a2a84c691d98069fd4db717fb9f662ef91e62ee2368f5e3a2d36b6e2d`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4371229a096d4b461b2835dc2475cc1209d0ee06121fc6c98a3049b1e6631bb`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762469014b03799043b4eaadf732e0c53db37928faebfa5e249f7d9bea79ce9c`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b1ab208e5df793b1e52d074b57d8fa317786a78f36ba5afe019ef25f82c5bb`  
		Last Modified: Fri, 25 Apr 2025 22:17:21 GMT  
		Size: 68.3 KB (68301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113dbddb03b847a01262ccf7d870307c5e743a317ab502d26f384e6ee12addac`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2326e7bd1a74ca5ee071f27a498759857ba18b4098fb8726cdcbcc1a443d628c`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512a99d0df04a385ce7dbfa73418d7be09dab45faf4be268942817a1fe444526`  
		Last Modified: Fri, 25 Apr 2025 22:17:31 GMT  
		Size: 207.7 MB (207700826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96991270863c6a793cccd5f9ec418bf4f77dfe5175bd73bff0caf0c7358445f8`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 4.4 MB (4358473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c05f6048f5485de612fb39fed95bc4ff45b408a445a995a94631c496e1aab18`  
		Last Modified: Fri, 25 Apr 2025 22:17:20 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
