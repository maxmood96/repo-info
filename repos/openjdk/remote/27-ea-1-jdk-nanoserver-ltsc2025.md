## `openjdk:27-ea-1-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:c062024b770e86fd682f1bdcdb08649b6c2e87584711d637f61d140dd380ac47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:27-ea-1-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:813f0d2f7a30cf808d3271e882099a543dd39494d571c4adf0dc1fc78cc692f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.3 MB (424296100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8577093eb8d81099fee4cb58394f6892b0d4714b53ea5cc27777f7fdbdd2ec3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:53 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:18:23 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Dec 2025 21:18:23 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:18:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Dec 2025 21:18:25 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:18:26 GMT
ENV JAVA_VERSION=27-ea+1
# Tue, 09 Dec 2025 21:18:36 GMT
COPY dir:19d14afdca91419101de212977382a6561545d70f03a447b9d85c65ba4bb2f53 in C:\openjdk-27 
# Tue, 09 Dec 2025 21:18:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Dec 2025 21:18:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3aa2fd9c43d5870304ea449c22f4fbf73f16c064a13e04297c92a2a200461b`  
		Last Modified: Tue, 09 Dec 2025 21:14:09 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d56691594efb0339c3f263c9ec12664fc33f13f62b121d19c73aaaaa74371fd`  
		Last Modified: Tue, 09 Dec 2025 21:19:08 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194b92d8605e91408096468599969deeb5f921a060fb0695acdaf9fc5cdb9ead`  
		Last Modified: Tue, 09 Dec 2025 21:19:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ed6285c23bf465fafbf216c7b009eac77d48f4e7217f641dcbada1296b5c84`  
		Last Modified: Tue, 09 Dec 2025 21:19:08 GMT  
		Size: 71.7 KB (71728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4feb51a53a7fa05d3ddbe474147c4d260690f51ca6eaf22d6f2338117c39cee`  
		Last Modified: Tue, 09 Dec 2025 21:19:08 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07f61631c80fed8471e45e3882ede4c146fc9d832f58b6fc6047ec404367628`  
		Last Modified: Tue, 09 Dec 2025 21:19:08 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1215362fb46c1fa2b3d0993a0db9b4ef66c17d586d51e5fb811c797a5c384aad`  
		Last Modified: Tue, 09 Dec 2025 21:19:56 GMT  
		Size: 225.2 MB (225224414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a99ac96d3f9278cb8e68d5edfa3fdd400ca84a763544876b4a547c264e43a`  
		Last Modified: Tue, 09 Dec 2025 21:19:08 GMT  
		Size: 119.7 KB (119678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a3b22666ea185a643c1297120e5383ecf8b2663fa4f101ad4b1ce7244ffb7d`  
		Last Modified: Tue, 09 Dec 2025 21:19:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
