## `eclipse-temurin:8-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:53ea97043973c8ddcf5f66a4b32624069e721137b44aef4ae9aeadecd4b7a9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:8-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:80f88c99efc893d8341f51de207ebe8a8a2752c3840ac458049baa91b8edc78b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296657747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e2b1bb734beca6e03d99491ae7d94151755b65af5830c7633256071421a7c7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:17:09 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:17:10 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 19:17:10 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 08 Nov 2025 19:17:11 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:17:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:17:17 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:17:38 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Sat, 08 Nov 2025 19:17:43 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5bcaa6a59bca329f822ff0f20eb66ba9198423e4c584b435e6c65c73c8ea82`  
		Last Modified: Sat, 08 Nov 2025 19:18:15 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7834b6d9619ec372eb1100be6b3c4a50eb834e1bf4e7c1e3836a85f0b94367`  
		Last Modified: Sat, 08 Nov 2025 19:18:14 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ee036418afba1ccc3944ffde952060e139ca41e85a48a4fc1da32a377e1364`  
		Last Modified: Sat, 08 Nov 2025 19:18:15 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470470850b0f3721490f28711efce5e72ffd156a21ac223d79bdd1a7a5bdd36d`  
		Last Modified: Sat, 08 Nov 2025 19:18:14 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065109cb74512f3f46fd30292a25a624d50058430cc23b71196d1238a55efde0`  
		Last Modified: Sat, 08 Nov 2025 19:18:14 GMT  
		Size: 70.3 KB (70256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25284ee38c6848924afe34f115619a410612b497b1b73e92a81f10104d2ed8a`  
		Last Modified: Sat, 08 Nov 2025 19:18:14 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16335f506c29bca02f432d5ee12470907a40dfec8a9701c717306d756337073`  
		Last Modified: Sat, 08 Nov 2025 19:18:30 GMT  
		Size: 102.4 MB (102438379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cd1d7f9b96d5180162d4c5bd144fa0e0f9173a7565c604639e8a3964d5b671`  
		Last Modified: Sat, 08 Nov 2025 19:18:14 GMT  
		Size: 114.4 KB (114388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
