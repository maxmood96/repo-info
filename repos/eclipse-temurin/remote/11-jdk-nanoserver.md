## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:066d40625da732e68854fdb9d9a263c25c2356129154e0b35ccdede4b3210fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:cd99a994a9edbcc5fbb5d1fec5f36f82b7d26b985eedbd13a19a47555fb659cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.9 MB (394914240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751ed1009df585972eccd37e899e5ab77fffb5975f8dc75da6999c1638a9c283`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:35 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:35 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 22 Jan 2025 19:34:36 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 22 Jan 2025 19:34:36 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:40 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:46 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Wed, 22 Jan 2025 19:34:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Jan 2025 19:34:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025deb4acd18fe013bb7a99aa496a09e4a7fd186f5239655669d0a41a58f1e38`  
		Last Modified: Wed, 22 Jan 2025 19:34:57 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbc14cf4c9e6ad2c077406ab79b61b5fa8f7f3f458e54766ea5e93d910d2a04`  
		Last Modified: Wed, 22 Jan 2025 19:34:56 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832abaa20689d4524c047e3876a96854db8aad582b31077d3c777730a920bf96`  
		Last Modified: Wed, 22 Jan 2025 19:34:56 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1719de8f7bd72623fd85ac15cf75e58d73c41d59bf1314a962fb48582b6772`  
		Last Modified: Wed, 22 Jan 2025 19:34:56 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df255a2ed981b14f005766e2fca791a18a8a54937c6d2ac84c824fd80fecad`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 76.3 KB (76252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f9390f0d6312d4cf9034855d97527b692c956804725df6dba8cf3f55ae8a7`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebef3241164c48e8c3977f46353d0d9eef860df5330a9b57ac2439605c90d81`  
		Last Modified: Wed, 22 Jan 2025 19:35:05 GMT  
		Size: 195.7 MB (195673028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97796a264a7e6e42a51fc64185038a76ff78347b1a969014afae5b4b20db7f00`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 104.3 KB (104320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4779daeb1dadd97090f52cd63869cff0cb7a9786121ec8e7f0a90f1e626023d1`  
		Last Modified: Wed, 22 Jan 2025 19:34:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:8cc2a0bb354506a764c5578ea805bdefd6f0b7af47df9c71a886acdf0cf215a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316522482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2510b8067ee2c213d60293467c28afeb7bc78e5d2dcf7fb5cf86aa1d23d3ec1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:01:27 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:01:27 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 15 Jan 2025 18:01:28 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2025 18:01:28 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:01:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:01:31 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:01:37 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Wed, 15 Jan 2025 18:01:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 18:01:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd27b4bca88b469c1dc025f141b3dd658e30681c371beb6357ba75bf79d0e9e8`  
		Last Modified: Wed, 15 Jan 2025 18:01:49 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa979c1cc087667c763b0031baf4ee6aa8edfb452b7828c57249069b863e2ff`  
		Last Modified: Wed, 15 Jan 2025 18:01:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d810f24adae91c5e56b1cae9d91cee28dd1801fd3a5bc186c8d9eec3f6687424`  
		Last Modified: Wed, 15 Jan 2025 18:01:49 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae5b68d6ffd80d31b496de04030f00c491e802d897c992b24418d3fa19b8249`  
		Last Modified: Wed, 15 Jan 2025 18:01:49 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23626ac79653bacb5c7e9c4bb2801ea6bf977830933adaa18247d56a3da0b51`  
		Last Modified: Wed, 15 Jan 2025 18:01:47 GMT  
		Size: 76.2 KB (76206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf13a01927b7d722439abf5dddea850ce1021bf63e868b7eaf836ee9d7cefe2`  
		Last Modified: Wed, 15 Jan 2025 18:01:47 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740250c7319a4c5d4513086ec5e4d254fd903c402996096e7e79e68befa72114`  
		Last Modified: Wed, 15 Jan 2025 18:01:57 GMT  
		Size: 195.7 MB (195671439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f982188cb7fec9b6261892ea8dcfebd8d0dd454bc9e0d84ad03683e575c80a`  
		Last Modified: Wed, 15 Jan 2025 18:01:47 GMT  
		Size: 107.1 KB (107106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92c6c4befae9064c1f6aa60491eaa7508b32052d33efa8ecb1190f808cb76aa`  
		Last Modified: Wed, 15 Jan 2025 18:01:47 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:3038cad1684dacecc295fef423a4e45232c045f9b37ee2c44c64ab2ac90a9ed4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351130035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0272b483cd10f261642b72a818691d14ab938db561df2c2b343008e5bb4ab913`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:00:02 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:00:04 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 15 Jan 2025 18:00:04 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2025 18:00:04 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:00:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:00:07 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:00:14 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Wed, 15 Jan 2025 18:00:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 18:00:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d77a62b0d5777ecd9b8a52b046c6887302c612feda8a86cbb9c9f51dec4b99`  
		Last Modified: Wed, 15 Jan 2025 18:00:23 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9ab9b443a0c19f4c542724f521183c7f00068420d651e426b69676f7f40fed`  
		Last Modified: Wed, 15 Jan 2025 18:00:23 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554d63937f901c33c52f5a5af18f48485aee9ae0feb0b0de922f47aca9d1429a`  
		Last Modified: Wed, 15 Jan 2025 18:00:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7e5655aba20dfacaeb1a744da498cb40baceb3b1d3398e63422a14e569a44c`  
		Last Modified: Wed, 15 Jan 2025 18:00:23 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33152816e0ab8452d71674ff525c39e5054cd034680b51d23c503aecf362f33`  
		Last Modified: Wed, 15 Jan 2025 18:00:22 GMT  
		Size: 75.5 KB (75473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02760dea4da72f80a392efa9bdcd1dec1947e376331f71bb524a7317a412403`  
		Last Modified: Wed, 15 Jan 2025 18:00:22 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfcab81f0cb0a10d725cedfb2842b57b11829cb5ddefe698d4f3b357c3ba32f5`  
		Last Modified: Wed, 15 Jan 2025 18:00:31 GMT  
		Size: 195.7 MB (195671960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f938a52b0dbda8e73032d5f66e0673b88a1680f47cdc4d12156aae59f53c3ef6`  
		Last Modified: Wed, 15 Jan 2025 18:00:22 GMT  
		Size: 108.8 KB (108804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3a91038415cae8d6aac39734f741770b4139ab477b335448de9e6fe20f2810`  
		Last Modified: Wed, 15 Jan 2025 18:00:22 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
