## `eclipse-temurin:21-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:9395badfde142632286805efa04c7243f478295846e4ac80981e62d4c3b81dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:21-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:7150b8a8ae812f87f552252172d51e7f251705b842001748b6e616c287967d8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.8 MB (391815475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d922d3422bc7f013c6abc72ee86e576da32a5e7332a3e987fff0680fc67f5d35`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:58 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:59 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Fri, 18 Apr 2025 04:15:00 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 18 Apr 2025 04:15:01 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:05 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:13 GMT
COPY dir:87fb2a3fe15bf051f07e33b0f4d627a83582ff5ee0a30a4b75036496ad24f723 in C:\openjdk-21 
# Fri, 18 Apr 2025 04:15:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:15:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b47e80cf06020c6d9c791d19b288bb8dbcc74f3977e609bded147735b06acf`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d72b27313df724a3fd651182f8667cf7ceadc611ce44ccfe37c5084c78fa57e`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8f37013157d75d3577b4bbb5a6d4ff6ca2c05940d17dc13a7343af1cba9fce`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f83b8ab39e73000f236fc570dbaff46bc3de1bdebcec49a751e363d472b91b`  
		Last Modified: Fri, 18 Apr 2025 04:15:25 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609b3260f014188310ac84c78b1f33bab58710fe28cb243435b9fcd3279cb06f`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 76.4 KB (76416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a6470c1ba45d72a13f28742d6c3a85c2c136b1361dedaa4d4290cfb5273a62`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87aefe6a9e8e06db0e3c3c37f1bdcb835990364170270d99ce44a652cda239ca`  
		Last Modified: Fri, 18 Apr 2025 04:15:35 GMT  
		Size: 201.5 MB (201475986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39922790ce4f9ea5740440487cf355b7ad1225f6e2abb93ef93a2c664313d4fe`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 114.6 KB (114617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d393b2b1ba2f0224012fe01c1281bba7e10633b0e36a9a80107ddeb8e957651a`  
		Last Modified: Fri, 18 Apr 2025 04:15:23 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
