## `openjdk:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7417f73da351e22fd5008a60b0097fe01d71c99940de659a5e90473b8cae1978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:b34c912b950f657ef1b57669aae51b184fcdfc53285511167c0f1ce06848eef7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341178198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1beff44253b80e2fb254da657e2cd9c3b145432cbbbbd7e5e5d7f5c00c78d9d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:19:20 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:19:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Jun 2025 22:19:22 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:19:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Jun 2025 22:19:26 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:19:27 GMT
ENV JAVA_VERSION=25-ea+26
# Tue, 10 Jun 2025 22:19:35 GMT
COPY dir:2a5431c9629d8e59dc59f707822e3e4d9048b856e0212fd4224a68120121ffaf in C:\openjdk-25 
# Tue, 10 Jun 2025 22:19:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Jun 2025 22:19:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f15b792c70a32caae9a5657ae6244a801151f95365a609ca2210c4198cc7c9a`  
		Last Modified: Tue, 10 Jun 2025 22:20:25 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be69bb47c72187b74f58a3a6749a40fb8434f537932779df73614d93e3634aef`  
		Last Modified: Tue, 10 Jun 2025 22:20:25 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b6d3d55a8e1353c23a53976e980f2fb1cf0852e43f116d27c05dbfd1458a59`  
		Last Modified: Tue, 10 Jun 2025 22:20:25 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bec947ebf10b565a5577bcf67351b0814523e493d89c88aacdf1496f465b90`  
		Last Modified: Tue, 10 Jun 2025 22:20:25 GMT  
		Size: 80.1 KB (80059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b796ab9894733547ef2204cda8b5f9ab79d0db5426c2e99a635aae17ee1d4c0f`  
		Last Modified: Tue, 10 Jun 2025 22:20:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e37c7c3944c45961b05acf1c8d0cf1d8bfac4c61574e55b98aefd4f7fe1f8a5`  
		Last Modified: Tue, 10 Jun 2025 22:20:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4243c1345dd03c2da43e4af9dbefce17c7e5f8f0f433d0bcb1216ec7849c95be`  
		Last Modified: Wed, 11 Jun 2025 00:23:55 GMT  
		Size: 218.4 MB (218443974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89471b680a9342d3ab196affb34a9f03b507aabf05318460e1bf5db3988eab5a`  
		Last Modified: Tue, 10 Jun 2025 22:20:26 GMT  
		Size: 107.2 KB (107233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff0879cd07463acafa594e06d4690ee223ae6afc0a0c2fee1c3ac2fe3b0edeb`  
		Last Modified: Tue, 10 Jun 2025 22:20:26 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
