## `eclipse-temurin:17-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:48ed5715c85c698df8002d46c8ca9a28cf8489ada56bf088aa67bcac07c24769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:17-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:0077cf1590381456545801159c051839f9e395e60d34d51272c414b860455c36
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380659676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7444b6c67e6f42d0199ba6c3f0fc58adebf8f0412a88f62eec4a4e1c0d998d90`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:15:21 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:15:24 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 09 Jul 2025 19:15:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Jul 2025 19:15:28 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:15:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:15:34 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:15:41 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Wed, 09 Jul 2025 19:15:50 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Jul 2025 19:15:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b565695996de0c36ce9d46ccee73e2775a04b59c0378463c914c696178b283`  
		Last Modified: Wed, 09 Jul 2025 19:16:28 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e900b144c8d2d4cbc29c0f8143173ba3955d82979f41d28cf429cbf811bd0ce`  
		Last Modified: Wed, 09 Jul 2025 19:16:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac1bfdeabd2aff21135ddaca5081a120d0c723b373dc45eb666f6d53435c3d0`  
		Last Modified: Wed, 09 Jul 2025 19:16:28 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea841b8b6230c664d50de574eb37368eedfb91533371a3f7b994d57be2456b6`  
		Last Modified: Wed, 09 Jul 2025 19:16:28 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17d1836fb8effc7743d82dac0b4b2f568a08db7a696cd75af6b596dd2dd0fbc`  
		Last Modified: Wed, 09 Jul 2025 19:16:29 GMT  
		Size: 77.2 KB (77224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c89d8604777a50bc6defb3c883bf3e626351c4ad630635249e1f55da1579fd`  
		Last Modified: Wed, 09 Jul 2025 19:16:29 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21413b2fe2d70ca1af55dde2ac72f390275c37f8d5cfe6045f8e2cd5a5b57d5b`  
		Last Modified: Wed, 09 Jul 2025 21:14:12 GMT  
		Size: 187.3 MB (187310970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50e4ae6f697df2fc08c03fe4dc39fd1cfebab02fdae5c971d2966cf9c966f30`  
		Last Modified: Wed, 09 Jul 2025 19:16:29 GMT  
		Size: 114.6 KB (114632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54587ec0a8f05b026e23e3f8b44b1f8030315af7ec1b3df51c2bb9e37e053656`  
		Last Modified: Wed, 09 Jul 2025 19:16:29 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
