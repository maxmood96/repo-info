## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3eac41c3f71fb6bec22a4642521f4982fe67fc1356428ee4ca56fd65ec998ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:fd34b69b3b9ccf1812130ab0c8c2e7b7e43ef871ffd456fdcc6bb09112b4f88a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310076032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532e1c1012782ba8bf89078258abe8f101784a89d0bfadc5a682d31e19dcb364`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:12:53 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:12:53 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 14 May 2025 21:12:54 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 May 2025 21:12:55 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:12:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:12:58 GMT
USER ContainerUser
# Wed, 14 May 2025 21:13:06 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Wed, 14 May 2025 21:13:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:13:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318ac79855801726a8e41119b0fe9c1dbc536468a9eaf55017ef54a40bdacdc6`  
		Last Modified: Wed, 14 May 2025 21:13:17 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a052d73ce6c1da2c39fa95a954c042204166e307d4f6c03f8c0292b5709598d`  
		Last Modified: Wed, 14 May 2025 21:13:17 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36460887c48b2b239652e1beeb346d038483dcd181a8c219602139c9638941c0`  
		Last Modified: Wed, 14 May 2025 21:13:17 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1dd4a3b827e3bffd80ef4956d02abc50dba9f0511343acdc10e00311aa914`  
		Last Modified: Wed, 14 May 2025 21:13:17 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747412b20fc4ec9fc270c1edf1e40021b280f8cf8f4fa9f66749ba8c5a46581e`  
		Last Modified: Wed, 14 May 2025 21:13:15 GMT  
		Size: 76.7 KB (76664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693764ba449949c6b8c3649471c419a402a49bc8fa01058f4afdb6d48c7b135c`  
		Last Modified: Wed, 14 May 2025 21:13:15 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378ee30b6ccd4091d754e09a1d9cce2de2eb205490ead1eb3f0d05736bf22f42`  
		Last Modified: Wed, 14 May 2025 21:13:26 GMT  
		Size: 187.3 MB (187309236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528435d4a21dcb087880e233559871f50186cc3cdc36f51fb335f086d473ebb4`  
		Last Modified: Wed, 14 May 2025 21:13:15 GMT  
		Size: 107.3 KB (107266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c084c2d0491af09a194fb9fc55a00f4451d42f592804251dd676a1611da4703d`  
		Last Modified: Wed, 14 May 2025 21:13:15 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
