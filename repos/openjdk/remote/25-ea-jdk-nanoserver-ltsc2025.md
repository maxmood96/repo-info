## `openjdk:25-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:57417d310a25f2be7daf6e4deffe17d7d569d9b7b3048f4848078f3049283e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:e85d9ff0d61a0a07d9e5fd76b13f9e3607f9a10bf6a5814dc17611ee95e00f7a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410730074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e545df174c7a5f317a0ea0e00c07583fc93601ea26a4db41f848c5c28c52e98a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Sat, 21 Jun 2025 01:14:07 GMT
SHELL [cmd /s /c]
# Sat, 21 Jun 2025 01:14:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 21 Jun 2025 01:14:10 GMT
USER ContainerAdministrator
# Sat, 21 Jun 2025 01:14:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 21 Jun 2025 01:14:14 GMT
USER ContainerUser
# Sat, 21 Jun 2025 01:14:16 GMT
ENV JAVA_VERSION=25-ea+28
# Sat, 21 Jun 2025 01:14:25 GMT
COPY dir:5401461bb1e2d6bb9fab71a6bf196682408eddda480d435a025c18a8000305e3 in C:\openjdk-25 
# Sat, 21 Jun 2025 01:14:33 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 21 Jun 2025 01:14:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2193bddbbf48905036f2b57e3fa909e32649afcd21f5a99f02272e17455adf`  
		Last Modified: Sat, 21 Jun 2025 01:15:25 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6848fa67f19caa7563f602a599ee89642ea722786f5a61a4354a8c490fe56154`  
		Last Modified: Sat, 21 Jun 2025 01:15:25 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520831085150e5ab965f265efd216f0374962189a0936c88b66db84700633856`  
		Last Modified: Sat, 21 Jun 2025 01:15:26 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ef974d49b0afddf073b000e71a11fc9500808d39abc36f4219bb87ee7f9214`  
		Last Modified: Sat, 21 Jun 2025 01:15:26 GMT  
		Size: 77.4 KB (77357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4847b80161102df9ce3291f0923c26de733edcddbb34a1e9a80fcb4c6196a37`  
		Last Modified: Sat, 21 Jun 2025 01:15:27 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fd15553752c702c01e1bd86fbc57fa9eeeccf38f4e79946699666b64c95cf3`  
		Last Modified: Sat, 21 Jun 2025 01:15:26 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4792d4470e4cce3236a2c30b333c9e1db93ae191fbc62c0cad996477bac6844`  
		Last Modified: Sat, 21 Jun 2025 03:24:15 GMT  
		Size: 218.4 MB (218449812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0938fe1638a7cc199bed554444c141b4e489297ee3b488b125ad4bc638736e`  
		Last Modified: Sat, 21 Jun 2025 01:15:27 GMT  
		Size: 114.1 KB (114087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742ac14035d7faa530596981c8085abef332c1e804a0d5365a116cec17ed52aa`  
		Last Modified: Sat, 21 Jun 2025 01:15:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
