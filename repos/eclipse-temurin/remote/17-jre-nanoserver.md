## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:94212365a64d0dbfa8cf0d739cc41e0dd684dd67f495ff42a3c3e9bbfe8e80a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:c6e9998c96c4eae369596dc68c16926a3b102ac73ae4d27a818bebe929da9b37
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242958213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6965c219ac6a486b9bb1e759838db0b02fdaf2f64a2fba1aafea628d1de4922f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:15:43 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:15:44 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 02:15:45 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 02:15:46 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:15:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:15:49 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:15:53 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Fri, 31 Jan 2025 02:15:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f1cfb1a515301c5d46cf52e997da0cd6b39b4931276bb0a8f949bf64df59b`  
		Last Modified: Fri, 31 Jan 2025 02:16:05 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361c604da3cd668ec671428558ab50f8041ccbabb3e2d701206ebe8fc4d2f82`  
		Last Modified: Fri, 31 Jan 2025 02:16:05 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8678fb2273aaea0e5d8b4a4d441519357db4ba2c0ed3d698c5f6d700b8da8`  
		Last Modified: Fri, 31 Jan 2025 02:16:05 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d357b54a9ccdeda6a0652b96b0af50cf040baf64894e289a3854b14b6c92f88`  
		Last Modified: Fri, 31 Jan 2025 02:16:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4868e4d22dcd0f4885ea20c49394df92ba867e8417b085cdec5b960b265e540e`  
		Last Modified: Fri, 31 Jan 2025 02:16:03 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf18df91fa4de25aa893064c380b047c7860e68b005375d1819e6b1636639bb`  
		Last Modified: Fri, 31 Jan 2025 02:16:03 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee17614b6e84590d7aab5cc47da2e026a4503522e09d4d43ca950f61fe84bf30`  
		Last Modified: Fri, 31 Jan 2025 02:16:09 GMT  
		Size: 43.7 MB (43728332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bb93e23d0fcf21539e3b4be7aafd5164ccdb181fa8afaac39d956ea7be442a`  
		Last Modified: Fri, 31 Jan 2025 02:16:03 GMT  
		Size: 93.9 KB (93906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:9793fbedf201223e7d5fe89dddf8b45910dfa8f5a97a26562466e5cf58cfff1e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164581167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa26082f09062bdb33469539a7048104f7b14b244f75004d44aa8be32b82ed7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:17 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:18 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 02:11:18 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 02:11:19 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:35 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:11:38 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Fri, 31 Jan 2025 02:11:43 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7ef1d7294a5bd3559f84d41284ff4da48c408f8a55e8312a68bf5c74333983`  
		Last Modified: Fri, 31 Jan 2025 02:11:48 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ae9548a41cf37fe6aa39437ed2b9addf795200219ef62e09526beb9628d05e`  
		Last Modified: Fri, 31 Jan 2025 02:11:48 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ae49fc2dc8c98cdb42753161973d3a65c48a40be2041b47168778c1d2195a9`  
		Last Modified: Fri, 31 Jan 2025 02:11:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b7d32525aaad59dc1a124a17c5f10027a2869a8a67d93a8200bb58be022c11`  
		Last Modified: Fri, 31 Jan 2025 02:11:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c09ad0877e1f9c7c838fa69e373723eee92a16219e653ad2cf0f37d78debadf`  
		Last Modified: Fri, 31 Jan 2025 02:11:46 GMT  
		Size: 88.9 KB (88903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44cf60f6a7d2ab83ce260d10057924c939ab1721a03d97fd34e41b21766d839`  
		Last Modified: Fri, 31 Jan 2025 02:11:46 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf904e92c4a19c178fa6813b5fdc7dae728befc017f8e8e43f588e125c7ab382`  
		Last Modified: Fri, 31 Jan 2025 02:11:51 GMT  
		Size: 43.7 MB (43728131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2140bd3c295a26fb7cb70ccf9ee73f0520f15aa7e540cea518a4644f984f81`  
		Last Modified: Fri, 31 Jan 2025 02:11:46 GMT  
		Size: 97.4 KB (97428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:2cbe46127d053fd504593a30154e5110c80c95a5064419a3688ebc7972422b36
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.0 MB (202043425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088a193a0a995ee13e348d77c30725110c0b376853900001eabc1792697334d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:11:46 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:48 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 02:11:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 02:11:49 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:08 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:17 GMT
COPY dir:e48212bf4bd9a001a558a3ce6925b9b3b6903c8af46347cbb9e06ca86192ff86 in C:\openjdk-17 
# Fri, 31 Jan 2025 02:12:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1d44072914e85d8aef8f480a6d089701677bcee11e6b8fd2aeffb001ef2eb2`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e48fddc7733467c55c4aa368d87b972da7dca7709eeb179fccbd0414a1214f`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51ef85cb87f1af29efe103a1470072cdb9cd31df84b1e8255da13102f2fe0ae`  
		Last Modified: Fri, 31 Jan 2025 02:12:27 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37973e712afd7b836700ddb4aee17bad305fcca7203eddeb3e33b5ec2227596`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacf67623da9b5d61a83b0125c59620d3ff80b9bf567f8cfb8baaafa7daead73`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 65.6 KB (65554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e072ea265e19dc3e48e09724e792d30a06f4018d6ead3123891a22999eed20b`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975c56306282a001cc1ca8f7f33d9eeafbd74f478a873057e9e7120782e055da`  
		Last Modified: Fri, 31 Jan 2025 02:12:31 GMT  
		Size: 43.7 MB (43728867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f20533afa69afeb1dd968c596928086f2cdcd12f86ffd6995ff798fdbdd82a9`  
		Last Modified: Fri, 31 Jan 2025 02:12:26 GMT  
		Size: 3.0 MB (2976091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
