## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b3e8ec27018bcb2c683f4577d09e0c3500db2629b1c225851ec8bd294905c240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:0089d380f18922116c76b44d70342672558f3afabdf97418759a6cf6663065ad
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315221562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c5541bf2d59f739d2c128fe5b4f3fb7b886ac99a2c960d840c9e6bd638bf4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:23:58 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 24 Apr 2024 19:23:59 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Apr 2024 19:23:59 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:24:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:24:11 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:24:27 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 24 Apr 2024 19:24:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 19:24:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2193f7233ee9ca7d1dda364e716073831621842dd832deb8f3c69021aa9d6334`  
		Last Modified: Wed, 24 Apr 2024 19:46:46 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1727b617a83ee4a6ad51740f7c297bf8f286e72a3aaad5a45fc7a5ff594d9f2`  
		Last Modified: Wed, 24 Apr 2024 19:46:46 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6589479c4d6064b58314b90fbe097b165dfe7c0bce69f14eb48a896cb9d2e0`  
		Last Modified: Wed, 24 Apr 2024 19:46:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc05e4667a98baef0dbcc6e71d46c018dc80e22b83a3e32435c2063c1ec507d`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 76.8 KB (76791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c3360e9b88abe16f00f54eb59d334aedf61e54d3fa3776751aea8e2fb6a73b`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b930dab2b7897785c835ff84cb9f42d45edfe677606da0452d0022195c6683`  
		Last Modified: Wed, 24 Apr 2024 19:47:02 GMT  
		Size: 194.1 MB (194083519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e422cb81c1d8c70dc848b8ae0bc1e0c2031e835ee125163b9dfac27e9ef7f8cd`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 61.2 KB (61211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6331fe34cbb0422b7e33e9467b9a5d91245d68fa7a5c09fa4166d54c5d7d0b`  
		Last Modified: Wed, 24 Apr 2024 19:46:44 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:f5dfc975fd2433073becbc9427f88b5756431c710f6a121b87fcdd2e9da74854
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299132824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79fd1705c45b8bbb9934cd9f6102d6248745a0370da177aeb12d240ab17d9ad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 18:41:40 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 24 Apr 2024 18:41:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Apr 2024 18:41:41 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 18:41:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 18:41:52 GMT
USER ContainerUser
# Wed, 24 Apr 2024 18:42:09 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 24 Apr 2024 18:42:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 18:42:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73dd9de1f4ee2da0931c1efc7e007a79d522de315970bd4907f8c25164b4031`  
		Last Modified: Wed, 24 Apr 2024 19:36:04 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7f2c5227d7bceac1a1244abe9f29e1b98f10b958eb2e11d13368d8d4a1015`  
		Last Modified: Wed, 24 Apr 2024 19:36:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc4b0d14ed0bfa53e3fc8ed4b1fcd11a8044f1787b20c50741d17b5f8b62ca8`  
		Last Modified: Wed, 24 Apr 2024 19:36:04 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8591bed2b34e6566a4509056ef1b7ce711037fd180b7805c456d83705454a6`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 66.9 KB (66856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5127635c315d87e10a1285051f1aac1cb26539824ae9224bcb54a542a1e1faa`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e0670c91bff7268ee61dd4cc4f8bc88a79a8cb7b8b10d095f8b445eb10eb3`  
		Last Modified: Wed, 24 Apr 2024 19:36:20 GMT  
		Size: 194.1 MB (194084434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e577d90cbcf65ce6e9f87955d46e7c08cc81c277e126f9618ebb49c1fd2d70`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 85.5 KB (85477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eb4157d4521d11f623e392ef3498109d9504a5c4b5039910f2d4d9f1741ee6`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
