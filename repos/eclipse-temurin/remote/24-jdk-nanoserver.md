## `eclipse-temurin:24-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b17bea3ba08fcf1a324a039dfd060dcef00184ba48b22fbb3e345b754961139b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:a3bdd3e0797a67bbbec78d2c61b85b09959413d0ce311684e905f8f4e1b28044
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329644110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b294d986825891014411455c3ed74fc2cbf2da3c57c4d4e5ce2271f59b9f571c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:35 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:36 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Tue, 10 Jun 2025 22:15:37 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 10 Jun 2025 22:15:38 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:15:44 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:52 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Tue, 10 Jun 2025 22:16:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:16:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48143856f507f816971464e6e6b4136263f18cb2c5f54579a6cc7aed82dff6b3`  
		Last Modified: Tue, 10 Jun 2025 22:16:50 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e15fb0c18b6582994abe657c946cc4e1077c4607d40bca65cc8021ae926f25f`  
		Last Modified: Tue, 10 Jun 2025 22:16:51 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bb5bbd19a82e95c88a085fee615165085f4646e813e64f73031838eaeb8226`  
		Last Modified: Tue, 10 Jun 2025 22:16:50 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d7d3982e00378335596d4600795ba21fc62f0eca76cfbf84f886ffaabbe74`  
		Last Modified: Tue, 10 Jun 2025 22:16:51 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45563d5236808001a54f6bdce1ab22a6b2286b8747679e8b36ff5256fc17d7b3`  
		Last Modified: Tue, 10 Jun 2025 22:16:51 GMT  
		Size: 77.2 KB (77240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8326523d2a30ef29f1dd4d818b6ba844535ddbc61372faf23bd0110392043e5b`  
		Last Modified: Tue, 10 Jun 2025 22:16:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6827d493e23a0a4bb42eb9b76c60adcc1d075f2fd7cd14f8ef38744b4099375b`  
		Last Modified: Wed, 11 Jun 2025 14:30:26 GMT  
		Size: 137.4 MB (137364078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c0e845497bbe751de473918c9107062556a92da609dad32948f5d68cc3b4ce`  
		Last Modified: Tue, 10 Jun 2025 22:16:52 GMT  
		Size: 114.0 KB (113958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baad5dc5943bcfe291fd71b7f2f350e78e19a9420f41a1ed4a092a4b84bc0543`  
		Last Modified: Tue, 10 Jun 2025 22:16:51 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:bfaa50d011e8468998116d05e352dd44d9ad6c0cd27164611c37f659ac50f6a5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260098314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8ea7b477eee3aa6780722273795cc16e644fd3028d706907bfe130d9b996ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:20:43 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:20:44 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Tue, 10 Jun 2025 22:20:45 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 10 Jun 2025 22:20:46 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:20:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:20:51 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:20:59 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Tue, 10 Jun 2025 22:21:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:21:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8771e26c290070c650424f40cd3be0328be487630f97a29c164162e643b737d`  
		Last Modified: Tue, 10 Jun 2025 22:21:47 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0344e3e832699e656ac028b35f7eab6e5cdcdb8d4eedfde3126b4064536905b`  
		Last Modified: Tue, 10 Jun 2025 22:21:47 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef332c16492aeabeac9211b02211642e54164491b1cf0cf30f941b65d0fcd70e`  
		Last Modified: Tue, 10 Jun 2025 22:21:47 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4149e187e5ee29bcf3a2f82013d38460ce8be2f57ea9ff564babebcb7bbb28`  
		Last Modified: Tue, 10 Jun 2025 22:21:47 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48c7659916bfd05204c77e635c52b9095c6f746c023d7272efad8c8cfd90aac`  
		Last Modified: Tue, 10 Jun 2025 22:21:47 GMT  
		Size: 79.6 KB (79641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb884b60026ce0ff2cfa4c849924a7179e2ca9d7ebc92599b0ad9ebc5a588942`  
		Last Modified: Wed, 11 Jun 2025 00:16:26 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8d07f399c14be20d14059623163225a2a95ac2ff72dbd5133ba0d7d1e477e`  
		Last Modified: Wed, 11 Jun 2025 00:16:36 GMT  
		Size: 137.4 MB (137364258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfab01adf683bed7201f6f8366959992a95c35c654ab91bc929d3756a50e569d`  
		Last Modified: Wed, 11 Jun 2025 00:16:27 GMT  
		Size: 107.7 KB (107706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd561d7dc5f197d2a46cc1dbc4936666596df5398549be6d65b4c2d3c7d7cb9`  
		Last Modified: Wed, 11 Jun 2025 00:16:27 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
