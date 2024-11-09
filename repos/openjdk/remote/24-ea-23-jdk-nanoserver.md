## `openjdk:24-ea-23-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:567c20c6f22623512b1d5c6bf76b696572323311c449906f28be5b13e269435a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-23-jdk-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:7d0c629f15248af61d4cb0efeb4b5953e3d176ff0ff1c0c7bbce5c73743ce47e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369089965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a28249956870f1b5d1fde0b1ea20093a6ad3e8a269abf72371ac5bb9d482ad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 09 Nov 2024 02:51:07 GMT
SHELL [cmd /s /c]
# Sat, 09 Nov 2024 02:51:09 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 09 Nov 2024 02:51:09 GMT
USER ContainerAdministrator
# Sat, 09 Nov 2024 02:51:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 09 Nov 2024 02:51:24 GMT
USER ContainerUser
# Sat, 09 Nov 2024 02:51:25 GMT
ENV JAVA_VERSION=24-ea+23
# Sat, 09 Nov 2024 02:51:34 GMT
COPY dir:7e2236fae53de415a6b985bfcada000d61dbc6a40126a0107213015de3141463 in C:\openjdk-24 
# Sat, 09 Nov 2024 02:51:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 09 Nov 2024 02:51:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93adc2d170633135f22934c2a65425765da7c941a28e9fffb3ab24f3e39cb319`  
		Last Modified: Sat, 09 Nov 2024 02:51:46 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f277592ad03a4a6c5a00b22514bce1132505e1bce43c76c5c90743936a6d4f`  
		Last Modified: Sat, 09 Nov 2024 02:51:45 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d613d2fcc11b439dd981d0f2fde1cf5a1829026a162bc26bb3e1874b62c1c18c`  
		Last Modified: Sat, 09 Nov 2024 02:51:45 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a09f34e3ac39540734ac3e3655803f61a34abe0f794386b9c6acfa0afda659`  
		Last Modified: Sat, 09 Nov 2024 02:51:45 GMT  
		Size: 67.9 KB (67854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2123f41827c3ee4806dc490b4922ff081f173dfb761dff1bfd0efac1c19203`  
		Last Modified: Sat, 09 Nov 2024 02:51:44 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6da8e9cc0f0337aa2c0aaaa3547ae7b448040e41a694da2d4ef9b91b865945`  
		Last Modified: Sat, 09 Nov 2024 02:51:44 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ce8783d37eb704c2efc1bc1a9a472b24a66734f06f915a797b7c70d88a8bc3`  
		Last Modified: Sat, 09 Nov 2024 02:51:56 GMT  
		Size: 209.3 MB (209324716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26c86b629fbf04e6596d27e224abe8484e5d5d0848c24a340ee9f249b632a83`  
		Last Modified: Sat, 09 Nov 2024 02:51:45 GMT  
		Size: 4.6 MB (4597362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fbd37a7e3d51ce75e887c0689ac28afb9ecaa4b3e2e22f0142d1da92e736c26`  
		Last Modified: Sat, 09 Nov 2024 02:51:44 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
