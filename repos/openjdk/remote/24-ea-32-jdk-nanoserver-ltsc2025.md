## `openjdk:24-ea-32-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:3dfdbe269049d0fa060c74fdbf4c97e76adb0417f231684db093762874e40b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-ea-32-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:7c418f94525150b0de229c87baa48ab4eff9c7b16637d0296a035e881323bf34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407729479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19c4e3b6e5fae62e771d6d5db18ed2f4390a5f72d700ee4ef7fae98d5c6c9ac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Thu, 23 Jan 2025 23:12:13 GMT
SHELL [cmd /s /c]
# Thu, 23 Jan 2025 23:12:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 23:12:14 GMT
USER ContainerAdministrator
# Thu, 23 Jan 2025 23:12:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 23 Jan 2025 23:12:17 GMT
USER ContainerUser
# Thu, 23 Jan 2025 23:12:17 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 23:12:24 GMT
COPY dir:86d923ef445b254beb0a3a098fc78a6b4825f40d8c18f13f837cc4a7df771680 in C:\openjdk-24 
# Thu, 23 Jan 2025 23:12:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 23 Jan 2025 23:12:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f917ac7a32bf48c832a0ba0c239739d2c45590c0b226f2c563e65acbc676c59c`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb67ef85e47db4d2a778df2ad9372bb3d44717e804859ffaed503fbae55811f`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8192936863631a5175ca6787b49593875c3eeaf6c27a2f30e70a6fadf91b12bb`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e44fc286a5d790b0e1027e0f63930823879e7cdb9891f8097431a1480c85e93`  
		Last Modified: Thu, 23 Jan 2025 23:12:35 GMT  
		Size: 75.9 KB (75895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2fb306b6b7f337040eb8aa771edf924263230401893c3da1d6ed5c660b0b60`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d252c87bd13f23b6fd2458aec45bc2f1c7738dafd04e8c672d53af22cbcb5422`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe25d95442b33bb386d49e678441b6b7eabb2d32b619f74df1f07d95ca336141`  
		Last Modified: Thu, 23 Jan 2025 23:12:45 GMT  
		Size: 208.5 MB (208489020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efd5c606a068b39d4ea414f7220d93200cd07bdfe086b6262ffe4dddf430c7c`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 104.0 KB (103997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7607673a60f6efd7dd945944bb03d5b29d56c41ddb066e17369e50869f80b6`  
		Last Modified: Thu, 23 Jan 2025 23:12:34 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
