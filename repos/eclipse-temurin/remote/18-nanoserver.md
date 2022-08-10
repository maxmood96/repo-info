## `eclipse-temurin:18-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2d4d55e18771b106e5171a5ab521a93251478df1ed60d1545d4095dfea52edcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:18-nanoserver` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:d78009058be1aeb24c83464b9c0e572e19062cd7f093c730288ec503ad5d2343
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304814445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c9957c051690d4565bb8bb81b9d9723aca4082a88b21809d3a109de6db8f67`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:33:50 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 16:33:51 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Aug 2022 16:33:52 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:34:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:34:04 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:34:19 GMT
COPY dir:fe0d9ce398e3d169055678c6642e68d763dc7a30e25c08274ab6c7ec599f7aba in C:\openjdk-18 
# Wed, 10 Aug 2022 16:34:33 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:34:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f13999e9467c86cf2ef854733e78081046c1b26eaee3ab579f32308a22ad3f2`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984aadb5c294a031eb9bf139e089a14953bfd160b9e3fb63c5407283f238f4b0`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b8e890683ee09a276afb5655197ed4536d7af93add242ec3ef49a79370b553`  
		Last Modified: Wed, 10 Aug 2022 16:50:57 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0017fc6b7e0fc882e7f2169bdf28cd916bdd5becfc60b3660f256cd4bdeb7f`  
		Last Modified: Wed, 10 Aug 2022 16:50:55 GMT  
		Size: 84.8 KB (84820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5484fbab0fb42fe9cd48851c5207ac52537278b619798735df6ce414ff445b`  
		Last Modified: Wed, 10 Aug 2022 16:50:54 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a183a1fe7904ad9094916997034bb713236ea12492576d6391c4d969fedff4`  
		Last Modified: Wed, 10 Aug 2022 16:51:13 GMT  
		Size: 186.6 MB (186571395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f481a0e3b0201a728db3d7ec94d4aa08f5a62bd78682a9264e21ebae6e2a38f`  
		Last Modified: Wed, 10 Aug 2022 16:50:54 GMT  
		Size: 62.8 KB (62795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f40c8235aaff932ddb56d70d6f332c2d4e8ef552bd75f2ea282bd021cf968a`  
		Last Modified: Wed, 10 Aug 2022 16:50:54 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:18-nanoserver` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:b3d6ba4620e73d7f822f1d9e6043e816f54219d23a4ce872fc2c91ddcf2847a0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293393948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5216b9afa2fb24792b48e2b71621b38ac7b8fcf93f22bba5d9121ad09495857`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:23:45 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 16:23:46 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Aug 2022 16:23:47 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:23:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:23:57 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:24:10 GMT
COPY dir:fe0d9ce398e3d169055678c6642e68d763dc7a30e25c08274ab6c7ec599f7aba in C:\openjdk-18 
# Wed, 10 Aug 2022 16:24:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:24:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b77c03a9a9dbcc9a7ce04d7ab0b4e19a43c3c215dd1fbcbccfa8b99441f7b4`  
		Last Modified: Wed, 10 Aug 2022 16:47:11 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f3461283188f5fe78ba7b0be84df6da7face268c80e8fb2cd24af9d4cd2ba1`  
		Last Modified: Wed, 10 Aug 2022 16:47:10 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15327e487f857893b0188f60c77476725b0c95a54b2bb662bb16b85228d87825`  
		Last Modified: Wed, 10 Aug 2022 16:47:10 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcc603f19994408c0f57ba9ba4c5d501dd3dc2aeb86208e0b8f8397454c0c60`  
		Last Modified: Wed, 10 Aug 2022 16:47:08 GMT  
		Size: 73.2 KB (73226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c294176c6badce0e1cc6e2bda845443033039aa5dc57470b0bb307f817f2551c`  
		Last Modified: Wed, 10 Aug 2022 16:47:08 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2291e532b264206697c2a264f7aa0aa0d59f997e6b932fccd92f658d0af639`  
		Last Modified: Wed, 10 Aug 2022 16:47:27 GMT  
		Size: 186.6 MB (186568962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9ee7845cb67a01b518ca9de8e57dafbbabf3b37fd16a3aac7e85bfae70bab1`  
		Last Modified: Wed, 10 Aug 2022 16:47:09 GMT  
		Size: 3.5 MB (3540667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b5a7a3c7a9de665295544c26fed1c90438eff1481e9985576e390f10f11fe9`  
		Last Modified: Wed, 10 Aug 2022 16:47:08 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
