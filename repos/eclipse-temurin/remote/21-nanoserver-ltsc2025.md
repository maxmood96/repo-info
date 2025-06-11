## `eclipse-temurin:21-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:c24bfa01802c873a822a151e826ecb8d66f321a7204d154ccb7a7739d8fbc015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:21-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:0155af1a845870bd8604778af153ef3b8735e396f82bd81c79b9fddc224455c2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393830328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f871ccf748d1ca2b4861acc11f4f146f311954d745c1b2809016eb8711aade60`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:14:41 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:14:42 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 10 Jun 2025 22:14:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Jun 2025 22:14:43 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:14:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:14:47 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:14:53 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Tue, 10 Jun 2025 22:14:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Jun 2025 22:15:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f01f8ccaeedfa276bc823ea222d03ea47f5961b7770173549e841265ac76f7`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbba9f599eec03ff023de92f8b9dc849a4b7827287de063f7769b77570631ceb`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bba5404bb6fe533d4a67dd40d5c48faf49229c52b4b4c9d1f571b0165031008`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8365f2f8b588bc3c3723cbdc81217eb4558ef90ab33be52d7d136b4c2e528ec6`  
		Last Modified: Tue, 10 Jun 2025 22:15:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f41e941b6eacb5b89809cd0d41c515316f020e62cf83431c8e9574d5ef9dd2`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 75.8 KB (75778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d7ee6fb193e39902d69f5637048fc6d906b01765f5bdb74c4b5177e3d755ab`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001f0812ee97126c43d1e5bbf24ff00fb28797a0667274130c3e1946076839bb`  
		Last Modified: Wed, 11 Jun 2025 00:15:34 GMT  
		Size: 201.6 MB (201552111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bb241dfccc9210f3dc187b54dad6752b18a357d1d173395e56f02026034251`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 113.6 KB (113601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a174b7a8f1816b739a447b4776b1234c03bd508fd8b582118d60eccb7cc8e`  
		Last Modified: Tue, 10 Jun 2025 22:15:45 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
