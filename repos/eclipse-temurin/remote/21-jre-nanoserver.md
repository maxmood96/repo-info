## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:228ccc9db860aed4a3fcf0eec83ad88f3616a7f9fd23bf42dfa82e360d49d879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2582; amd64

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

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:5fdc351a657730fc48b15ff089df4f79ae2f416282bf222fbc71329435c744f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207278101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae5b3c1b02e20a99e6357d68ee2d59e4ef8cc4fda91463e4bc9345fd895caa8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:04:08 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Wed, 10 Jul 2024 17:04:09 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jul 2024 17:04:09 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:04:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:04:19 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:08:27 GMT
COPY dir:30866ffc44919960ba2d43fceab02c0cbcad12e73e3b28316799617dca9a13d0 in C:\openjdk-21 
# Wed, 10 Jul 2024 17:08:36 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aabadac1b5e8483dd0ae114f714f10423b6947f765a9dde2c2c6d731513597`  
		Last Modified: Wed, 10 Jul 2024 17:35:07 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fcbbd57410aa25734b68c59c6ae804fd136d1f505eb7e01e5324081af58f06`  
		Last Modified: Wed, 10 Jul 2024 17:35:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9078f7dbe89c925f6ae3f302e728969d791fccb21aa0e35eb541a30a028f1e61`  
		Last Modified: Wed, 10 Jul 2024 17:35:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4887d113cf376f063e8fba98477195e8a9d5b2768bbc11bc929ff28828558993`  
		Last Modified: Wed, 10 Jul 2024 17:35:05 GMT  
		Size: 66.9 KB (66918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea31cc61a3c1ac32f5bcede5a330efc719315ae087ed5c5202ce3ee843b7d2`  
		Last Modified: Wed, 10 Jul 2024 17:35:05 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f19394ebdc28b233bb4fffd2856e2eea562ca9ba28019d8f7a2ace08643105`  
		Last Modified: Wed, 10 Jul 2024 17:36:15 GMT  
		Size: 48.8 MB (48758680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab8dc373e4494ff305d5e0987263d49476e033d99b40f48b704022fa31eda17`  
		Last Modified: Wed, 10 Jul 2024 17:36:08 GMT  
		Size: 3.4 MB (3365385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
