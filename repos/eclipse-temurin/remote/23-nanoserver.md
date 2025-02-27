## `eclipse-temurin:23-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a6d9254bb9b4f8ff9ad002f7cbde11ebcea1d62e5cf483c1273b7b26a225c494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:23-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:b6ab76cca4343180a24dcfecb8ae057b51924372890192186051f6da72df115c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329886337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d6989b7fd5d645c0545293068c4e2fe6e09f8c827463c7c1e83f5f5052d6e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:40 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:40 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 13 Feb 2025 01:18:41 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 13 Feb 2025 01:18:42 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:18:45 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:54 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Thu, 13 Feb 2025 01:18:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:19:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b8a93df5ec96a3670c2536704a0ec50639dac53102b8d3afa1061c6fa8e122`  
		Last Modified: Thu, 13 Feb 2025 01:19:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745333a68259cbda4596140625eff4a4d3a422f08e702be9ff2dd49346af12e1`  
		Last Modified: Thu, 13 Feb 2025 01:19:03 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd4fbba5085fd5a946947e49e5d6138df155aae84d933d0783ecf2b85adbed7`  
		Last Modified: Thu, 13 Feb 2025 01:19:03 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc891fc798f55a2ba237435803bc7c5b985ad9c97fc8da916d7704a5c29db1`  
		Last Modified: Thu, 13 Feb 2025 01:19:03 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55afeac324966cec80001e2d92d21f07f55dfdf1af83744fc523066cb6d24841`  
		Last Modified: Thu, 13 Feb 2025 01:19:02 GMT  
		Size: 78.6 KB (78644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49ec7e86448470b4affea16a3f9bb08e315b276ed349e9a9c34a1b39b026a3e`  
		Last Modified: Thu, 13 Feb 2025 01:19:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78d9aec8f646b95252dca283235b760661ca2009154d92fff1a51a01df97d15`  
		Last Modified: Thu, 13 Feb 2025 01:19:14 GMT  
		Size: 209.0 MB (209028211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccf6ac2788fd952fa4027dd0360fe2bc634acb370d79befe96a0e05e43794fe`  
		Last Modified: Thu, 13 Feb 2025 01:19:02 GMT  
		Size: 106.6 KB (106619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce87ea8a492ad550bb5be6ad200be140e324e2c14aaf8d3f7d806eacf5147232`  
		Last Modified: Thu, 13 Feb 2025 01:19:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:8f04df5e9812916948b179d307bfbac36eb0bf222be5246060cd455e61fdaa5f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 MB (320167648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb440f9f3f6f04ce901322844879517e782afe9e1e3bb658a7bc1b49c6fc7414`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:16:45 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:47 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 13 Feb 2025 01:16:48 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 13 Feb 2025 01:16:48 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:52 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:58 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Thu, 13 Feb 2025 01:17:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:17:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af165d2201f27c3c8ecd13eb740ce23daf2453f85f11afd3cd2b21d35718ffd`  
		Last Modified: Thu, 13 Feb 2025 01:17:10 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f0d11e89d655d0ba9d17eb00dc3bcc98840b9588ab2c448224d69153604ccd`  
		Last Modified: Thu, 13 Feb 2025 01:17:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72e7d4e50899022aa8e3f9d04ec97d824b637643b439d9adcc06eeda1d1b24a`  
		Last Modified: Thu, 13 Feb 2025 01:17:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080bf397bd8dfa8b1b6f320bff1642300aeac098cac839f395bb54cf26c64516`  
		Last Modified: Thu, 13 Feb 2025 01:17:09 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570db502148469282b33667cdddb0b156449523abe14dc3924216d6fe1367804`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 82.9 KB (82899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e02d23a2590ec484479fbdd6162f8792390868e97cdd1920d7b14701c5be2`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ec605d14a9e573b337d368554c4c27dca084bfc9dbacc1ffeca4c4986bfd8e`  
		Last Modified: Thu, 13 Feb 2025 01:17:19 GMT  
		Size: 209.0 MB (209027463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3627b76c6ce75bd294568c8a3e7a3c6e534109219e88a3b8c7962fbcc4c3c6`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 4.1 MB (4135511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06867a1c9b4769674d25add14ec06fc8e4233b615fd9a220c647178eb4df11aa`  
		Last Modified: Thu, 13 Feb 2025 01:17:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
