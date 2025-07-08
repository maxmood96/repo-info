## `openjdk:26-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:a39eb8593e9ab5716714ba3399c53fbd387cb5761f1e57a1890dfc690373ff85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:48a967f1f7c71f9107983efb2c5b1f4ad1797a49bf2b956bcd8c632316389f48
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410762372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eea38c368b423c0f9c8780843a154027a9317d27bd74b9837b9d4515d2508aa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 07 Jul 2025 22:13:48 GMT
SHELL [cmd /s /c]
# Mon, 07 Jul 2025 22:13:49 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 07 Jul 2025 22:13:49 GMT
USER ContainerAdministrator
# Mon, 07 Jul 2025 22:13:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Jul 2025 22:13:53 GMT
USER ContainerUser
# Mon, 07 Jul 2025 22:13:54 GMT
ENV JAVA_VERSION=26-ea+5
# Mon, 07 Jul 2025 22:14:03 GMT
COPY dir:a8af305eda69ca7e4a97e843a96509e487ef158cc8b5f27ab7de11cd1f4c0ba7 in C:\openjdk-26 
# Mon, 07 Jul 2025 22:14:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Jul 2025 22:14:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44036ad8b30f4270e47559fda5cb64c44caf7c766c5627ebc0977a548bccd0bb`  
		Last Modified: Mon, 07 Jul 2025 22:14:49 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541881420f521b01b600d45c46e0691af41d6d3c132e60fad5ef7c7b2ebc4bdd`  
		Last Modified: Mon, 07 Jul 2025 22:14:48 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4a0540e05e333c0a0d08d7cdd245be1e2b5f8cb7541c3725a01ab08e4a36c6`  
		Last Modified: Mon, 07 Jul 2025 22:14:49 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cdddb1ba7c56b2fecc4200a090143ea7e4a31478d73bf014a8e34403873a12`  
		Last Modified: Mon, 07 Jul 2025 22:14:49 GMT  
		Size: 75.8 KB (75776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d37aedc407d8209442eff475ee9e4fed9260b0a34f52a088af6223ca72fd47`  
		Last Modified: Mon, 07 Jul 2025 22:14:48 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13186ae846bd211069e358f3669bc93e73b8fa2c8a34d278a09f2de3a4fb3b49`  
		Last Modified: Mon, 07 Jul 2025 22:14:48 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9373f6261b982390b88fe433432f0e2f059ee4934fb622fdc08021d76e901a9d`  
		Last Modified: Tue, 08 Jul 2025 00:24:49 GMT  
		Size: 218.5 MB (218483785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0190ad60f645184c450f581cab974384d0ec3425e2e3e8a6754c1b83c28f198`  
		Last Modified: Mon, 07 Jul 2025 22:14:48 GMT  
		Size: 113.9 KB (113930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2450d85243a1064b9e396d2b93a909220210376c1a9190f3162af47adca255`  
		Last Modified: Mon, 07 Jul 2025 22:14:49 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
