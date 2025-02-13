## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7a02540cce570371612806ef23c488f679e4819719b5a5987611f59609bea652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:b975fae58d69b9d73ba37be1135b7242912cce2dd2ea40ddabdd66c9feb9e3dd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393801078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45667f9b181f584bee0a2ab032df61344b5374ee68bdb942d53550ebe0adfe5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:16:40 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:16:41 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 02:16:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 31 Jan 2025 02:16:43 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:16:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:16:49 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:16:56 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Fri, 31 Jan 2025 02:17:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:17:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf4cac08657e35f531d4d122b5dea475e3fcb8473a30c2d0b98694e65011bf8`  
		Last Modified: Fri, 31 Jan 2025 02:17:10 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ec2b9e65e8712b8f0e30b631f7614cba427aa7084a52ef53924d801a7b5f71`  
		Last Modified: Fri, 31 Jan 2025 02:17:10 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdce1f6ae7973a405d5172cd6a657ad2161ce15105a2204e99c2c1d6b7ee8ec`  
		Last Modified: Tue, 04 Feb 2025 17:18:53 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c24debb0cfbf08a5908319a43f11dfc9e4e3cf25df28ae2d717af653bd137d`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b75727cac3d511d96c604cb484f14adfe06edc58bed0c0533b4d361da21781`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 76.2 KB (76241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38e63857b81a33b940431536733517488c6157adb542b1c6fa1cb654b0364e0`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04163d4be6ee7ca67ed67e04b3170f729e0394b4e2935844e9f65b3f6963da57`  
		Last Modified: Fri, 31 Jan 2025 02:17:19 GMT  
		Size: 194.6 MB (194557242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227318206d3b582ef3d70a6a1f7be95cd3867a2a3b383ae9f7232302b6341f67`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 107.0 KB (107019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6bcd98ceef5031a4346422c80ef0791241d37aad2b53fc8a2b68ebb27906a`  
		Last Modified: Fri, 31 Jan 2025 02:17:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:ade93d863953bd2cb86ab15eac4ebfd43f8e7696c0dc0651f81b22ac117541b2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315413732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07fad728c329034da99dd31830854fa06c2d08c0d2ed830ad6db59522c3723`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:39 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:40 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:18:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:18:42 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:18:46 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:53 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Thu, 13 Feb 2025 01:19:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:19:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a10a0feedc7dc71d6069a1910fa2f6c6fab8d26c3eb9258ddd4a452600e15e`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8f394aef31637bf2d62726e45fa921c1f69858cdb7fad7c8a8009cfba1ca62`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7eb79eb3be23dc422362e030b2683cae6213181b9cc1009595323c6bf7a38a`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df56be39d92120c3b06aef88f3bedadd3ae11c1a679ba7ca0f0e978fd172124`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df1843bbecab426366124d35064d251ca9a6ac50bdeb27e103e272da2142e6d`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 77.0 KB (76995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc9c62487efe4fb7fa3b070e4be6b896e1fce2c7c1c80cd04883a12213e1f6d`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7c651ef068fd24f841439b3903587e5efd50025359639cd55f38b9934bb308`  
		Last Modified: Thu, 13 Feb 2025 04:12:46 GMT  
		Size: 194.6 MB (194556786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e9bb039ca0dcc2b26abcf9fb8ae71c28d0b6727ce59cf377e27b9f1a9699c8`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 106.9 KB (106877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b482822ecd365f70f4ed5389b779b9d410d35ef2a3225f5e2f5841261e4ce10`  
		Last Modified: Thu, 13 Feb 2025 04:12:38 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:f9d4d5220b4ad3dc4fedfde49848e71e770493499cdae8f0e2d3a242da4c356c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301648456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5526874000f840fc8708e0617520a1f369fec717c5e41e4138cdd76e9baaae0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:11:53 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:11:53 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:11:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:11:54 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:11:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:11:56 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:12:03 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Thu, 13 Feb 2025 01:12:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:12:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee5e44cb2688ba9714bcd16871834fa8451602470e350aa40d00e945513aba6`  
		Last Modified: Thu, 13 Feb 2025 04:12:36 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0282a74c64f75268f379c718c068cd2307c2c2a3aca9b6bc30af8d8a38b68e2a`  
		Last Modified: Thu, 13 Feb 2025 04:12:35 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0bb9eb067940e945e2d2de8ddbadf5d82a6bc72f52cc4ae2f9d0d9f2d39421`  
		Last Modified: Thu, 13 Feb 2025 04:12:35 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0e2e7fb0809c379887c08c14d15b51d61d402d917d83a8ac35cf937d5c0893`  
		Last Modified: Thu, 13 Feb 2025 04:12:36 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6953294570ba3d03408c4f789af998f871679df0146736eb54019bf700eb71`  
		Last Modified: Thu, 13 Feb 2025 04:12:36 GMT  
		Size: 71.0 KB (71022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb932f4e49331dc4cb2df20eb9fa2075498a2d69a5efb9c646ea4fced90fb17`  
		Last Modified: Thu, 13 Feb 2025 04:12:36 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3af8a0e08082525f0805dd2643e73c92931a3df8cbb6ab2fb0b3d1600b2f1b`  
		Last Modified: Thu, 13 Feb 2025 04:12:47 GMT  
		Size: 194.6 MB (194555902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dc7fbcb9d50edd7186dc23b7262c7cc82955bb980eb6386a36055152edb75c`  
		Last Modified: Thu, 13 Feb 2025 04:12:36 GMT  
		Size: 99.8 KB (99840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3889e6eb9cafca8240e2d15981c0480627d0eb7fca0e39a975ec06166e36a259`  
		Last Modified: Thu, 13 Feb 2025 04:12:36 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
