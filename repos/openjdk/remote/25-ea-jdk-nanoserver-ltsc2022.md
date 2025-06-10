## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:aa95ee01fd7bf4354c41a9cf0112e248489c8bc79b799d3e369f7a6dc8e75591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:fac3902ddac46e6a492e921f5ec3cc5d57cfb88ef8dfa933f4854e8a62250dcd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341237228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff05ffbbe1876411bf1f8d885bc88ec386cf94fb880b91d08840f7fe5c4ac941`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Mon, 09 Jun 2025 23:07:15 GMT
SHELL [cmd /s /c]
# Mon, 09 Jun 2025 23:07:16 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Jun 2025 23:07:17 GMT
USER ContainerAdministrator
# Mon, 09 Jun 2025 23:07:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 09 Jun 2025 23:07:34 GMT
USER ContainerUser
# Mon, 09 Jun 2025 23:07:34 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 23:07:43 GMT
COPY dir:2a5431c9629d8e59dc59f707822e3e4d9048b856e0212fd4224a68120121ffaf in C:\openjdk-25 
# Mon, 09 Jun 2025 23:07:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 09 Jun 2025 23:07:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856cd523692bd4e19216fd00010dc6e6428e9fa8949e9d482b82a8040681100a`  
		Last Modified: Mon, 09 Jun 2025 23:17:40 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75f914a7097615c47e01a8919d44feb0cc46dba7dcafb435ce3d9edab402951`  
		Last Modified: Mon, 09 Jun 2025 23:17:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747ab2d6f834e44d53aab5d87a3ac87277fe091f06d6c51d0438aedd50c88425`  
		Last Modified: Mon, 09 Jun 2025 23:17:46 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab623a0a6f0ff1bba6a66a5a8e28efa63ca4adeb1263ae824cbc083e84c21d99`  
		Last Modified: Mon, 09 Jun 2025 23:17:49 GMT  
		Size: 100.9 KB (100920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca187ed3e6c99c3d13091955170ec946df811a763a19aef24b0aa4ad544422e3`  
		Last Modified: Mon, 09 Jun 2025 23:17:51 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ebaf055cf8f2fb1ded7136004fd4be6e1b839d230c04d508797c6d846e1a26`  
		Last Modified: Mon, 09 Jun 2025 23:17:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be49af4c29d09e440192107e5fed4b531858edeaeb43c30dc171a6bde6561ed9`  
		Last Modified: Tue, 10 Jun 2025 00:24:18 GMT  
		Size: 218.4 MB (218444348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c0fab37bbcfb4d7ff340e06224f51673ce2c6478b50cbd2dc25bb5f8d23e57`  
		Last Modified: Mon, 09 Jun 2025 23:18:01 GMT  
		Size: 109.1 KB (109147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf662afdce5d095c8635a49f8a4e7655f732451a6631353a57194adf32466fc`  
		Last Modified: Mon, 09 Jun 2025 23:18:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
