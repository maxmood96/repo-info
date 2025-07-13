## `eclipse-temurin:21-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:6b01c4f141d3f243c5bdda7ad0ffebb4c14e939d4f337b7fb0ae669e2fd8c814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:21-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:e4b50d3377e3fe6b7b19c99cb7bc1068f18802c97cc5b11ffffc87ea08d9ee58
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.9 MB (394899279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d85a9f7b53245ff629c4b86e9da4bc56badafc45816cf18153cc524a3461b9d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:17:39 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:17:40 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Jul 2025 19:17:41 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Jul 2025 19:17:42 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:17:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:17:46 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:17:53 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Wed, 09 Jul 2025 19:18:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Jul 2025 19:18:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88fd31e1ec99c4053e4a04913ad10bfbb2b205ace6fdd874f82783b365faf1d`  
		Last Modified: Wed, 09 Jul 2025 19:18:31 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f002e96a6521913948e6df1de6c0a074f6b5b4181ca85cfda336b1a43e57ae`  
		Last Modified: Wed, 09 Jul 2025 19:18:30 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932e8b69c1788f724f9d5ba4681be59da4edc6ca8f75bc972820c2def46a433`  
		Last Modified: Wed, 09 Jul 2025 19:18:31 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c057a8f0a6836e5de2154d03ac9c1359803400a4a87a4a18924691af6587d2b`  
		Last Modified: Wed, 09 Jul 2025 19:18:30 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73845858353a9e799087dc39869fad5229be2db482250bd1b75bcf3d9d64fa47`  
		Last Modified: Wed, 09 Jul 2025 19:18:31 GMT  
		Size: 76.0 KB (76023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62d002af26c80e3e3386ed0240018485fd9104be78121ca30176e2a9c4113d4`  
		Last Modified: Wed, 09 Jul 2025 19:18:31 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391a4ee5d1dcba157f9a106bf8efa6b332a0de91da95d7d95b4cb45d3610a6cf`  
		Last Modified: Sat, 12 Jul 2025 23:49:48 GMT  
		Size: 201.6 MB (201552337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39459e25e45c35f7ae009766d74c7bf44f3bc9bcefce9e5e1a309894e46fa34`  
		Last Modified: Wed, 09 Jul 2025 19:18:32 GMT  
		Size: 114.2 KB (114242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfc196783f3a985c87d348808c7e13fb021b29b06c223e002ebcd387b4d31bc`  
		Last Modified: Wed, 09 Jul 2025 19:18:32 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
