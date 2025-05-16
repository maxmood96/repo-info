## `eclipse-temurin:24-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:59876d9907fc0e0a5c26fe060b37bc752a27f3f61e2b665be08ce58425f15462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:24-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:2c3196efcd00633b20afc63a3bc352b3b6caf3057352dec0caed1301d0a9b693
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260132445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ca54a91c7b89e95ba51dc11acbe284b7cf0f88f9e78bc64080d148bad2f8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:20:17 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:20:17 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 21:20:18 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 14 May 2025 21:20:19 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:20:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:20:23 GMT
USER ContainerUser
# Wed, 14 May 2025 21:20:29 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Wed, 14 May 2025 21:20:35 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:20:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939d81a27180b48f7f15ae5365326a36b8d166840e71452ee1a239279fea0ba7`  
		Last Modified: Fri, 16 May 2025 15:22:41 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4439a44114017e4442b88ed2dd453106485a705884d45bfc5644905f3f285e83`  
		Last Modified: Fri, 16 May 2025 15:22:41 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa49baa7921fef4398aaee7d44e1fcb3ff9e5224ca7b74c02f3e5755266e7ad8`  
		Last Modified: Fri, 16 May 2025 15:22:41 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87925e93bc821ed820fe34ee81ecc967dc82ec0b3d0e94b435663131f1cd81fc`  
		Last Modified: Fri, 16 May 2025 15:22:42 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dedfdb105cdf0146069b8f862653d1f07774c56f2f3f516446e30c0bbc6791`  
		Last Modified: Fri, 16 May 2025 15:22:41 GMT  
		Size: 78.1 KB (78100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35168324e6b43ca95f27469f1893f864fe6c867b80c2e2a22819f23f3df898d2`  
		Last Modified: Fri, 16 May 2025 15:22:41 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fc438fe7b005c1cd4cf46ccb7d14d485fde7c6d1515172d2ac35a8f2deed8e`  
		Last Modified: Wed, 14 May 2025 21:20:49 GMT  
		Size: 137.4 MB (137364691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e09c6fcd4756c962046624856b9d82c2a1785a9a7450d8121e2246d86cc852`  
		Last Modified: Fri, 16 May 2025 15:22:42 GMT  
		Size: 106.9 KB (106856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f55f45d704cf5b062e6e074a8083d7b0c40cc4dd5a748eca473fd10c78d825`  
		Last Modified: Fri, 16 May 2025 15:22:42 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
