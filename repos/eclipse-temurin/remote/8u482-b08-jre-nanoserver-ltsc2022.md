## `eclipse-temurin:8u482-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d52a1681e4034aa3fda8e4910e8f4eb5ff9fdea0563f37ecd30b9f2084a88469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:8u482-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:806e867eb498599efa28d1b6cdbc46cff6bcd151c3c0c656ef16712b806aa493
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166798529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d878b40baf5b67f0f9d0fde7b5cee9b8a3f7171c2c331e75b6682f611fdb79`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:19 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:30:19 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:30:20 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Feb 2026 23:30:20 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:30:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:30:23 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:30:28 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 10 Feb 2026 23:30:31 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197769c1803e408434ab708492fd6b579050a976074dbaed3739b29b6199a8ee`  
		Last Modified: Tue, 10 Feb 2026 23:30:37 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eceed90cbd5d1955c6216568900e73817ded358b9473f633f236a4991022da8`  
		Last Modified: Tue, 10 Feb 2026 23:30:37 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d08ae2ad7dbac17533b53ba8d5686a869850f2ea8498812a58c0c61c9120653`  
		Last Modified: Tue, 10 Feb 2026 23:30:37 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cab8b71b0d65da3ea85d644c9aacac85b339e0941a783b90f4089a5827b623`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac05d1dc1e36ef467ba07401c9f2701e89513ed43a7c5e665f6a41de49b009`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 77.5 KB (77492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354c3e453f871246c520377b6991faa27aab5e03280fddcbda1f2e688b747b47`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45e4d96db8cdfdb73d5cf2f22ecfa10528578e502414978388153e6cb4601d6`  
		Last Modified: Tue, 10 Feb 2026 23:30:40 GMT  
		Size: 40.0 MB (39969826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f0f9328d6792737799507cfe090170893f1b227342f311db22333f538a9888`  
		Last Modified: Tue, 10 Feb 2026 23:30:35 GMT  
		Size: 100.0 KB (100022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
