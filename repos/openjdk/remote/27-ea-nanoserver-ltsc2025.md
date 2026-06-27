## `openjdk:27-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:dc6432294802874d366604cf52d232a0fbc84fdd762a1346cef09d1e087cf086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:27-ea-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:9c77af29b5a0eba62288290bb7b2f2991f89cbf1bc1b0f2b33e198ff1a77d8b7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419961908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bc4a2b847c40840f97bd6aa6407bc0960aa75eb3adc5780fc49ab28e05aaa8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Fri, 26 Jun 2026 23:08:45 GMT
SHELL [cmd /s /c]
# Fri, 26 Jun 2026 23:08:45 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 26 Jun 2026 23:08:45 GMT
USER ContainerAdministrator
# Fri, 26 Jun 2026 23:08:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 26 Jun 2026 23:08:53 GMT
USER ContainerUser
# Fri, 26 Jun 2026 23:08:54 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 23:09:29 GMT
COPY dir:4ebef711240c45398e9b005c4af57e81a1e010a3220f8b29271464be340ccef0 in C:\openjdk-27 
# Fri, 26 Jun 2026 23:09:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 26 Jun 2026 23:09:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0de21116dc5fae444b7ce88a94e197a87e76830288082bc49d43d12f1662dd0`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb9ee015353694d4a67f86f9bb2da154bd5fa1fd98854a53d296eee1b70301f`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82bf5294ab7086a03ae3a627b7dac9767f6a6496a877061fd481da5c7b73d23`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c967391d3174ef7bb942206f3afe54e386b9be64711fc92c31942a5a2ecdac65`  
		Last Modified: Fri, 26 Jun 2026 23:09:41 GMT  
		Size: 70.2 KB (70175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f85acd70a14bbef54219e2ef8cbcf54f3cf8e68800c5aa1f9ddb33e6c48130`  
		Last Modified: Fri, 26 Jun 2026 23:09:39 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ad0153cc5cfdda24d1956d5062370d3e73c2ae1d950e10cea40c2889e4ef84`  
		Last Modified: Fri, 26 Jun 2026 23:09:39 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202ec147cf0c3225d01bd41d7009ee79f0f34c78ea5909a9d2cce2bde2651ff`  
		Last Modified: Fri, 26 Jun 2026 23:09:54 GMT  
		Size: 223.1 MB (223124767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700eb385341d38b8223ebcf5152dcf93ec0650d52eb214fa4498f82c5ec05bd`  
		Last Modified: Fri, 26 Jun 2026 23:09:39 GMT  
		Size: 92.6 KB (92613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a990081cf445ffb53e7aeab3fe39ebaebdd01eba877c059205367b25271cb9`  
		Last Modified: Fri, 26 Jun 2026 23:09:39 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
