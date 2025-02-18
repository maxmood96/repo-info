## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d5e32f12177edd28597c570ddd1fdc7be87608a4be815f3b4a5a866b2093beb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

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
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f1cfb1a515301c5d46cf52e997da0cd6b39b4931276bb0a8f949bf64df59b`  
		Last Modified: Tue, 18 Feb 2025 10:25:16 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361c604da3cd668ec671428558ab50f8041ccbabb3e2d701206ebe8fc4d2f82`  
		Last Modified: Tue, 18 Feb 2025 10:25:17 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f8678fb2273aaea0e5d8b4a4d441519357db4ba2c0ed3d698c5f6d700b8da8`  
		Last Modified: Tue, 18 Feb 2025 10:25:17 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d357b54a9ccdeda6a0652b96b0af50cf040baf64894e289a3854b14b6c92f88`  
		Last Modified: Tue, 18 Feb 2025 10:25:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4868e4d22dcd0f4885ea20c49394df92ba867e8417b085cdec5b960b265e540e`  
		Last Modified: Tue, 18 Feb 2025 10:25:19 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf18df91fa4de25aa893064c380b047c7860e68b005375d1819e6b1636639bb`  
		Last Modified: Tue, 18 Feb 2025 10:25:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee17614b6e84590d7aab5cc47da2e026a4503522e09d4d43ca950f61fe84bf30`  
		Last Modified: Tue, 18 Feb 2025 10:25:22 GMT  
		Size: 43.7 MB (43728332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bb93e23d0fcf21539e3b4be7aafd5164ccdb181fa8afaac39d956ea7be442a`  
		Last Modified: Tue, 18 Feb 2025 10:25:23 GMT  
		Size: 93.9 KB (93906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
