## `eclipse-temurin:26-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f8603b8d0bc8578bde2175adedf2470127bf64a1af248095dd9c279b2afa06b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:26-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:6f7200e3b9a539f18df0e1cb5b32a37c5eee01e15f4b7f36bb7a85040a4f176b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268174439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa9f6c983f786c40a98fe54799a3a510a2a01cadd8e58f1c475fa034ec10a0d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Wed, 08 Apr 2026 18:16:42 GMT
SHELL [cmd /s /c]
# Wed, 08 Apr 2026 18:16:45 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 18:16:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 08 Apr 2026 18:16:47 GMT
USER ContainerAdministrator
# Wed, 08 Apr 2026 18:17:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 08 Apr 2026 18:17:08 GMT
USER ContainerUser
# Wed, 08 Apr 2026 18:18:17 GMT
COPY dir:8f93d89558d485d03b81034182d43f2557754598b0731c760b32ca0af365b3c1 in C:\openjdk-26 
# Wed, 08 Apr 2026 18:18:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 08 Apr 2026 18:18:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c52e8dc7185acdf335f3e66a4717a90b37648943d2b2a62e58ac7fb994854cb`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c981a6f75f9ed56a17b30f4ad0d927abacfb8b22b4f1afb6524e8ea30c026316`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8619d6b7f5e7af3351c34b725959bf0183e9058375dea5a8142b3207ab8d4880`  
		Last Modified: Wed, 08 Apr 2026 18:18:36 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b17064cde33ad8eb5a19f7de5af5b266a60638019c915532c8865f9724a7a57`  
		Last Modified: Wed, 08 Apr 2026 18:18:35 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b982e7e2760363f18c3dead1835ea7a7e60fd85e7256482c93a57c01b81f38`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 84.9 KB (84946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d31be68e33cfbc0cdd9001fcd3a3b8bf53e62a516e7ab6e2f06cc929a078fa`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd02bf72fcd7253c32cdb948b464dff67794a8edecc86f81e9f29724d0116e77`  
		Last Modified: Wed, 08 Apr 2026 18:18:46 GMT  
		Size: 141.3 MB (141306852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d438d906dabcabd27b8261eaddce408a3323e5fb441fa609509d669adc8c00ea`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 125.8 KB (125753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b134feb2812a9cbcefb5a3f9e1048d60c96256ab6e978fea45a0fab7818269`  
		Last Modified: Wed, 08 Apr 2026 18:18:34 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
