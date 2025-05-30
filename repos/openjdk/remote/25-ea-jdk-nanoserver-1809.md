## `openjdk:25-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:5c66c02b6d76d1dd77c3d5612d5f053780daba7f316a083f63bbdeeb7aa41677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-jdk-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:3c367a9e08593cd951b9c2231401d5aab1048841b4720dba08ba00165be4ba62
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.4 MB (331412661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006165788f48cbd47df2a4b0671a55211c752dcd8021a34af173e89d680eda77`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Fri, 30 May 2025 18:00:19 GMT
SHELL [cmd /s /c]
# Fri, 30 May 2025 18:00:20 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 30 May 2025 18:00:21 GMT
USER ContainerAdministrator
# Fri, 30 May 2025 18:00:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 30 May 2025 18:00:23 GMT
USER ContainerUser
# Fri, 30 May 2025 18:00:24 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 18:00:31 GMT
COPY dir:bd2747e79afdad77e7098a4e268355ea8695f52ce1251320a131b555b1a0c1b4 in C:\openjdk-25 
# Fri, 30 May 2025 18:00:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 30 May 2025 18:00:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124eec2ed1e8d8409ab1fef7bcaa845816b76a5dee2206ca94d59c3b42dd0227`  
		Last Modified: Fri, 30 May 2025 18:00:42 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9559e900538627f18a145cde113fdb7024d7868b15aee12bf72b361d1b54d1e0`  
		Last Modified: Fri, 30 May 2025 18:00:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6e30ce1fbfd6b6193157ce22c002b2b53e5c6ff408d55c6ac42cd2f47c875f`  
		Last Modified: Fri, 30 May 2025 18:00:41 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75015ee0c01bbb9b5596826676fb37f70b43b704788021ddfe6a836a14465901`  
		Last Modified: Fri, 30 May 2025 18:00:41 GMT  
		Size: 68.7 KB (68722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866c1d8aad2e73c70df3b66e6eceec7e4309195d0dd0db75be152a4df40af095`  
		Last Modified: Fri, 30 May 2025 18:00:40 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4402b08344134c4778acb28192f0cd82ae3efe78523141cfadd79c63124eff`  
		Last Modified: Fri, 30 May 2025 18:00:40 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8255162478c67980bfe91a11326bccf3f9078838a488a7278bfdc904ea9c29`  
		Last Modified: Fri, 30 May 2025 18:00:52 GMT  
		Size: 218.1 MB (218116887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47264a84c82ed977f9442eb2db0acd06376c3034d11ca344a9ad6d53bc3ca30`  
		Last Modified: Fri, 30 May 2025 18:00:40 GMT  
		Size: 4.4 MB (4440266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25daf7f67f1bf0365705c73a4541a4615f9b8df7aeaf18828b598bb951d50214`  
		Last Modified: Fri, 30 May 2025 18:00:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
