## `openjdk:11-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:cd8d40eeccc8aeb8cdfb5a9712d33a2ae245b1dba0d1e8d3172499e634e2d303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `openjdk:11-jdk-nanoserver-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull openjdk@sha256:df64b2eb5bd58d08e2cf6031ad61eecae3885a725321a15bad59f6c7fa1e4574
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293871915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf055a8921211c6228c3c24d6b09def59689fd80e2f107fb5ae0afdcde6c4e0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 02:53:30 GMT
SHELL [cmd /s /c]
# Wed, 14 Jul 2021 03:18:47 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Jul 2021 03:18:49 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 03:19:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Jul 2021 03:19:06 GMT
USER ContainerUser
# Wed, 14 Jul 2021 03:19:08 GMT
ENV JAVA_VERSION=11.0.11+9
# Wed, 14 Jul 2021 03:19:26 GMT
COPY dir:fc1da1b67a232358030ccafe9e40cca6d0f12faab32f5871879cc4fd6550b119 in C:\openjdk-11 
# Wed, 14 Jul 2021 03:19:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 Jul 2021 03:19:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d8754fb12dd351c91bed29d92c703cddb135a78d8f056b6a3bf13a251c1d2d`  
		Last Modified: Wed, 14 Jul 2021 03:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe8e02e3faa5ffe937981f50a3277b0002846576df467ba8249d6f2b31304d8`  
		Last Modified: Wed, 14 Jul 2021 03:55:22 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ee577adaec81f9c2fc86655503a1a6c8f61898b66788f16a75115f54b86a70`  
		Last Modified: Wed, 14 Jul 2021 03:55:22 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1095968790bd405f2a988693d7983d88c75c1c828991e0bef3dc30db4960240`  
		Last Modified: Wed, 14 Jul 2021 03:55:22 GMT  
		Size: 65.2 KB (65235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0600a4c7c20741a18bd07b8b940ddd0dbe295deae0754a43febd281fc6b81e`  
		Last Modified: Wed, 14 Jul 2021 03:55:19 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648d362abde28d55d5339786af6cd5820275de78289b4377405d16dd4eafa0b9`  
		Last Modified: Wed, 14 Jul 2021 03:55:19 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb45a28915d585f380dc6d49083544feb0468f808e425ef177592204d6ac998`  
		Last Modified: Wed, 14 Jul 2021 03:55:39 GMT  
		Size: 191.0 MB (190985992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79a430384cf335e66c7b5367463f53026d7f5ce58722e56d634816ae7d01072`  
		Last Modified: Wed, 14 Jul 2021 03:55:19 GMT  
		Size: 88.1 KB (88082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7852b5cdd3ec89ede5afeef8c61f2378c938d844a3227e04a18f48667fa3611a`  
		Last Modified: Wed, 14 Jul 2021 03:55:19 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
