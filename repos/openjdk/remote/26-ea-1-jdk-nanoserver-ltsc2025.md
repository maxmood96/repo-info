## `openjdk:26-ea-1-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:29afcb57d96937bd55c457a5b3ed553139959dc83491fd9dcebb66a340e27ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:26-ea-1-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:fc411099f4d5872e09e62f456bc1e9262dddd60d258381f432c26c8c4c69aa77
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.1 MB (410139869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c2de2b9286967ae609d740995dd9357e204cbdf5fbf671ba410e560ff5d50f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Mon, 09 Jun 2025 23:12:24 GMT
SHELL [cmd /s /c]
# Mon, 09 Jun 2025 23:12:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 09 Jun 2025 23:12:26 GMT
USER ContainerAdministrator
# Mon, 09 Jun 2025 23:12:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 09 Jun 2025 23:12:30 GMT
USER ContainerUser
# Mon, 09 Jun 2025 23:12:31 GMT
ENV JAVA_VERSION=26-ea+1
# Mon, 09 Jun 2025 23:12:39 GMT
COPY dir:457747d16cd2fadf291c9e74f2db19f460bea57b69501abf66c1c6daf147dfd2 in C:\openjdk-26 
# Mon, 09 Jun 2025 23:12:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 09 Jun 2025 23:12:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bebc050849d2b6aea24f180172b64b8047f7cd1ab43105aad9fd1883699401b`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feefadce58e972b4944e795d9c36295ba9840be4f08fc75b2442e380b6d343e0`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f719f61be2afee3ed457203f2e0130a6715a186b2c9ab807ddf9237c490c6566`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaec0693d062e0a72738e74b6c95ca05f78380493e5aade94c4fc5be9b14b3dc`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 76.1 KB (76070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e08ef0c68b9f6718a3c806b47d902ac945fcd009d4f2b1536679b88665560dd`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b883646337141eda167b46ae24e45b3d9f76a3f769a9ef5f4a32e6cc511c0d6`  
		Last Modified: Mon, 09 Jun 2025 23:13:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f1363c6d58a3c69de6c37735f2766a594b7e7fe6d702abac5d7337ef721595`  
		Last Modified: Tue, 10 Jun 2025 00:26:06 GMT  
		Size: 218.5 MB (218529233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e6fccd1d614790b0ad93ba2a75e8fcf209c338e8635a699bd3ecd1b8869747`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 116.3 KB (116258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d514d351ad2c5e76b15a7a6bf7957a03dc37ca17b39bac5f822a04031001b598`  
		Last Modified: Mon, 09 Jun 2025 23:13:37 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
