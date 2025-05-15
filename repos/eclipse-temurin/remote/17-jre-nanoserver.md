## `eclipse-temurin:17-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1a6d854f9ac21e86fe91d49006fa2f0b8d6943ad58e41eac03cb590d2c0e1773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:60d0960634335e930ec5c8afe657ec9e3d8a0d14b24f2a7a8b3d9423d414cb49
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235332057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066d1c1db517bee1ee69c0e7f3d0d9912733b11e7905f0d5f626fca0c73e2dbc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:45 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:45 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 14 May 2025 21:14:46 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 May 2025 21:14:47 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:50 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:54 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Wed, 14 May 2025 21:14:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a7b3ff86be05ccf046e9249d9f06587f5e1e097077cb2e4d6f876f64b00e34`  
		Last Modified: Wed, 14 May 2025 21:15:02 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb3203be181923c907b7985a9a096e6ab7762bc24e7fb423ab309ff18ccaf`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e6cd53fe042de505cbb6a0ca6d0fc2cf63a675e02532b81ca09c849012d6a9`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2899e26c751a84f62e85834400c7f19854e515bd104cd0c103a2c25dbcfed920`  
		Last Modified: Wed, 14 May 2025 21:15:00 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be574b82940cec6c0c3eed5ef0cca9d693adc335f0fd6a2e52dec0051545e02f`  
		Last Modified: Wed, 14 May 2025 21:15:00 GMT  
		Size: 75.8 KB (75850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6655a66fe18fd74dcd871dc1d91581b6e4bbef6fffbc6e357e40404a88d6fea2`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1637804aabf9c1f5a419c77493bc850a83ac89532dfb381597947fd78da798f9`  
		Last Modified: Wed, 14 May 2025 21:15:05 GMT  
		Size: 43.7 MB (43736602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafb0006886b1d0888b6152c452884dc86144acccb179ba72566a440dd6d6b00`  
		Last Modified: Wed, 14 May 2025 21:15:00 GMT  
		Size: 102.3 KB (102313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:3f63ecda41fee2eb63cc5ef184b8dfa1f450127c4be297eb22f57f71a8114864
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166490496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fc56f819aec9c7a14b777d224d398cc6299be5e019188ea14c1af1b63d7317`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:17:49 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:17:50 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 14 May 2025 21:17:51 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 May 2025 21:17:51 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:17:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:17:55 GMT
USER ContainerUser
# Wed, 14 May 2025 21:17:59 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Wed, 14 May 2025 21:18:03 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Tue, 13 May 2025 19:42:18 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7167beea15f8697d05a761729964ac422b9f78dcc0f272b9396e20324053badf`  
		Last Modified: Wed, 14 May 2025 21:18:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8a68257d4d116507d44431d9b0f7ae54cd4a85d52c0724c3197741da3a7f21`  
		Last Modified: Wed, 14 May 2025 21:18:06 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc770bb54f0939ac65133c640faf7d14a75150eb41dba28900d84c000e6ef1a`  
		Last Modified: Wed, 14 May 2025 21:18:06 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f4410768093a91cff4c5b2bc205f578cd181f6d5620c6161b913892d958283`  
		Last Modified: Wed, 14 May 2025 21:18:05 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135395f8ac7f4cb9ef77c9467e4ed6b3004970ebc761f062c7ac16f394fc97d0`  
		Last Modified: Wed, 14 May 2025 21:18:06 GMT  
		Size: 75.9 KB (75948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e0f1bc261a376195c4afc76b5447f22d281b692134975fa2f998226a56be9`  
		Last Modified: Wed, 14 May 2025 21:18:05 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd54f6a6015071c405ebe9ed441d89399e0e1e4f609c20b4a2e0d7c0c28722c`  
		Last Modified: Wed, 14 May 2025 21:18:10 GMT  
		Size: 43.7 MB (43736920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c269676e79771774910e5f84cd28112450f75ef2afe34ca94592314759e228a1`  
		Last Modified: Wed, 14 May 2025 21:18:05 GMT  
		Size: 95.8 KB (95812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
