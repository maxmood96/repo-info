## `openjdk:23-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:83ee038732bb270e809f02916675b43b1ce09871df964a5af3a780e9016b987c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-jdk-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:8220f22b7afed4945db205f5124b98d92436cb7e105b108e2f7048962fa63033
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (306037072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8689e45671d0cf80a8b09d3416e20cb769eb97a4e06d72a986283dff29a4df30`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Sat, 13 Jan 2024 02:04:04 GMT
SHELL [cmd /s /c]
# Sat, 13 Jan 2024 02:04:05 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 13 Jan 2024 02:04:05 GMT
USER ContainerAdministrator
# Sat, 13 Jan 2024 02:04:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 13 Jan 2024 02:04:08 GMT
USER ContainerUser
# Sat, 13 Jan 2024 02:04:09 GMT
ENV JAVA_VERSION=23-ea+5
# Sat, 13 Jan 2024 02:04:18 GMT
COPY dir:cf5ac9dbf0c132e5638c82efcfa59e7919fe50a912c84b55131d99f2212d99e6 in C:\openjdk-23 
# Sat, 13 Jan 2024 02:04:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 13 Jan 2024 02:04:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8227dc0ddc5f679a069f3842fb610fb5943b30c6d1f6da47092c266d183d0a`  
		Last Modified: Sat, 13 Jan 2024 02:04:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029569bfeebae7c123054b148caf78477ca9fb5954fe46e9e4322d710e3552ee`  
		Last Modified: Sat, 13 Jan 2024 02:04:30 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd672e9299051711f26b3bc1837fedaa0e92610c6e358c7793f44cbc1151187`  
		Last Modified: Sat, 13 Jan 2024 02:04:30 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b9e8301514e18d30be05ebada24bd1b83be34633e556f2221151d56a9d7dec`  
		Last Modified: Sat, 13 Jan 2024 02:04:30 GMT  
		Size: 71.9 KB (71929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc26069bed9606910702399f7f44ac41766a41d9b8d6ac147a02d5adf44034c`  
		Last Modified: Sat, 13 Jan 2024 02:04:28 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670b5c9a5a9a529c8dbf0d878af7de7ef6d738b21d550a1f181b1b6ba2847b07`  
		Last Modified: Sat, 13 Jan 2024 02:04:28 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8e82706bb520eb1aa6fedc72ed247097bfbfb2c66f92a2ae47f691ab483f9`  
		Last Modified: Sat, 13 Jan 2024 02:04:40 GMT  
		Size: 197.5 MB (197499479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435f9478c76825efe414aa64e4a2e09f60ebfa4ce6e6d567108e866714dd56ed`  
		Last Modified: Sat, 13 Jan 2024 02:04:29 GMT  
		Size: 3.9 MB (3868196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3f0e7a752e8ce6f2b746a9b67dbbe7703c5935bf9152abba63a2e8af3c3b27`  
		Last Modified: Sat, 13 Jan 2024 02:04:28 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
