## `eclipse-temurin:8u372-b07-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:d39ed5796d694e7caecf0c3804a3ff3f889782ac0f01ab391f96609f037ceb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:8u372-b07-jdk-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:064ddfbf34281ae22d6ac548763801d452b8122b74ac2ec20af6b9bab5004302
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221668964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5639fda01d5cab4fc4eeba36a901cba815e769f6cc88c65121392f9db9289982`
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
# Thu, 13 Jul 2023 22:11:18 GMT
COPY dir:27c7e47be02cf877d3f45f48fc9f53f313487829869ebfc4770f3f1b0ee2a0d5 in C:\openjdk-8 
# Thu, 13 Jul 2023 22:11:32 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:24813fd2a4737f18439c6a8e06035f7ebe79d421ba4feb73092cd5455adc6bd9`  
		Last Modified: Thu, 13 Jul 2023 22:28:44 GMT  
		Size: 101.4 MB (101438490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a5b81cf53fa5c1db46bc0d9602992a4dc1d453613f243b488326d5f10c9b49`  
		Last Modified: Thu, 13 Jul 2023 22:28:33 GMT  
		Size: 69.1 KB (69133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u372-b07-jdk-nanoserver` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:35f53462f89790f6ef76da51daf2a18a321c3ac3fc760dbe61d7ef77747cb456
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (206035499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b5a519a6d39a78ac577b0f51fab50973d23def5615e654911d148746a16542`
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
# Thu, 13 Jul 2023 21:36:55 GMT
COPY dir:27c7e47be02cf877d3f45f48fc9f53f313487829869ebfc4770f3f1b0ee2a0d5 in C:\openjdk-8 
# Thu, 13 Jul 2023 21:37:10 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:4daa7a06d352a9d2aad50e301bf153f9f7b37b2e533e69a634a49d558ba503e5`  
		Last Modified: Thu, 13 Jul 2023 22:19:16 GMT  
		Size: 101.4 MB (101434649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eceb4d756fa9c54183a3622c7075415e145c2dae90bc1e6a7c9430593f0f8e4e`  
		Last Modified: Thu, 13 Jul 2023 22:19:04 GMT  
		Size: 109.6 KB (109556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
