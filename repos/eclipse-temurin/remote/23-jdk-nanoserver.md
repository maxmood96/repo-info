## `eclipse-temurin:23-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:952f722f934f93b542845baf403f606cb4a34727f6c0ff40784f882d5a77e872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:23-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:7c4fe25d70b13040b2685ad29c01fcc4b512fdf3774269c60a9f1e8f80839f3b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.3 MB (408262296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa85f47b9e63f3c9465e9b782e69ecad8253a273c48ecfc525992878a5e0664`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:17:27 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:17:27 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:17:28 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:17:29 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:17:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:17:32 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:17:39 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:17:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:17:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6b5f40b86f9fb30a774131b42f8beb4b7c5e87a57f06add607abf865b77fed`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d334c3db862cca288884361979938e08f15480be833ff7e6d72643b3ad1f49`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5f1f35d30850044b66dfe9aa006b2e5d31ee2d1731397d2df63585bda5039a`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb6d7983e1878a19431f28973091b40dbe740310b4edbc14272b2de6778426`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130cd2a93fade2d3e9b6ad1386174c725bfd86b343a54f7ed2b37b6d2720b96`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 79.2 KB (79247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87790e4b98bcb47113e24effba4c67cea60e01984ae96245d0498f77545f0d76`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d853ab627528bf0a6fcf87423d9b25bbf6a73440efd5fa65b01fd6146fcfa7ee`  
		Last Modified: Fri, 31 Jan 2025 02:18:02 GMT  
		Size: 209.0 MB (209029316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45da4b2bca5cee38d1b54febf841cd3c8d19f80f07ac07507437ccf03718f707`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 93.2 KB (93181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c31975bd0aae60c12d932b92916e1b472f79899a3ff0817f54984fe4b79b71e`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

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
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b8a93df5ec96a3670c2536704a0ec50639dac53102b8d3afa1061c6fa8e122`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745333a68259cbda4596140625eff4a4d3a422f08e702be9ff2dd49346af12e1`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd4fbba5085fd5a946947e49e5d6138df155aae84d933d0783ecf2b85adbed7`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcc891fc798f55a2ba237435803bc7c5b985ad9c97fc8da916d7704a5c29db1`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55afeac324966cec80001e2d92d21f07f55dfdf1af83744fc523066cb6d24841`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 78.6 KB (78644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49ec7e86448470b4affea16a3f9bb08e315b276ed349e9a9c34a1b39b026a3e`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78d9aec8f646b95252dca283235b760661ca2009154d92fff1a51a01df97d15`  
		Last Modified: Thu, 13 Feb 2025 04:16:25 GMT  
		Size: 209.0 MB (209028211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccf6ac2788fd952fa4027dd0360fe2bc634acb370d79befe96a0e05e43794fe`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 106.6 KB (106619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce87ea8a492ad550bb5be6ad200be140e324e2c14aaf8d3f7d806eacf5147232`  
		Last Modified: Thu, 13 Feb 2025 04:16:17 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

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
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af165d2201f27c3c8ecd13eb740ce23daf2453f85f11afd3cd2b21d35718ffd`  
		Last Modified: Thu, 13 Feb 2025 04:16:16 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f0d11e89d655d0ba9d17eb00dc3bcc98840b9588ab2c448224d69153604ccd`  
		Last Modified: Thu, 13 Feb 2025 04:16:15 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72e7d4e50899022aa8e3f9d04ec97d824b637643b439d9adcc06eeda1d1b24a`  
		Last Modified: Thu, 13 Feb 2025 04:16:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080bf397bd8dfa8b1b6f320bff1642300aeac098cac839f395bb54cf26c64516`  
		Last Modified: Thu, 13 Feb 2025 04:16:16 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570db502148469282b33667cdddb0b156449523abe14dc3924216d6fe1367804`  
		Last Modified: Thu, 13 Feb 2025 04:16:16 GMT  
		Size: 82.9 KB (82899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e02d23a2590ec484479fbdd6162f8792390868e97cdd1920d7b14701c5be2`  
		Last Modified: Thu, 13 Feb 2025 04:16:16 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ec605d14a9e573b337d368554c4c27dca084bfc9dbacc1ffeca4c4986bfd8e`  
		Last Modified: Thu, 13 Feb 2025 04:16:30 GMT  
		Size: 209.0 MB (209027463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3627b76c6ce75bd294568c8a3e7a3c6e534109219e88a3b8c7962fbcc4c3c6`  
		Last Modified: Thu, 13 Feb 2025 04:16:16 GMT  
		Size: 4.1 MB (4135511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06867a1c9b4769674d25add14ec06fc8e4233b615fd9a220c647178eb4df11aa`  
		Last Modified: Thu, 13 Feb 2025 04:16:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
