## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6ea11a0845c7f0d9e63e12514d1d11f1e833230c55df84dfc88759bc3165995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:4a0fe7c2ef279539ce9ad9e3007851b290c7590b53e8595c8fb533a1081fe3d6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367801595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9caf168b3a329c90722e30f101e7e1aaf896714ba1cdd69ae16d967b892233`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Fri, 11 Oct 2024 19:57:48 GMT
SHELL [cmd /s /c]
# Fri, 11 Oct 2024 19:57:50 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 11 Oct 2024 19:57:50 GMT
USER ContainerAdministrator
# Fri, 11 Oct 2024 19:57:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 11 Oct 2024 19:57:53 GMT
USER ContainerUser
# Fri, 11 Oct 2024 19:57:54 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 19:58:01 GMT
COPY dir:2e661239102df48292f4d44924b25a0ecc91b8bc072d34b4bb2d3da392a9c04d in C:\openjdk-24 
# Fri, 11 Oct 2024 19:58:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 11 Oct 2024 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8988dd04ab0e848fe58361ede780b1ac24b438ac4ad9f81c0321543bd8634137`  
		Last Modified: Fri, 11 Oct 2024 19:58:10 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8026c8d62a1f97a9f26aa3bf9111d271af1246b89f3182b2c8d48046848cdf`  
		Last Modified: Fri, 11 Oct 2024 19:58:10 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36f5538c70282bf9d2f6cf87fdeeb345458eb750e4c76dcb7a9137ab806933f`  
		Last Modified: Fri, 11 Oct 2024 19:58:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f4f2f3c1783635259d15fe0023bfbaab78e23efeeb181ae5e3631d0f566da6`  
		Last Modified: Fri, 11 Oct 2024 19:58:09 GMT  
		Size: 71.3 KB (71269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117427e6d881e42e1240e8c878885225bec513295449cf8f1c174e48cbbc77ff`  
		Last Modified: Fri, 11 Oct 2024 19:58:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2799ca2650c297131000ecdf42ad611e44c85ada118e38609f546c1e9e777a6`  
		Last Modified: Fri, 11 Oct 2024 19:58:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d289ab500dff4ba403014ab33c98511511ca183d56d7fa1c42094fa53e576d9`  
		Last Modified: Fri, 11 Oct 2024 19:58:21 GMT  
		Size: 208.0 MB (208016814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f9600c0c81d43499413eef5c3814ef76c5c73c0f8ea008e1b9ee1981a57926`  
		Last Modified: Fri, 11 Oct 2024 19:58:09 GMT  
		Size: 4.6 MB (4613655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20ea778c274da972e63ac97ec8cb032e73891eebada05f91eb25d423eb090c4`  
		Last Modified: Fri, 11 Oct 2024 19:58:08 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
