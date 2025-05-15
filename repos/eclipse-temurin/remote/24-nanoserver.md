## `eclipse-temurin:24-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0529edf8fdade0d4cf7bd8fe517d10b9e47ca69ef7ee6c48302a9715ec44b035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:24-nanoserver` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:51d8d3f5e42cb381d77a5fa58b8527580391e449a1b450844c751a6f7317db45
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328972558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6671b439ce98594d8d2724658b5b817678526ee564687dceb1e55e66ad239a76`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:28 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:31 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 14 May 2025 21:14:32 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 14 May 2025 21:14:33 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:40 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:48 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Wed, 14 May 2025 21:14:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:14:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089c21d93e5b8c9b33fec4f9ecbe0a37721f6c76310f0389e7611f84ac1d16b1`  
		Last Modified: Wed, 14 May 2025 21:15:04 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0216f23c109ebd263b55c3fc10a590ef56e82c207fc0588c5818cf1f4a23a53`  
		Last Modified: Wed, 14 May 2025 21:15:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec147bd3294e3bb0877157d3cf5268741d14c65ff00444370a6bcb1d83a3be1`  
		Last Modified: Wed, 14 May 2025 21:15:04 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6bd0d58fa3b1e739a4c187d2aef7f4428163236afcc638a476389c29ed8061`  
		Last Modified: Wed, 14 May 2025 21:15:02 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cf9ad41b09ff6cd91cdb374c19685f86b203b5e233e5875669216826541f56`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 76.1 KB (76076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4112afe2f3120d2e2b2f135772cd296cd906ec971aa478dcf1061ecaee590ee`  
		Last Modified: Wed, 14 May 2025 21:15:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e176917ef5d5174572a470731e2d7d79a30e3a681c0ba55d8bbd3c1f270aed7`  
		Last Modified: Wed, 14 May 2025 21:15:12 GMT  
		Size: 137.4 MB (137364034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b905d7251814993d7b57dc126c9cb733c86768de56ddf975947d3cdd914f2e03`  
		Last Modified: Wed, 14 May 2025 21:15:03 GMT  
		Size: 114.2 KB (114180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f860926913667c589bd253c0f530467f3f14ea7ae81c2f54beeba457c86e77`  
		Last Modified: Wed, 14 May 2025 21:15:01 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-nanoserver` - windows version 10.0.20348.3692; amd64

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
		Last Modified: Wed, 14 May 2025 21:20:40 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4439a44114017e4442b88ed2dd453106485a705884d45bfc5644905f3f285e83`  
		Last Modified: Wed, 14 May 2025 21:20:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa49baa7921fef4398aaee7d44e1fcb3ff9e5224ca7b74c02f3e5755266e7ad8`  
		Last Modified: Wed, 14 May 2025 21:20:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87925e93bc821ed820fe34ee81ecc967dc82ec0b3d0e94b435663131f1cd81fc`  
		Last Modified: Wed, 14 May 2025 21:20:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dedfdb105cdf0146069b8f862653d1f07774c56f2f3f516446e30c0bbc6791`  
		Last Modified: Wed, 14 May 2025 21:20:38 GMT  
		Size: 78.1 KB (78100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35168324e6b43ca95f27469f1893f864fe6c867b80c2e2a22819f23f3df898d2`  
		Last Modified: Wed, 14 May 2025 21:20:38 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fc438fe7b005c1cd4cf46ccb7d14d485fde7c6d1515172d2ac35a8f2deed8e`  
		Last Modified: Wed, 14 May 2025 21:20:49 GMT  
		Size: 137.4 MB (137364691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e09c6fcd4756c962046624856b9d82c2a1785a9a7450d8121e2246d86cc852`  
		Last Modified: Wed, 14 May 2025 21:20:39 GMT  
		Size: 106.9 KB (106856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f55f45d704cf5b062e6e074a8083d7b0c40cc4dd5a748eca473fd10c78d825`  
		Last Modified: Wed, 14 May 2025 21:20:38 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
