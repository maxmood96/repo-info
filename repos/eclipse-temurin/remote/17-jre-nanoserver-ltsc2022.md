## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0f11fefa6dd9516f5e9da6c56fa48d45b833fae4f57f4e97999643558a11f8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:618529ec77a88e4bd9239164282d4afa05db0ce63d49045e6d302c9ffcb5ced9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164104313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb932f0f310327e22a66fcf6c6c85c71ebd0a723f8bbc019233ef79d089b903`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:50:29 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 00:53:04 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Sat, 22 Jun 2024 00:53:05 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 22 Jun 2024 00:53:06 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:53:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 22 Jun 2024 00:53:16 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:54:06 GMT
COPY dir:a78f43753c24e3e0717a998b116850ca8c6149210b4cd2529d3fd312f361a7bd in C:\openjdk-17 
# Sat, 22 Jun 2024 00:54:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c04e6fe7f33e5ed7b73641c362d031eb0404b55967c9af2b8fa6f2269d9f92`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9803dbc941f205828a0d8bc61e5dc9da41077da5e02114f4902bbbbc156ecc7b`  
		Last Modified: Sat, 22 Jun 2024 01:07:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5739c49a35688d6f38646859512fb3830f981dda2c790af7ccb4565dc33c39`  
		Last Modified: Sat, 22 Jun 2024 01:07:58 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406a1038bc5a44c9617393f7df8f7f50605ad1fbc13ec30241c95aeceb276188`  
		Last Modified: Sat, 22 Jun 2024 01:07:58 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3aa002337d4eaa521b373b4706827a1de9f68f132b657b37396fd96b13642`  
		Last Modified: Sat, 22 Jun 2024 01:07:56 GMT  
		Size: 85.7 KB (85652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299ddcec7bd2eda31e50cbf79a3641cee7d67a859279f54204fdf1d1a845becb`  
		Last Modified: Sat, 22 Jun 2024 01:07:56 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bd4a5491b31a365f73aec980adac6aa28945ccbefe4879be812d548ce66a8a`  
		Last Modified: Sat, 22 Jun 2024 01:08:32 GMT  
		Size: 43.5 MB (43454603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e7fa2bd6fc7f5bfaf7fe4833d3a1599d20a570cc16cb3b209bc9d716be84f4`  
		Last Modified: Sat, 22 Jun 2024 01:08:24 GMT  
		Size: 58.7 KB (58706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
