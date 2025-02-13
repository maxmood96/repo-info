## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9074f0b83f281ecd5aa47dd6c74364d69ec9670e974b886db18b3b7a1381f6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:23633053af253668ca1d29ccf4584deaa6b99417e2f9a0703d94df678b6dfc11
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.1 MB (308086455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4c90b4dcdfd29310d7bba6815ae4e8876015b5b2bf3bb5e24770a1299c7456`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:52 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:52 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 31 Jan 2025 02:11:53 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 31 Jan 2025 02:11:53 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:15 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:25 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 31 Jan 2025 02:12:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:12:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6741908a3573e93ec87b8f3cddd01298399de0b4e4b43331f7ac22dcdf7865`  
		Last Modified: Tue, 11 Feb 2025 07:15:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e1c20be48399a5e19ea9affaba712a5447e21469993906ed4c3472ae892717`  
		Last Modified: Tue, 11 Feb 2025 07:15:38 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492f76981cca18e5e7a590b2d8d6eea23084d58b04c7c4ad5e1cac84b8ea9d74`  
		Last Modified: Fri, 31 Jan 2025 02:12:36 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596532e150659c6e49728645038b6d160c9ad31c3d1b070e384c71f36165e259`  
		Last Modified: Tue, 04 Feb 2025 17:27:16 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0586230100fdb9f47f97e2e43e5add0c7e72278597bfd297acffba445dba624`  
		Last Modified: Fri, 31 Jan 2025 02:12:35 GMT  
		Size: 84.5 KB (84510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067438762b6de144f2fcda298ea7ee195f0f53424ae66ec05e654eba5063a983`  
		Last Modified: Tue, 11 Feb 2025 07:15:39 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dce9e54ada3b783774fb00f818e5d5818b6639c41ee34d1bb41c693a52d999`  
		Last Modified: Tue, 11 Feb 2025 07:15:45 GMT  
		Size: 187.2 MB (187235194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf5a87827a511a6b62a27e60c0bdc27b761d39cbf21e77faa3aa4e538fdf405`  
		Last Modified: Tue, 11 Feb 2025 07:15:40 GMT  
		Size: 98.7 KB (98730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fc15e4276cc608899fcd6a6c858e2b8d77dee4b3c5967dde7aada64a3e5a71`  
		Last Modified: Fri, 31 Jan 2025 02:12:35 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
