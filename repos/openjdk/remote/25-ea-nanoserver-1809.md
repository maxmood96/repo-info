## `openjdk:25-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:3e065cb19317007944dfaf372596feecb5d62f8ed5c4b637ca211d0cac4379fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-ea-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:29b24bcaeb181abcae645729afd80c23e1f646af8523e4978f20066b5375d733
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320869409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55beb3840133bd7c57d213d6740ef5d43f5fb93cc73f2aa9bf7fbceb1c750b3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 19:17:51 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 19:17:54 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 19:17:54 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 19:17:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 19:17:57 GMT
USER ContainerUser
# Fri, 18 Apr 2025 19:17:58 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 19:18:06 GMT
COPY dir:595a9046aeb360afc9a03339cfcb9f80b8fb3559c4a1bfb194a0956d7f6a1899 in C:\openjdk-25 
# Fri, 18 Apr 2025 19:18:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 19:18:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2194e047ba19706a2edb4aa09f4bceefb6eb182e136c01eacb0218fc9b3e8431`  
		Last Modified: Fri, 18 Apr 2025 19:18:16 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea9286d32283cfdf9986cd94760448a280dfa03b66fbd6acabeacbb6803ad8f`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238449a32813860e4417cded4e60b4e63a3888ace81bb64615180cfea0dbc876`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71cb2a88ab624ca06f7ab21037d3c4efb0576580bd35cb5f02938163a005cfd7`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 71.9 KB (71882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18be9c78d2197e03323d34272b4f5fe19144fc81c91b95a376764c72f6fa6dc7`  
		Last Modified: Fri, 18 Apr 2025 19:18:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a7686a23a37c4a39d6a580dd70f2483e4f65571419599d78bf6b1f09e38998`  
		Last Modified: Fri, 18 Apr 2025 19:18:14 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6021216e0333fb93b9c52831b8adbcf088d49d66b1fd1d511683096144d6c8`  
		Last Modified: Fri, 18 Apr 2025 19:18:25 GMT  
		Size: 207.7 MB (207663978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df93ab5b0769004c97508527dddd89c7757d892e76c640c3430672cb614b52e0`  
		Last Modified: Fri, 18 Apr 2025 19:18:15 GMT  
		Size: 4.4 MB (4375065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36640fe87809fa6f14d331dd2af82143811576c6382dcc757fca09ab66429665`  
		Last Modified: Fri, 18 Apr 2025 19:18:14 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
