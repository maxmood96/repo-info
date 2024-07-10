## `eclipse-temurin:8u412-b08-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:28e9f23c1bf4bccc78039efff01b5ba9980e260de45f7fb68ea3f9fed597da2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8u412-b08-jdk-nanoserver` - windows version 10.0.20348.2582; amd64

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

### `eclipse-temurin:8u412-b08-jdk-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:f5ab3e204084e6fa6712f722907855d0849fc0091e94cea71acfeb21b214d7bb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256941451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf1724a4c4a5a0b882dd85e487294e7a8a3562cf5499e75fe12f7687d9b1c26`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 16:38:43 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 10 Jul 2024 16:38:44 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jul 2024 16:38:44 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 16:38:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 16:38:53 GMT
USER ContainerUser
# Wed, 10 Jul 2024 16:39:01 GMT
COPY dir:5498972beafb1de3e4749bc87b064f8ce9cec472aae9e7d0f4643a99f48638da in C:\openjdk-8 
# Wed, 10 Jul 2024 16:39:10 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd3dd1b370e698d233bca9d38691b4d603232ec3e80613b652b90ae272c62aa`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a2b5477760dae20db86c6d6529fa89fcfc8ceb4de0fe7ba849b19ba328c3bd`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d51b65f5511b893cb79015a960daad47e830557616e8335cc43450ce7cadd1`  
		Last Modified: Wed, 10 Jul 2024 17:27:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ff86607556cfacf2fca5f41b5573273f2e2331c55a9d4d898185cf00df449`  
		Last Modified: Wed, 10 Jul 2024 17:27:58 GMT  
		Size: 66.8 KB (66790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49814bb6e0056128b77482bd4ee3a7c198ff64b3e3380fac2f7699330bbf8093`  
		Last Modified: Wed, 10 Jul 2024 17:27:58 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0230ef4839f040031d6bef11748da25f92153e2f990a4fca18ad5277f104cb9`  
		Last Modified: Wed, 10 Jul 2024 17:28:11 GMT  
		Size: 101.7 MB (101700649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15312df7a5f78572b5b3e8aa9bde5f90db232f6676813881419952818611925f`  
		Last Modified: Wed, 10 Jul 2024 17:27:58 GMT  
		Size: 86.9 KB (86866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
