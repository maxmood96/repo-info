## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:8d51400f31f0e25995a3916b73a07b30dd052a0e0ddf8287f0eb98cc712f60e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:a929f4f8a23182e2081394a925c774d62a11515c96fbe11fb72157aed81223b1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.1 MB (423144467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadfa39fe8b013cee9d5a1b7c21e6dd4ff630f91637e5c121cda9a1e1a434cf2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Tue, 02 Dec 2025 02:17:11 GMT
SHELL [cmd /s /c]
# Tue, 02 Dec 2025 02:17:12 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Dec 2025 02:17:13 GMT
USER ContainerAdministrator
# Tue, 02 Dec 2025 02:17:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Dec 2025 02:17:26 GMT
USER ContainerUser
# Tue, 02 Dec 2025 02:17:26 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 02:18:22 GMT
COPY dir:af429b7e2d5dac7004e75510486adbb236437e3b8445f2d868ed1c16921e40c5 in C:\openjdk-26 
# Tue, 02 Dec 2025 02:18:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Dec 2025 02:18:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c42dc6bd6cf6d0b1831d7e233e0904ce0b44c83daf5c0473d1984555ff6dd`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b931a9027207ef8b6801f89ce5ad118219f392a3172509e1df6acfa99bc9c`  
		Last Modified: Tue, 02 Dec 2025 02:19:06 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e35998e1fb76d1b7dd15f7ecfe3ef0f9f73b666cc1a71e3a505193398ab4cc`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09e8c584df6d13ca99c351d02f49a54f30920528d33ba4ce77b22a8a0f4f78a`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 71.0 KB (70994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b21ac62e07012a0de91208a7c49a97acb6e4fd8f47a9addb4f2c5d04c202a56`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7089158482ad16419fff0bd48fc094ac16acaca438540eb66a70e9a180b51f`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f9925afa1bdb4d51a23ce463066c191a7be56fb945e96e979c0b48ea759288`  
		Last Modified: Tue, 02 Dec 2025 04:24:23 GMT  
		Size: 225.0 MB (225028174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e39f841cab6613c4811924ea703e101e857e7583bdb38805ce22eaba5b98ee6`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 102.5 KB (102451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3917e41fdd7b0473075bf7f4575dbef2d0c46ec754dd1c90f3f16aadf0d4e5b4`  
		Last Modified: Tue, 02 Dec 2025 02:19:02 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
