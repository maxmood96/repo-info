## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:55e991489c0a3277ad1f454d44e4d06976fe1018287f9d7e089d315e8b1d38dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:fbea5c2ecd94719047cd48870a44e60ba222b2149933b0e6f3df294b54abb53b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309610796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0523279e393812cee73c172b0cbec2682ba80d9c7f289971695e3061c2bc4c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 24 Jan 2024 21:48:36 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 21:48:36 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 24 Jan 2024 21:48:37 GMT
USER ContainerAdministrator
# Wed, 24 Jan 2024 21:48:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jan 2024 21:48:46 GMT
USER ContainerUser
# Wed, 24 Jan 2024 21:49:00 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 24 Jan 2024 21:49:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jan 2024 21:49:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec88c6fd1d0cd14082069642ccb3b0dd5a7538a4b8b0c2d430549f345d8fd53`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cec230829dbfcf404f6c33286166ea2078a19b9d68b0df812ecf36f024e6dea`  
		Last Modified: Wed, 24 Jan 2024 22:09:56 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a4733a1e7b5204caa5600e2eb27e416f65a832e6f45729f6a1ed8e163294bf`  
		Last Modified: Wed, 24 Jan 2024 22:09:55 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857afbd5749e10f14a05f80bf17299f68c74f57f74b6ef39324782790f49694e`  
		Last Modified: Wed, 24 Jan 2024 22:09:56 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971b4fd09ea068aef662c8791827450311f9b77d140c7c6510119a0c9b200a5a`  
		Last Modified: Wed, 24 Jan 2024 22:09:53 GMT  
		Size: 68.3 KB (68334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae59143b8d2d281ad288506d7bdcf851e63b207cdf90262d1e44c9c5e754b434`  
		Last Modified: Wed, 24 Jan 2024 22:09:53 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a014f06283402e136e0ded0afd2fb5edee12c3497cefb2faf0e3493eee0e1d`  
		Last Modified: Wed, 24 Jan 2024 22:10:11 GMT  
		Size: 201.1 MB (201125725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c8f39ff7608e3233798ceeba0d8104795389865fefd77e2a7968f230200391`  
		Last Modified: Wed, 24 Jan 2024 22:09:54 GMT  
		Size: 3.8 MB (3818553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe2772c5dce43e8229603f7ffb302a5486e4fdb66d804646ab434651424830`  
		Last Modified: Wed, 24 Jan 2024 22:09:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
