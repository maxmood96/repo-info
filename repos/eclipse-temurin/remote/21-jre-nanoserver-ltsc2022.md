## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4914eb7b7141fb56ebba728a5ec75961c0fd114d67f99d3131c2a5b03c426971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:6fb8429357ba170e1494738943398f050695536069cae54992f9a98d7d9619e0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169394086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455b9ae0c04ee6eca311acf4fb0f85597d171f48589acfb8d019196056a0bf13`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:20:41 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 10 Jul 2024 17:20:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jul 2024 17:20:42 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:20:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:20:51 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:21:32 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 10 Jul 2024 17:21:42 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ad1a124fbd90523f5c17a2b76fa73394d844f86941264af090f155024cd16f`  
		Last Modified: Wed, 10 Jul 2024 17:40:52 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2d8886c6766a53c0b8e4d19f8642de7bca3a9bd424376eb402f4a33468096a`  
		Last Modified: Wed, 10 Jul 2024 17:40:52 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cec8f8ac15d117d4376079b1dc4f9f2f0373062b79b7a28deaac6ddc84b962`  
		Last Modified: Wed, 10 Jul 2024 17:40:52 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0d89c8324c507c3efbe6f90dcd2f22c20e5b212f48aa548db6be2a451bc5c1`  
		Last Modified: Wed, 10 Jul 2024 17:40:50 GMT  
		Size: 77.9 KB (77897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d78b0917266f1cb72cd484428a1816a6124940f8113629dd4f56cece113b2`  
		Last Modified: Wed, 10 Jul 2024 17:40:50 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de45bf49eff74fe6a48022e4478a0d1a88b3e7029201ba5b287b4898865c6deb`  
		Last Modified: Wed, 10 Jul 2024 17:41:23 GMT  
		Size: 48.8 MB (48758852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110fbb7ef1ca5fdbdde5a5faa766f33ef51dc04bc2ba124dbd261c5bac3057f`  
		Last Modified: Wed, 10 Jul 2024 17:41:16 GMT  
		Size: 61.2 KB (61162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
