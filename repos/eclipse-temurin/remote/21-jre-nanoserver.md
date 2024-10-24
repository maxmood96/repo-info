## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ace2d8e365383bbabaa115bf6823f929f72398437ab00ec514f78944241d9e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:1d05b1e4980511108bc1045f70aa7581acb688f10369bd9d023b2a60f22f9c3e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170269773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bac12f57bd8c8c9848b9c9a2f7dad311ebcabe358fc9eadd5b6cf3c5707672`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:54 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:55 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 24 Oct 2024 01:52:55 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 24 Oct 2024 01:52:56 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:13 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:17 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Thu, 24 Oct 2024 01:53:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd86b35b31f6ce93bdcc634d20f86ce031451d92f153f93b3462fb1e38665f2`  
		Last Modified: Thu, 24 Oct 2024 01:53:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9616c773bbec773cc4a8ed41084c518336b429b18395a5788e996d1b2d9fc7`  
		Last Modified: Thu, 24 Oct 2024 01:53:27 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f41933868a0abfa744e0ed4ae6939845437f9ed0fe12f6e4d89fa1aab3c53be`  
		Last Modified: Thu, 24 Oct 2024 01:53:27 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bff111f67ee223aa38af2bc19ed4e4323f44487c1e1936ee8c9110bd20503d5`  
		Last Modified: Thu, 24 Oct 2024 01:53:25 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38be76c1a2269bdee7452e0c8ca2dc5db44b82df77c233f509c585a633014701`  
		Last Modified: Thu, 24 Oct 2024 01:53:25 GMT  
		Size: 72.0 KB (72001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f2e9fd19bae53fca006b18f58ef6820d6da6b6436f3ba85ae051f79a4b5dab`  
		Last Modified: Thu, 24 Oct 2024 01:53:25 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b925d1560f065060a0c8a0750837e8d5b0620215f4a76ff23f5828193f9f56b0`  
		Last Modified: Thu, 24 Oct 2024 01:53:31 GMT  
		Size: 49.6 MB (49585517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d4488d6d350822a947ced3a0df3517354336c428ac5cc7966ae4ec0266510b`  
		Last Modified: Thu, 24 Oct 2024 01:53:25 GMT  
		Size: 96.1 KB (96072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:51e2b0ee389ced8ea0a8b4882bdf41cbdf10b2db462defce3432a5764ab9965a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208102926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dcf9cd6d936f012d13304af798152727a4d5ca675aed2e1a0af9bbd6513c97`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:53:07 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:53:09 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 24 Oct 2024 01:53:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 24 Oct 2024 01:53:09 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:23 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:27 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Thu, 24 Oct 2024 01:53:31 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5651bf5fafa6f66ce40e4b5d5356dbc83adfdc7fe0d6fd1330f1528ab4e0e7c3`  
		Last Modified: Thu, 24 Oct 2024 01:53:36 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63fc1c454d8e19173d4f2cdcb7e7474bb4e0f3c54de2169f9f20a96ef3045e4`  
		Last Modified: Thu, 24 Oct 2024 01:53:36 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4beec1a9b2348207c6cd4dd63a6bd7ecec61d15ef4011f312b40a68470b1e20`  
		Last Modified: Thu, 24 Oct 2024 01:53:35 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ecc7745dfdd3201043cac660393ff83a4f256e90d8a82c107e8bfe2ed0a9dd`  
		Last Modified: Thu, 24 Oct 2024 01:53:34 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbd70de2fea2fd65f49663581f6c527a51e9bced0a57568f02261b430fd5b2a`  
		Last Modified: Thu, 24 Oct 2024 01:53:34 GMT  
		Size: 67.2 KB (67248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3f218a56bb7c9293bbb3583fa52acda95c62a704541ebeabbf4747cbf1e181`  
		Last Modified: Thu, 24 Oct 2024 01:53:34 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc42bf1fc2835c975affdb99478acc2086ebf65e6fe0f6bad6c8514e0e02eff`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 49.6 MB (49587088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3c4db31b12e68a8e723925fa1e469d5b9d0d26c7fddacc7af64d7e3ff05400`  
		Last Modified: Thu, 24 Oct 2024 01:53:35 GMT  
		Size: 3.3 MB (3349475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
