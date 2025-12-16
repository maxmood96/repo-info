## `openjdk:26-ea-nanoserver`

```console
$ docker pull openjdk@sha256:a21f15ba3a2feb57d2ceadf5750bcf4d2db46793ff917328dff3452480843e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:2beddd2233e9cd8a9098678091a4e3c5520082db65af86329ccfb22917264d02
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422897851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bf583877944e34d508092c282fbc8f18d721bbffc42b664a97d50a6130bf07`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 16 Dec 2025 01:09:47 GMT
SHELL [cmd /s /c]
# Tue, 16 Dec 2025 01:09:48 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 16 Dec 2025 01:09:48 GMT
USER ContainerAdministrator
# Tue, 16 Dec 2025 01:09:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 16 Dec 2025 01:09:55 GMT
USER ContainerUser
# Tue, 16 Dec 2025 01:09:55 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 01:10:30 GMT
COPY dir:eacc860438b809f9859b19e16ae39a947eb51a2178590a6f10254cdc1bcc414c in C:\openjdk-26 
# Tue, 16 Dec 2025 01:10:37 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 16 Dec 2025 01:10:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3806e5e70ef53bf57ac133d64c6630554cf260d0b0feb9af79e0888e162db0e6`  
		Last Modified: Tue, 16 Dec 2025 01:11:48 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aca84cb5ef525b6246dd2503ba0a85b938623115ebd617a9e62c0ad31fd1ecd`  
		Last Modified: Tue, 16 Dec 2025 01:11:47 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f622438ebbaf3ab404fba7753a069edfb00a25306a5fff6750bea1d06c46629d`  
		Last Modified: Tue, 16 Dec 2025 01:11:47 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9c0343f71b38034e1fdc7c0b48bfcc5de2b905a6db6c6fd840f1b19ea16382`  
		Last Modified: Tue, 16 Dec 2025 01:11:47 GMT  
		Size: 72.7 KB (72699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8bae78161c73813d759d88e10a575714cb9cca130cee5b7d8e21762e5c06dd`  
		Last Modified: Tue, 16 Dec 2025 01:11:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18faa061b63522e7b2230a93ba38ed12faf7fb2d3224cd7b9a2e432e1c539ab9`  
		Last Modified: Tue, 16 Dec 2025 01:11:47 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d73add33b1e66c79336ca91de557db402aadb0265776a97b47feb8af578a2b6`  
		Last Modified: Tue, 16 Dec 2025 01:12:15 GMT  
		Size: 223.8 MB (223830634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f09f3cdd5cc847f742a0c9f3deda21b53404b91b70292265a5178220c275d5f`  
		Last Modified: Tue, 16 Dec 2025 01:11:47 GMT  
		Size: 114.1 KB (114110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd26c37b39470c61661ebca56571286326f363d1b3ba0a0ed4748f18a711fea`  
		Last Modified: Tue, 16 Dec 2025 01:11:47 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:1a1664c45ce829b48bfbb09a9b3027cefc44ca0ca183596d59887b5a0d0f96cf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350354213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f39722aab2d7608ce99bd7c8a9fa0c412fcabfcac43b458bba329c5f58b5764`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 01:09:34 GMT
SHELL [cmd /s /c]
# Tue, 16 Dec 2025 01:09:35 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 16 Dec 2025 01:09:36 GMT
USER ContainerAdministrator
# Tue, 16 Dec 2025 01:09:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 16 Dec 2025 01:09:44 GMT
USER ContainerUser
# Tue, 16 Dec 2025 01:09:44 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 01:11:14 GMT
COPY dir:eacc860438b809f9859b19e16ae39a947eb51a2178590a6f10254cdc1bcc414c in C:\openjdk-26 
# Tue, 16 Dec 2025 01:11:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 16 Dec 2025 01:11:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1534c7635137aae9170bdf1c71b679926ddb9fe813e926158a336cb217fd1d85`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d428a5c454ac7ae01c53db0626e9d8230d3f0f04eeca27bf7b3881ee58f10d68`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581bf41afe080927253db1cab89ebc70efef2c14a42ca627f9efd694b8574273`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400db2004eaff1ed159a420b62722411b74e70308f10fae27e392e647361f799`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 65.5 KB (65455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4746aa5035b6788ada4f7632079cd07b269c77aca6fb07ef6f7cc2fd9add921`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3071320c70dd29652f1f3632016ece1572d218c8b0a7de739f0c8b1ce8661170`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25c0bc1b5f938f5bf48bce75866ad380d9f2b79275b198664e15fb8985d6391`  
		Last Modified: Tue, 16 Dec 2025 01:12:43 GMT  
		Size: 223.8 MB (223831325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b908b3a7d6c39d215914ce8c33c302ad63353e80c2e31879230bf24097ea4fc`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 92.7 KB (92670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433b72fc9a86cea0757772f2d9f51b45c5e058a59ed62620c0f860be876f3a12`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
