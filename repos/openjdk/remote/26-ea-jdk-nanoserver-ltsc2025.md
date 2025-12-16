## `openjdk:26-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:f8b8fda6a0bd33cf225c08712da904f61f6d05a87334c978feadbab6e7eae105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

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
