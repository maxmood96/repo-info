## `openjdk:24-ea-nanoserver`

```console
$ docker pull openjdk@sha256:af393e79c90c1d74579b7fa7e73e650c10b17f93f2fe9ee36f0b47d7b01b8aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:63cff5034d718ce54982df1726a362ad9aaf8a58ef6370452538c2e6434f36b4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367243198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d95f54ab300c7ee90bbd83f9e6f08c9fdde10741b84df64f36f089563665e4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Fri, 06 Sep 2024 23:16:51 GMT
SHELL [cmd /s /c]
# Fri, 06 Sep 2024 23:16:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 06 Sep 2024 23:16:54 GMT
USER ContainerAdministrator
# Fri, 06 Sep 2024 23:17:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 06 Sep 2024 23:17:11 GMT
USER ContainerUser
# Fri, 06 Sep 2024 23:17:11 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 23:17:19 GMT
COPY dir:4f2970b6340f2cfe63b9e3f11a70a1b094e6fbb8d6435dc5c9906911ec8278a3 in C:\openjdk-24 
# Fri, 06 Sep 2024 23:17:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 06 Sep 2024 23:17:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6e406d4ffccb1194491e8a72fa1c08613ede1612b1e37e0c3a75651a96eddf`  
		Last Modified: Fri, 06 Sep 2024 23:17:31 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f0264d3485b64c995902a5ea84d527647dcf6d2363f532d8f30a26a2884cd5`  
		Last Modified: Fri, 06 Sep 2024 23:17:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614b8b223d22f50792fe9d24dd2f5ab13b4b79b4a2cd95180f310b7526b67203`  
		Last Modified: Fri, 06 Sep 2024 23:17:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157ca5e10e379efb4e3d7ded4cee97489e3244d096b6f1b220dd021ba138a7d1`  
		Last Modified: Fri, 06 Sep 2024 23:17:30 GMT  
		Size: 67.3 KB (67280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f83b036cb042c3f909973c86220b7bb6d747d3cb832a4b7e1c11b56f73b63f`  
		Last Modified: Fri, 06 Sep 2024 23:17:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ae2a0a600eb721a4e08f7d0a31538d3c73500998cd0a40bd43f864096c4dad`  
		Last Modified: Fri, 06 Sep 2024 23:17:29 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3eac6db0620578f59da7d76da6c45701436a3a58ec2b0df1c9e4b4d97dbaf5`  
		Last Modified: Fri, 06 Sep 2024 23:17:41 GMT  
		Size: 207.6 MB (207618340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbc76bc249fe7bbbb9bf901ee7e39159fbdb123fd3b9bc4cdb96e192c426394`  
		Last Modified: Fri, 06 Sep 2024 23:17:30 GMT  
		Size: 4.5 MB (4468269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2457e48d7aae9706ff90f40c0a7d4ca38d9c5de9750d29c486a60b9ca656063e`  
		Last Modified: Fri, 06 Sep 2024 23:17:29 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
