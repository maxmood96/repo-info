## `openjdk:24-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:b8c1a3b06e3b86076a5e1c99a26f8d1a5e53ca08b56f14ca2d4f9ce2a357747b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `openjdk:24-ea-jdk-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull openjdk@sha256:91bca40de0bdc0e5888e90646212bdf7679e4b3a48d3b8ae86a48030401b3d84
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367978001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec1baa4a1fb9e0b762e748fb7c1f858112ce33cf096b92b85faa87f2b34bf1d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 26 Oct 2024 00:49:02 GMT
SHELL [cmd /s /c]
# Sat, 26 Oct 2024 00:49:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Sat, 26 Oct 2024 00:49:03 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 00:49:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 26 Oct 2024 00:49:08 GMT
USER ContainerUser
# Sat, 26 Oct 2024 00:49:08 GMT
ENV JAVA_VERSION=24-ea+21
# Sat, 26 Oct 2024 00:49:16 GMT
COPY dir:c12edf00fb62ed8180b479f52df78f482cd0e38f0a2747d742e6d206b0a62351 in C:\openjdk-24 
# Sat, 26 Oct 2024 00:49:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 26 Oct 2024 00:49:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1eb9c6e8b02e08eedecc50c6222976922f5a97d2f7fb476830618a7359077d`  
		Last Modified: Sat, 26 Oct 2024 00:49:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7268ff7b12465dc6e22cd4ce0761ab3f802d9d0f9e955aeba08ff19322d7e95`  
		Last Modified: Sat, 26 Oct 2024 00:49:29 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2b1bccf1a08ad28f999bb9a465cc06c47309d62168406a4048ec19bc03b887`  
		Last Modified: Sat, 26 Oct 2024 00:49:28 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9bc087f92672561ab9d758263c080d5e75d8b063b44e91c26b58effaa6cbff`  
		Last Modified: Sat, 26 Oct 2024 00:49:28 GMT  
		Size: 66.0 KB (66027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80a1704b602c8808aa7253207962b7529ddc1263534f21d13175a0327e930fb`  
		Last Modified: Sat, 26 Oct 2024 00:49:27 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22897ccffe72fae4a7a1ef3c7ae0b661e42bd3e0d6b17e854df620efb7c5476`  
		Last Modified: Sat, 26 Oct 2024 00:49:27 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e34e57414ed5d78ae2e049dff90f98c7205eca1839f7dbe7997f1d24194a00`  
		Last Modified: Sat, 26 Oct 2024 00:49:38 GMT  
		Size: 208.2 MB (208208243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b0479227dfd1983dbdab5f56713540812f77f7ef4ab063c4ccec0d74ba96c9`  
		Last Modified: Sat, 26 Oct 2024 00:49:28 GMT  
		Size: 4.6 MB (4603883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00accba26809a9ba1e43c6e9eb16165091d3d4d39a2c48cc0202ee2c84219c7`  
		Last Modified: Sat, 26 Oct 2024 00:49:27 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
