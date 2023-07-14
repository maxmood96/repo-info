## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1baf6ea997dccb02bcc186d644443e5edd4f56093d4ebb11b60a86505b75537e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

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
