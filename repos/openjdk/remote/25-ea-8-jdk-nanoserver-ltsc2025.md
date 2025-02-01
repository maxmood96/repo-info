## `openjdk:25-ea-8-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:41b9d1a42ff7e94d3ade3dac6eac71d1de60deb382101cbb64e8801cb90f7665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:6656dc6e800001b1953aafa7725cc06e2fcdfd0eab35cefc9413c1b3e19371eb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406702263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d5bfeb80a8324772211fd0d1f66aacbf1a49460df076816a78e92328349abe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 23:32:34 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 23:32:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 31 Jan 2025 23:32:36 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 23:32:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 31 Jan 2025 23:32:39 GMT
USER ContainerUser
# Fri, 31 Jan 2025 23:32:39 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 23:32:46 GMT
COPY dir:0f89cb81afdb881ec0a835597e0e5b8ef37085da6c3213f99555c2a1da7025d9 in C:\openjdk-25 
# Fri, 31 Jan 2025 23:32:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 31 Jan 2025 23:32:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ddc8dc4bc937d78b80c16900804d5218428251cad8529c8b925da31ff547f7`  
		Last Modified: Fri, 31 Jan 2025 23:32:58 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfb467b9b6104db3bc8d9ff623f81c48bd6d07c8fc7265d79d31ab81a85d312`  
		Last Modified: Fri, 31 Jan 2025 23:32:57 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6571afb8831e731b2fd3a3ccab200659b4340073e14b82c9392553b488f1ca57`  
		Last Modified: Fri, 31 Jan 2025 23:32:58 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46276aefa9e06d9b69d7e7334b2c0b1c5668067ec4404f03735da26ec851b3e3`  
		Last Modified: Fri, 31 Jan 2025 23:32:58 GMT  
		Size: 76.1 KB (76079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a1e63569cbbdbd0235d13705d273c8fb97d7d1d364521747ba7b7db8fd8a52`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfaf8691b520b201c830140628948f134191da31a46a1e7f96cd938edc35c86`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11830e09d94cedd95fdc1249f8e9e07d99fd8f30942a61ac8fa9b4f4efda7b3`  
		Last Modified: Fri, 31 Jan 2025 23:33:08 GMT  
		Size: 207.5 MB (207472724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabb2523b460148e2e1fda2cc8aa56acbef4b3f56e68183afd55a377afb82c17`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 92.9 KB (92912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eda93759bb14b8b21347ff8b80ef4c4c6ec18aa77d926669692c8a74fda22c4`  
		Last Modified: Fri, 31 Jan 2025 23:32:56 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
