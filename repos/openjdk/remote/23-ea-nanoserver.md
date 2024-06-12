## `openjdk:23-ea-nanoserver`

```console
$ docker pull openjdk@sha256:a772b11442c27ae9bfc555c6805b1507dbb8d747a56cd36bca37e118c7c48e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:23-ea-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:0679718f8f34ad6e1865be87a3e62923faf59f4b6c7b1e98b13368e4a41c1655
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365275443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a3b5162f61d744bef868835b203f538d1045bf980b46fb4f1bda84cf24c81b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:07:18 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 19:07:19 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 12 Jun 2024 19:07:20 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:07:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Jun 2024 19:07:23 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:07:24 GMT
ENV JAVA_VERSION=23-ea+26
# Wed, 12 Jun 2024 19:07:32 GMT
COPY dir:40a82c570517dedd498b0b8d242aa1177d065a56837a01711f48d67cb3613213 in C:\openjdk-23 
# Wed, 12 Jun 2024 19:07:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Jun 2024 19:07:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a8661b3d42028a9ac9ff70cc66a995360cc27ae67bfbd43a6c46fc4b9a7bc`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23633d3731306a690b20a9af480e329aeccd57452272c17e1166fc386940126`  
		Last Modified: Wed, 12 Jun 2024 19:07:45 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bb8e26f92fa6554a0761ae1ca2396fa0e543fcdb2d69816e3598afd0b11810`  
		Last Modified: Wed, 12 Jun 2024 19:07:45 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee0d9b3f4f6bcda59f427abbb18431db6921d4e34b1b140a284a4c11061972`  
		Last Modified: Wed, 12 Jun 2024 19:07:45 GMT  
		Size: 72.4 KB (72406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb07f3dcd5f7c8f45078a823da0e0c41e637a8c5822fbb190ef171812610958`  
		Last Modified: Wed, 12 Jun 2024 19:07:43 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05166e597af711ff88bd122b7e67da02323cf3d74d91473d5d12d562ff77d0a`  
		Last Modified: Wed, 12 Jun 2024 19:07:43 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e829cc3851578f1960768d4580553b1b6576620c15d5ce09dc10fac061dbc7f`  
		Last Modified: Wed, 12 Jun 2024 19:07:54 GMT  
		Size: 206.0 MB (206040431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51d61dbc0535eddc1f0ab52cec1cc23b34ae67d1796281904b4f3fa8bfcdf5f`  
		Last Modified: Wed, 12 Jun 2024 19:07:44 GMT  
		Size: 4.1 MB (4123158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbcd150f852c840b176541aeb497519288391a532b1abbb794d8026ea010747`  
		Last Modified: Wed, 12 Jun 2024 19:07:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
