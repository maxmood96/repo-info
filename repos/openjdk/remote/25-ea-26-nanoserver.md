## `openjdk:25-ea-26-nanoserver`

```console
$ docker pull openjdk@sha256:cd44818d1e72f3a7fd457c5ea764173a3d24c170be52923ea7ff9dde57706fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-26-nanoserver` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:ac6df361dcf03aefaf832636ac9ec184866a5e2a26f57e236398718aaea56cb1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410722434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adb21c0e084735690011d77b731f9e391aa3384893c58cf2dc22e513e956c1c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:07 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Jun 2025 22:15:10 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Jun 2025 22:15:16 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:18 GMT
ENV JAVA_VERSION=25-ea+26
# Tue, 10 Jun 2025 22:15:28 GMT
COPY dir:2a5431c9629d8e59dc59f707822e3e4d9048b856e0212fd4224a68120121ffaf in C:\openjdk-25 
# Tue, 10 Jun 2025 22:15:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Jun 2025 22:15:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b5ac83507b673505f004dd89033c360582e5618c4840d7a181f1f6ad22b707`  
		Last Modified: Tue, 10 Jun 2025 22:16:31 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba89929126fd534632face073b9a910ac81219b89624f9ef5f08be22bebabc`  
		Last Modified: Tue, 10 Jun 2025 22:16:32 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c362e746e2340b68691fba051a6567dbcc69b9436ee9481124fa095676c7632`  
		Last Modified: Tue, 10 Jun 2025 22:16:32 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab2cc9a92219992e17eaaf1ad07ac919a3ac727509f56d5897919b803f4bcba`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 75.8 KB (75831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d502afd814c3cd3a4e18b6d603cd08812411f0ebebfb0a0e671382e1537b31c`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e23dbe848b0aaedb55a3768876b07347cb313e5aad67f30c32f3e3ebeb0b5`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6d9f88d05b368bb4ad81064b2c55a2d48971bc6656768a86b2eaec2a9e28cb`  
		Last Modified: Wed, 11 Jun 2025 00:23:54 GMT  
		Size: 218.4 MB (218444354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b972f3bd2b070eb7e8697d961a8f369a3fdaf67ce2e076bc8c3e9d892314414`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 113.4 KB (113419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126316482b7d4cbf018959d45cd0a6a78a7eb90bb7627c80cd4dcbf7d1e7def2`  
		Last Modified: Tue, 10 Jun 2025 22:16:33 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-26-nanoserver` - windows version 10.0.20348.3807; amd64

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
