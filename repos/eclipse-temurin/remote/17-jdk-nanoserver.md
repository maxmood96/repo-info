## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7d0368c2a0d2e5e11fc780083c2e4fdc629f267c695b73068de25062a7498ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:cc3f10b9d090495ef9fba8debb657df8992cd01de56e5e23f52ee1f3a81f3041
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378910849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d112168e6c27a6f2659963aa1ef26a8b9a811d2ee59e14b3a2314da057bc3f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:00 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:02 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 14 May 2025 21:14:04 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 May 2025 21:14:05 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:11 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:20 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Wed, 14 May 2025 21:14:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:14:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d6b9a96e5ff7cc0cf5b965e710a2c82df56be17a5dc508db8dd1d1bd6d38e9`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0d044b65fab6b1efc0f6f0d8f58f8b765d70f50ae8e65182b8c456d5acea2d`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc659115d4b46d8c49d5c3e0ad86c424ec3b7462753cbf8b5a7856fbd596cb1`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d18067d3bac9f8c29ba7847697208cdcc925fce4475a5206c653e42f784a4`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79dc294f09b66f0e7c4d0d161159a76381ec6d28769a39885a6291c27a3e351`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 77.9 KB (77917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49caae00fd568c3b4738ee75c61b23666f3265ae3cfa7caa85b82594c2e92f07`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318d339a5f098692f576fbe37cb646baef072ef05ea962809645e914ac14c46`  
		Last Modified: Wed, 14 May 2025 21:14:44 GMT  
		Size: 187.3 MB (187310232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b843262cb961ccdad232f7f858b78601e87e0719b7d616ec3b9358fb51af1e93`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 104.4 KB (104444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524e56621313becf168498234dfa18d36e46c83dfab902ea14dedd90c553c3ed`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.3692; amd64

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
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a052d73ce6c1da2c39fa95a954c042204166e307d4f6c03f8c0292b5709598d`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36460887c48b2b239652e1beeb346d038483dcd181a8c219602139c9638941c0`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1dd4a3b827e3bffd80ef4956d02abc50dba9f0511343acdc10e00311aa914`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747412b20fc4ec9fc270c1edf1e40021b280f8cf8f4fa9f66749ba8c5a46581e`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 76.7 KB (76664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693764ba449949c6b8c3649471c419a402a49bc8fa01058f4afdb6d48c7b135c`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378ee30b6ccd4091d754e09a1d9cce2de2eb205490ead1eb3f0d05736bf22f42`  
		Last Modified: Wed, 14 May 2025 21:13:26 GMT  
		Size: 187.3 MB (187309236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528435d4a21dcb087880e233559871f50186cc3cdc36f51fb335f086d473ebb4`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 107.3 KB (107266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c084c2d0491af09a194fb9fc55a00f4451d42f592804251dd676a1611da4703d`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
