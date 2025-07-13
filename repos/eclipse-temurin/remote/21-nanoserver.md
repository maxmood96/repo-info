## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5e8d874f9e3bfbf006f6017f3eed8b7d0c197e0328e2f771c4e30e139a7f3497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.26100.4652; amd64

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

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:d599c668950217f0d21877b7e905935af7461c72f79d37eb0574d5be715f69f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324374646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c2f38457b4a0f8e3cff2cdbdd34af0bca564321ef7d14858362cfce00b9625`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:26 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Jul 2025 19:12:29 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Jul 2025 19:12:30 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:12:33 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:40 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Wed, 09 Jul 2025 19:12:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Jul 2025 19:12:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe2274f38ad1a38bc60861757fc560e37b1f973124cd416e0193f9d0437474`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693823f39d9a8f6bd698c99ef27c224b756b257bfd1c7d1d85e8603e113fcf3`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727cdaa79b87d3729b380e9e080048d75a21f546cb1d39b5f831a3146772d27f`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af172acbb5a1711fdc375d86e5f8438140b66e6eabc5763f293437760aaea4ee`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83758e3be61a8ea514c2885fb741f1df38abb48999cfcb27e02e05f93fee0c33`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 79.3 KB (79325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5daf818a9abeb7e634296b41ee5a75329447958c2374b222f6ffb46b378277`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1915cba74f768d6258dea24021b2ee8d045c0c506ca88696f608a211abe31496`  
		Last Modified: Wed, 09 Jul 2025 21:15:44 GMT  
		Size: 201.6 MB (201551161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a306962865f4875f6b97b2bf2b69d1c34d7a66083519a96f54a79383295c485d`  
		Last Modified: Wed, 09 Jul 2025 19:13:10 GMT  
		Size: 107.1 KB (107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db80a41d93cd97b1810fefbd90d954b1f9ea2edf025b7a77b8e4da21a24efd77`  
		Last Modified: Wed, 09 Jul 2025 19:13:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
