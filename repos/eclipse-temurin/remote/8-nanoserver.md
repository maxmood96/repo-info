## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6a1d8179495d89469eea1428c393869ad69d723f60ae8e2ed3aa085c93867d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.26100.6905; amd64

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

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:373d4d604024c01cbdf9bcb9cc6e65547b1a12836f216b7f7037da5882271474
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225340004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeaee3454475929e7c00dff175716b14788cc63b7f7b5e8122a8318e7f33c05`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 18:23:56 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 18:23:57 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Sat, 08 Nov 2025 18:23:58 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 08 Nov 2025 18:23:59 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 18:24:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 18:24:06 GMT
USER ContainerUser
# Sat, 08 Nov 2025 18:24:46 GMT
COPY dir:2635c350952b93f594bde5c3dd80336e4c4ce35889642cd7d3de9ae358e6cda3 in C:\openjdk-8 
# Sat, 08 Nov 2025 18:24:51 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29e827a0b0b7fa018d91809186f9e730d22f75e2cbc863540c33822cfe22b96`  
		Last Modified: Sat, 08 Nov 2025 18:25:12 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ab01cdcf9566c7663a47c114253d6e523f02c84119c22fbddb6c5bd115a26f`  
		Last Modified: Sat, 08 Nov 2025 18:25:12 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3163af7200288bc5618422bb2e8bc11d5f593e4373298e4ca33bbe4d4800027c`  
		Last Modified: Sat, 08 Nov 2025 18:25:12 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef3fb97898d3595671f2514a46d9ea02764f0e0807890dcfb3c7b7855cad837`  
		Last Modified: Sat, 08 Nov 2025 18:25:12 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7468809fdb5dfdae8ba254e64e240d4c8f9b09b182b375e6fda86fa34fa1981`  
		Last Modified: Sat, 08 Nov 2025 18:25:12 GMT  
		Size: 84.2 KB (84238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58486da37d228af9ed580833dbd425871810813396f40e9524f4ac6768520247`  
		Last Modified: Sat, 08 Nov 2025 18:25:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e312e9b721d57292d996ed8e9596efed963495ca6437e31c25c39bb9a1d3caf8`  
		Last Modified: Sat, 08 Nov 2025 18:25:28 GMT  
		Size: 102.4 MB (102438131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1bb2641ba4b016bf64691c5c7c699f6c65458a1fa03faffcea951d7f543aa`  
		Last Modified: Sat, 08 Nov 2025 18:25:13 GMT  
		Size: 128.2 KB (128242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
