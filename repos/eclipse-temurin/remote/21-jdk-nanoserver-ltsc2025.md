## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ef767c3cad38f6e863992b8193454ce8b9c618f06fd9bc5c05d7b8cba6afc23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:884dfc0a7f56de016fa1c2970db77859de78a4d9fbebbccf71ad4b078e395efb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.4 MB (395393510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd06ee821fbba10ac23dd0f59fe0ff73838799e4bab97bf8865244e1b01dd14`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:19:45 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:45 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Wed, 10 Sep 2025 22:19:46 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Sep 2025 22:19:46 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:50 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:58 GMT
COPY dir:a3fe1d88014e165c39b52565bb4587e5a787fc090e6660a0edced9167c6512ac in C:\openjdk-21 
# Wed, 10 Sep 2025 22:20:03 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:20:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879f436d837a2b288893b482e02b87f8d8f98f0f4343ff630a85352370cc334`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea347919ad67858602c006e12e1cf532c2aff2a50ee5897ec50a8ec43507dab`  
		Last Modified: Wed, 10 Sep 2025 22:20:54 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33efc8c2e7c922e361a26b9e89eb2173112ea22c458afc9028333be992cab2c`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b6b50c62bce22472fbada35a7b8d1d032717c8a64de6591ce232a9594b464d`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e972cc0a8d0c3af83d1cb5e52bab47f31f1b2c5b2e29c980394a33369f8774`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 71.4 KB (71443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4d1d3a6fefda51f1f7f779d2efb5649ae9aca08b6b3c659d1c5de3a64aea02`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a344efba588616d1d540b335cb4ecc161b7b3c0ec7c2d4e07ebc6f0cb001b`  
		Last Modified: Thu, 11 Sep 2025 00:16:36 GMT  
		Size: 201.7 MB (201671756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df062406cf9863a33e092c79609399de9cd6878e594d4da273dde16fd8f9ccfa`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f44de5f49856bf66b91af3649b62b1b7abd1e3ac0270cd16aa93ea0f053d81d`  
		Last Modified: Wed, 10 Sep 2025 22:20:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
