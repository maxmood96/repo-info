## `openjdk:26-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:0ba4d7d6c70799ebb817b35ab5a9ca6914b3484f2f46ae54066c5f3e407a8fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:15756a0890fd7705e8cbb2d09430ff0c4289bb74e5f1dc895ecfb870a7962527
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344136582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afd64ac65a3722e92a4884c6fe2d4e278d62a5ccd365be8a370f1a6d4798cdf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Mon, 13 Oct 2025 20:18:30 GMT
SHELL [cmd /s /c]
# Mon, 13 Oct 2025 20:18:31 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 13 Oct 2025 20:18:33 GMT
USER ContainerAdministrator
# Mon, 13 Oct 2025 20:18:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 13 Oct 2025 20:18:44 GMT
USER ContainerUser
# Mon, 13 Oct 2025 20:18:45 GMT
ENV JAVA_VERSION=26-ea+19
# Mon, 13 Oct 2025 20:19:56 GMT
COPY dir:83313e74e1bdca6c4da8521f7958b3cb9f989c8b9d5087396f320ade6e966d10 in C:\openjdk-26 
# Mon, 13 Oct 2025 20:20:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 13 Oct 2025 20:20:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa8975bee983a0965126ce10c9b6b93cfac4f64538e80402d7d0578f13b9ff7`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee5f8cbb91b4b576db531d90e42aabb2533282769791c93733bac5888d15e70`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca2c88e757d4b5d5220ef4b2ec8883a4216dbb1bc5ca3012de66f26092694d2`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04a9bb4b5d7f5410d52fd4856303e9bed0bdeb4c8491ce48189cfb3a7313fec`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 87.0 KB (87050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057eee2a5dc68c3fe690c80aea0f636ee52dc81cfba8dff633f740eb40c4d59c`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b065ace366f9757ee03b8dd8888e3bfa9de3bcd19964c17ec56cce7c2fb0e7eb`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28817b336b727504313e39d5fdb792b2d5f7a5b0c15c79c711552104581e749a`  
		Last Modified: Mon, 13 Oct 2025 21:24:16 GMT  
		Size: 221.2 MB (221201009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eef051caa93f4d0c2a50e9246252ef9db703ee9ebd165045b6081e02adbdcd`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 122.2 KB (122218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5a1e09d6c881df444e9004345bdfde1e7a3ca59302beaf7be6f5b70c0cf0f4`  
		Last Modified: Mon, 13 Oct 2025 20:20:34 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
