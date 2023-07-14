## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:3a7f69844ce382384e576170660e31c9830076bd4488259e5f7d82e08e8fe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:e2778e97fe99a809f6eb35998734cf788779cc1991cc551918a72aedd3c879a8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160187797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f69013a16918b0d86ef3e126743f666bb65b9aeea7a6843f7e93170037616c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:10:52 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 13 Jul 2023 22:10:52 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Jul 2023 22:10:53 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:11:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:11:08 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:11:48 GMT
COPY dir:8a6c7975745f12f5841a11f3a56ce128ecca26850fc38f023ad9679c09b008c3 in C:\openjdk-8 
# Thu, 13 Jul 2023 22:12:00 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11750b624a775aa3c21a13406dfc54458855b8684e21efba5bbb9b27ee0b12`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7769a380665a420d9507522f1aa2325e5ff8533bc2b44ab31bdce3ae0a172a7d`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c2074eceda78b9dcbe189644d3b9e33ee5cb27926556651d9c61b87e520367`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4628b22c6414e87da57200de9ba8ac51cda12d9df80db5968aaaef1ca99c9f0a`  
		Last Modified: Thu, 13 Jul 2023 22:28:33 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0adea2a769db0f465f4aa2659011ba096f32696159a4711a292a33c79cc956`  
		Last Modified: Thu, 13 Jul 2023 22:28:33 GMT  
		Size: 99.1 KB (99086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c7910b6891ee313a57a67dacd3e5c325c8b805c9f694110896297824801a26`  
		Last Modified: Thu, 13 Jul 2023 22:28:33 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19540e8570b262ca419b6189cca7537814ae5eaf85661105fe47836d7d2b8f11`  
		Last Modified: Thu, 13 Jul 2023 22:29:02 GMT  
		Size: 40.0 MB (39957289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdafd43c49a94441a85086ffc4008fa12d90e697d483c74f873dfd3e178646e`  
		Last Modified: Thu, 13 Jul 2023 22:28:56 GMT  
		Size: 69.2 KB (69167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:1d1aae9742e8fff072fd84161263ed7ddb77bb151898329d4cff7f837756c543
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144537737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76085169d938af871ddd8401f894fe5ad0c944206ad2506d01e3ac827b235f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 21:36:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 21:36:33 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 13 Jul 2023 21:36:33 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 13 Jul 2023 21:36:34 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 21:36:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 21:36:44 GMT
USER ContainerUser
# Thu, 13 Jul 2023 21:41:10 GMT
COPY dir:8a6c7975745f12f5841a11f3a56ce128ecca26850fc38f023ad9679c09b008c3 in C:\openjdk-8 
# Thu, 13 Jul 2023 21:41:22 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13c473988daf5951866dd9b290bd6417227c1d7df6e811cfe11438d033a1eba`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b30eda955daff9169341fdb80582892899af8281f4a212720442538e2423fe7`  
		Last Modified: Thu, 13 Jul 2023 22:19:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81b7fe9ecdd110abd7fdedec4f78d1c2618bbd040bdaff607352462b87e69e2`  
		Last Modified: Thu, 13 Jul 2023 22:19:06 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c488c573b312bf1ff8965a90b400d1c0e504c43a3ef81be737fc6a2b6a1685b8`  
		Last Modified: Thu, 13 Jul 2023 22:19:04 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce833e9d67aa99c3f24c4581dab3878c0005cfaca0340e8ac34e310ed4eedb4`  
		Last Modified: Thu, 13 Jul 2023 22:19:05 GMT  
		Size: 77.7 KB (77728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de2e484bb71b98cc30d2c993a6a3478b5686b6e41e6a711d21c54aac53170cf`  
		Last Modified: Thu, 13 Jul 2023 22:19:04 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141559ac6f1bdbf8391cefe42425abf40ef3b8455686a0bc707569194cfad974`  
		Last Modified: Thu, 13 Jul 2023 22:20:08 GMT  
		Size: 40.0 MB (39958474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ede0d7cf7aa8f091ab0e11e872ff37221185e5b73f24ed6cd69a5cd7503568`  
		Last Modified: Thu, 13 Jul 2023 22:20:02 GMT  
		Size: 88.0 KB (87969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
