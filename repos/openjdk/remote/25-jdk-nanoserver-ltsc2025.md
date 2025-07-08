## `openjdk:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:52f8d77df80bd991ffd574cacc31b8247ec6cea5c39cdc0e7b63b91d14b9b79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:038c83266d423215ab50d5db2f150a58f03b8a89d16eebe683843c8b28ab18fb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410808642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0797855484280b1552d2a679d13d91064682c5be726312f02bb24cb912a72c9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 07 Jul 2025 22:14:05 GMT
SHELL [cmd /s /c]
# Mon, 07 Jul 2025 22:14:06 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Jul 2025 22:14:07 GMT
USER ContainerAdministrator
# Mon, 07 Jul 2025 22:14:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Jul 2025 22:14:11 GMT
USER ContainerUser
# Mon, 07 Jul 2025 22:14:12 GMT
ENV JAVA_VERSION=25-ea+30
# Mon, 07 Jul 2025 22:14:19 GMT
COPY dir:3f4870c1d66808f40120812f97095242c2c5faef4fbe09ec60976bc998095719 in C:\openjdk-25 
# Mon, 07 Jul 2025 22:14:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Jul 2025 22:14:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60d98a9cf27920e441a0fd0c82511c8ea060d4b85c499819a3fa7f7bc78c1a0`  
		Last Modified: Mon, 07 Jul 2025 22:15:02 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6221947616d3f3a4e6eb430d409d79b3bca14bd71ff05d0a61a60f2e7e6ed0a8`  
		Last Modified: Mon, 07 Jul 2025 22:15:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206f4182b397555cb58f089e909406842d027360b8b36f478866a643fecb8417`  
		Last Modified: Mon, 07 Jul 2025 22:15:03 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50af49274ca4b99dc26797e19a5a322e6b5f93bcc64f02df29ed5305cf4fa801`  
		Last Modified: Mon, 07 Jul 2025 22:15:02 GMT  
		Size: 76.2 KB (76191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07147119dbd82933fcb5cfdf94c734e0b85a2d8739eab4d22f61010a1d8eb2fd`  
		Last Modified: Mon, 07 Jul 2025 22:15:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e3630787026c525960fb64384d3ce9e45b4368abd2ef3e7264f4065bfd8e52`  
		Last Modified: Mon, 07 Jul 2025 22:15:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a5f525decb545377b7dbcaf606cb01018057d8f6a388e1dbecbf177f4b1202`  
		Last Modified: Tue, 08 Jul 2025 00:23:46 GMT  
		Size: 218.5 MB (218529412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1a3978439a38c4ea46095a3bb23f8cd7403689d9753baca22cfc530f12a95c`  
		Last Modified: Mon, 07 Jul 2025 22:15:03 GMT  
		Size: 114.3 KB (114251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19efbf9df963ef14091861a8bef0a0bec5b987faaa225757a0e6e8a7b6964a8a`  
		Last Modified: Mon, 07 Jul 2025 22:15:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
