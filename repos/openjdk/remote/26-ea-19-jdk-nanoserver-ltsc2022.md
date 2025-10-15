## `openjdk:26-ea-19-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7a394380f937b2cea9863f2e775b5762f50449ed1649db5c68eb5877de90f55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `openjdk:26-ea-19-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull openjdk@sha256:98a78977cdba9f4e69bd9111461a75df432d9b31e8d783c6df01cb2a48b7cb92
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344088630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba43ed0ba4cbe89da8eebf4618baeb4df7e28590170a87f39c1d76c3f15afd1c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:37 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:14:27 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Oct 2025 21:14:27 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:14:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Oct 2025 21:14:30 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:14:30 GMT
ENV JAVA_VERSION=26-ea+19
# Tue, 14 Oct 2025 21:14:39 GMT
COPY dir:83313e74e1bdca6c4da8521f7958b3cb9f989c8b9d5087396f320ade6e966d10 in C:\openjdk-26 
# Tue, 14 Oct 2025 21:14:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Oct 2025 21:14:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cc1e407ae6e924b90e92be01a4a3da1bfc030b400da250e7591cd9ecad51cd`  
		Last Modified: Tue, 14 Oct 2025 21:13:12 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017b8633e516e9c65ea75bf25e05b4319e8ce2a1258f965fe9d1182fb4f2e171`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdee083643e2f969b0bc6d5021a520056fdeadd1ebee6c3bdd8aa878e9141f73`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165e387e403d0869d8286de362b1c71e656b8ca9714a0b6e4977bb3158862ee8`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 75.7 KB (75654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63cea1813ed21c57264d0dc3336b921e94d5ae287d91a34348c82ac4adc8ae0`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937a5d28d1dd7a04f4c63a0a4f061aecdd4e4507aece6c8e4e954a34b0d05a9f`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5a2fd1136f755b7555123b2b7de93d6c198aa17bc3ec8a1ae1d18c26bacd43`  
		Last Modified: Wed, 15 Oct 2025 00:24:19 GMT  
		Size: 221.2 MB (221200512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5f9c85cfd615516a00f922b9822b580f7fcc453901539333c57ad15adfb7db`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 117.2 KB (117208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886702eb9b0cf7a1e43ec35c83675b61c06f6c5f5adb45ad428f7b84a17ceb33`  
		Last Modified: Tue, 14 Oct 2025 21:15:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
