## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:49567fdb849c9b59df4302b4c4d9afb939c05111239c6587694034637deee26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.6054; amd64

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
