## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:afc6621e6c5b40a85fdb2f914a6edd0db6666f2a551284f41e68d9fb3df213af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:796f55d1c452395124a38f63337194dd49b4d3808248c650d22abdb975a28bd2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237422783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e96651cb21cea60066632b36abcf308321f881751dd9821582f1298fb53e05c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Wed, 10 Sep 2025 22:18:57 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:18:57 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Wed, 10 Sep 2025 22:18:57 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Sep 2025 22:18:58 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:01 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:19:05 GMT
COPY dir:58dfc6149e1020fd4be2dce5848817d79ad79993fb8b5211b36f6f0e332ab65c in C:\openjdk-11 
# Wed, 10 Sep 2025 22:19:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cae81f6e5d0775570e4f827d0417ed429ae8e62c0aa0740d16384c5b2d5aa5`  
		Last Modified: Wed, 10 Sep 2025 22:19:33 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faea08d59e4a66baf72fae564faf492a66176572e09253fad4376bf355d9774`  
		Last Modified: Wed, 10 Sep 2025 22:19:33 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f931cee5befb051d50d334e7e98c8be7b2b24cd5fd0b97c8cc8f96a6bbbfe6f`  
		Last Modified: Wed, 10 Sep 2025 22:19:33 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b93b981c3963568da58a9ab61fd6be4b845cbd4fdd53c32da74ea8125266d8e`  
		Last Modified: Wed, 10 Sep 2025 22:19:34 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727e549fb4d472d87b7ccd4a9eea16650f805a57615c67eeab02aa6fdec9cbc6`  
		Last Modified: Wed, 10 Sep 2025 22:19:34 GMT  
		Size: 69.7 KB (69699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099abbbbaf719b35709d1c001ba647125c43e40c815602f422fa5a09a7167767`  
		Last Modified: Wed, 10 Sep 2025 22:19:34 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53d93854bc5b566312bae2036ff7b51b3e8cb5330e8a4956ded03a32cbbbea2`  
		Last Modified: Wed, 10 Sep 2025 22:19:40 GMT  
		Size: 43.7 MB (43666166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a036d766f5e4003a4d558b7a9a9a4b1da9b2b3022f9cb94c6f629584299d1aa`  
		Last Modified: Wed, 10 Sep 2025 22:19:34 GMT  
		Size: 130.8 KB (130769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
