## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8142f4690bc1d48e00afa4ee723da4e81a4d8a0989c0faabceef44f7189fbcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:ef6397bbdc5ad7b44248ea9ab1927bdf6765c5476c36ee617a5031f1345949da
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359758593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e9db3ee97732e144d265659ee941eb997a816e20ee43b57f314ea1926063f3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:56:26 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 11 Sep 2024 00:56:27 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 11 Sep 2024 00:56:28 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:56:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:56:36 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:56:51 GMT
COPY dir:a4ffd7e89e4f3b2e7536e802b1dd43338b71e63559dd6ffcb51f99d655bc67fd in C:\openjdk-21 
# Wed, 11 Sep 2024 00:57:28 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 00:57:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b92e12c8f6ec07a21a2271d3953b9e4199d822f6336369d764ad7fdc1bf812`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab47d59758ea3159f4898e3cd3a8372bd6483dd1d570fb9bfe683d653a042c6`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d00b86dc2ec21fdab4595f7240c2ff0ff21ff173e345376c512154bea1054b9`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08c629607bc5b9c1be71f291aed5469a2a49e901959d71212f8677ed9de5382`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 68.4 KB (68440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfa7f4fb49e97d65a836414e690c0ab71ac0f6e67d8f65a912dc39cc2932f7`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f232700620fc4e06a104ec6f35e9770dae1efae8f4b6801b9e7d30d9a22ee31`  
		Last Modified: Wed, 11 Sep 2024 01:29:14 GMT  
		Size: 200.8 MB (200777394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff28b07ca7a36e32f266309369f8ea30aa5caa821a4ade9a3ba106aea1528cd`  
		Last Modified: Wed, 11 Sep 2024 01:28:57 GMT  
		Size: 3.8 MB (3824995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9966a30486c75029f215f3cecc8633fc576bfad79e08102f461079dc2b786f2`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
