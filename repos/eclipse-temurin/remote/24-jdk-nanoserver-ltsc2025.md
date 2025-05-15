## `eclipse-temurin:24-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:5bfb470ffbe20fd24355fa96af6591d112a21dc9a25477ab6fe79c9dc7da7551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:24-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

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
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
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
