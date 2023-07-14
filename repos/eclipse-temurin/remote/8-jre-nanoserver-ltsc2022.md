## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0abfb3b9ec0bee00708cda8fee3e4b3eafdd4aeba8667f14e0f8acb0ce2c651f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

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
