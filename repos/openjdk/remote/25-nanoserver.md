## `openjdk:25-nanoserver`

```console
$ docker pull openjdk@sha256:6a78f86250fce9d01f38f70dacbcf75baeb6e4c4a9106990aef9440612efbe1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:25-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:372a0c0fc159dfde62651c316654e13fbe91b00f3102b735e527f27728e3c55d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6888b9898d0f7ba5b3633ed808465199c0c06d358038ee0277e30fbe0c9b68f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Tue, 10 Dec 2024 00:08:51 GMT
SHELL [cmd /s /c]
# Tue, 10 Dec 2024 00:08:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Dec 2024 00:08:52 GMT
USER ContainerAdministrator
# Tue, 10 Dec 2024 00:08:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Dec 2024 00:08:57 GMT
USER ContainerUser
# Tue, 10 Dec 2024 00:08:58 GMT
ENV JAVA_VERSION=25-ea+1
# Tue, 10 Dec 2024 00:09:07 GMT
COPY dir:2e6cdc7f1b1fe8d940d6b4a43862b3e1f54bcd94c04e6589c6d482f98b5321b1 in C:\openjdk-25 
# Tue, 10 Dec 2024 00:09:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Dec 2024 00:09:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9022a9b898ca0eeb100c9155581c76f02d8500930eb13b1583a51bca0d2a251`  
		Last Modified: Tue, 10 Dec 2024 00:09:20 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90b8048e81a6a338ad0e4545fcb987d81c0ebdadd6bf85779d28782882b9b7f`  
		Last Modified: Tue, 10 Dec 2024 00:09:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b349a7fb38398799b44eea8de246f707e607f6176dec3e5fd94453d97dadddc`  
		Last Modified: Tue, 10 Dec 2024 00:09:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b049dc2d2aaf2a2bdf7ff166c4eef1b229708ede881aec88e7a945f5f997ef`  
		Last Modified: Tue, 10 Dec 2024 00:09:19 GMT  
		Size: 67.6 KB (67600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e386307956326318972ef9836e84e6e62fcbcd15439d94ac8c6708245c1e8629`  
		Last Modified: Tue, 10 Dec 2024 00:09:17 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03826940da989ddde9f06a095801be0c87285d576061b565336b5ea5938d05c`  
		Last Modified: Tue, 10 Dec 2024 00:09:17 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dc622eaa018331eac3bf65f47de45cd65c1f56c705e1c5288cdcfe07dc5aa4`  
		Last Modified: Tue, 10 Dec 2024 00:09:28 GMT  
		Size: 208.5 MB (208548247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e73945782773c941084dbc2e0d36160046eb58feb8c09cdb5ae2ecafe5688f`  
		Last Modified: Tue, 10 Dec 2024 00:09:18 GMT  
		Size: 4.4 MB (4406736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14bac47341fcbf2c82adfc84ec2b6da6ad16d675c64b1810027b915f54adf3a`  
		Last Modified: Tue, 10 Dec 2024 00:09:17 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
