## `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:42f5ea0385676a0cb1180c6e27de331b44c2f8ad0755c2368d7909cb6b2e4be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:8u442-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:58c49e8b09b5d4c8b9f40b76317b4dd65a411ffe610878d9aa57470dd959d7d4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161436651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac63d75b3c9b496d2b96f334c8522f7342592db70101beca9cfd7e489c0d22d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:26:23 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:26:24 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:26:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:26:25 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:26:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:26:28 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:26:32 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:26:36 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae632334bf112f435189793d6894283d928c18f1a290fc77842c2ed6d3048a2b`  
		Last Modified: Wed, 12 Mar 2025 19:26:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c906bcd06f0137cab4722e2d20cd2895877059bc83ee5065fc5a55c2a983e96c`  
		Last Modified: Wed, 12 Mar 2025 19:26:39 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6816c07da7288f774c3b8c6eef67da40a7c9ae3f484fb348eb3759f7d6c37d`  
		Last Modified: Wed, 12 Mar 2025 19:26:39 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914e31054b061396dc27c834532798a49a4f565b45c7e485731e67226c5e39b0`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0cdc83d30946b1e7ae564d1da0ee66c5661239ea3992863ad2c9c17e5aeffd`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 76.8 KB (76750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac1085568eeb3c4bfaa4053fce18def95d70ab6eda479c229d57b85d76b8f73`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bc5c4ba731749d0a057a410a6e11aed288c80a3129b1a99e67c2e89e9b8d32`  
		Last Modified: Wed, 12 Mar 2025 19:26:42 GMT  
		Size: 40.6 MB (40552261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ace66d996afeb53b4f34816caf69302eeed7b1e70036e5d71a1055b6e9cd4c`  
		Last Modified: Wed, 12 Mar 2025 19:26:38 GMT  
		Size: 106.9 KB (106948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
