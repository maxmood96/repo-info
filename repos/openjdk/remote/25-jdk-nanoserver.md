## `openjdk:25-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:00fec0dd7b0b826d48f96fe79c37f5d160889d514a55f2bce47773dee0ae008a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-jdk-nanoserver` - windows version 10.0.26100.4349; amd64

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

### `openjdk:25-jdk-nanoserver` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:7463df8efe71a574fecdd333f59b1b0e1ed2407087fc9bf12aed645039ab9129
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341240258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2230845d1d86bf505274df463f828e53d89001eabf1e3673354e8d294dc028a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Mon, 07 Jul 2025 21:05:11 GMT
SHELL [cmd /s /c]
# Mon, 07 Jul 2025 21:05:13 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Jul 2025 21:05:14 GMT
USER ContainerAdministrator
# Mon, 07 Jul 2025 21:05:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Jul 2025 21:05:22 GMT
USER ContainerUser
# Mon, 07 Jul 2025 21:05:23 GMT
ENV JAVA_VERSION=25-ea+30
# Mon, 07 Jul 2025 21:05:32 GMT
COPY dir:3f4870c1d66808f40120812f97095242c2c5faef4fbe09ec60976bc998095719 in C:\openjdk-25 
# Mon, 07 Jul 2025 21:05:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Jul 2025 21:05:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70278f567fa7073b829f6de00f89a2ea27e611a8c9b506ec5a8bc613ec8a2d57`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33f0ba90b7af44d5aef5052e98e551492ce881fd09b1d2639f789155f47fcad`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22080f33d0d9d46e62e47d67010f55d6f6261a7bd242200acdd3987ada00166d`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb81b1ea9dbb69bf04f3720071eac7e63db4efa7d1f4d78ae86086f222bfb6c`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 74.7 KB (74655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1668992a9950de1b30759249bb201e9be269a05dec989244be37d05b5dae0f`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18d09ee9f135ae5320eb293d9e3d3fe6b195643bc14a2151a069ad9ad93b096`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8038e941cfa34284607608d804eb2cd8edef55001cca4e37638ed003df93b6e`  
		Last Modified: Mon, 07 Jul 2025 21:24:02 GMT  
		Size: 218.5 MB (218530282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efc7e09f5ac668c6097dc66b5030d41673c8f418e3ad07dba08866df0f0049c`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 88.5 KB (88518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3dc67ba4eaaf51cc2aba6cb453b922d4fcabd2743feab2475b8ed143b73a8c4`  
		Last Modified: Mon, 07 Jul 2025 21:06:22 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
