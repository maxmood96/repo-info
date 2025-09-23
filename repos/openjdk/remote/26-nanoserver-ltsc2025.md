## `openjdk:26-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:8c8a59bf5ccf59627c2b2673d871feffb9a62bc9f7e3a79e4e73a500bfb323c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:52b28db21b1a123c0aad05f0fce01fb04b6b865c640a8ba6efeda42bfd7532be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.7 MB (412659295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508c9b32a8fbe6d315470f56d7f452e72180a0ec2a61dc9e4f414716c2321c54`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Mon, 22 Sep 2025 23:12:24 GMT
SHELL [cmd /s /c]
# Mon, 22 Sep 2025 23:12:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 22 Sep 2025 23:12:25 GMT
USER ContainerAdministrator
# Mon, 22 Sep 2025 23:12:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Sep 2025 23:12:37 GMT
USER ContainerUser
# Mon, 22 Sep 2025 23:12:37 GMT
ENV JAVA_VERSION=26-ea+16
# Mon, 22 Sep 2025 23:13:28 GMT
COPY dir:426c5eff4433821d86546e9933d9e51369c584ab771442942f2429c3418779a2 in C:\openjdk-26 
# Mon, 22 Sep 2025 23:13:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Sep 2025 23:13:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb60081c8a16a463b4f927307d9eea3ac9ded224397c5e9b065b7d761874a5a7`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08345df6c61e003c4163af6b5e08e8860516dba5e122db75ca84bfcdacd910`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d2633903dfd6ffefd3bbe7cc24e4d8567f395ea24eb5172ee7ef5c65b885e3`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601ef83935eca40d9e51c977f7d1a8b808f61d5b2256c23b0c4cd8bb9919829c`  
		Last Modified: Mon, 22 Sep 2025 23:14:06 GMT  
		Size: 82.7 KB (82728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf0cc6109acb93cc2a135b3e256cbdbc91ddcb646ff5ce43cbb79b09b3e625c`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f4531126c8769f223a772d9c63cd0790cbd52e3110cf53772a235f1aa29325`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c0a7f7f4ebac06144a8715914512774b17220594e0982b85620d9bbf192309`  
		Last Modified: Tue, 23 Sep 2025 00:24:12 GMT  
		Size: 218.9 MB (218905427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f25ba03b12fd9051e5b864a43f0868c7ea8938fe9c7cb303c418976757ebbc4`  
		Last Modified: Mon, 22 Sep 2025 23:14:06 GMT  
		Size: 113.9 KB (113925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18085c8998b0a893ec43b3c9a99abe0442ea780b4416cd5841b4fb56e080361c`  
		Last Modified: Mon, 22 Sep 2025 23:14:05 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
