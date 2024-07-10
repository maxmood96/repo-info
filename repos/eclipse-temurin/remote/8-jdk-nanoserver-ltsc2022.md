## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:867744d2aa76e50f004e8f14dd909bcb7b817f4dd099e910b8d7e4f972b18699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:3783f5afe4068358790987d9da9497a39f230335a3a635eeb9093fa12311e551
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222333514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429ba577985220d4bd613e1dbc253106f7fa6099adf6806f89b242639add045d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:17:20 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 10 Jul 2024 17:17:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jul 2024 17:17:22 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:17:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:17:34 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:17:42 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 10 Jul 2024 17:17:55 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b07b4ab2b5c1253e760d8d609ce086416c7f607dcd785ddc10ae04fc6dcf43`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466a2a5b4537cebbb010784b348c6d9dcd47b4f8d69d7cf47584a4b2b06a7e1e`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349dbf14a3f3dbc38bcf98fa084b4075217e8f81a60abc6a8419f18e28409955`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44202090d90884ecdf62a2ed28b786bc9682ca7d588cdc44d14ebe2faee6ba39`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 76.1 KB (76072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a2df7fd32b943df2a978a5227c92cbf590367f08819a2f021c1eb239e4ef10`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881702aaf6572648248494336d288c773891745d6c6324b72ab9925210406a65`  
		Last Modified: Wed, 10 Jul 2024 17:38:59 GMT  
		Size: 101.7 MB (101700277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0565844c1a915c3864d36452eeb24aeb1a57d055cdd3729d3182a86e06aa697`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 61.1 KB (61083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
