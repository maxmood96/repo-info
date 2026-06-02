## `openjdk:27-ea-nanoserver`

```console
$ docker pull openjdk@sha256:cd21fdbfccae9fc7a5ebc799d150e42cd0ba958aba3051367005cc06e8f55db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:a359f72b64999af9ba2173d7a02f11f09ce12a8e61c5cf514179f70832fee6e6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422948638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a16971301407e3b4fe90ec4c1b30989c74ec7933e64a11ff14762a0c79efdc0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Tue, 02 Jun 2026 08:16:55 GMT
SHELL [cmd /s /c]
# Tue, 02 Jun 2026 08:16:57 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 02 Jun 2026 08:16:58 GMT
USER ContainerAdministrator
# Tue, 02 Jun 2026 08:17:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Jun 2026 08:17:16 GMT
USER ContainerUser
# Tue, 02 Jun 2026 08:17:17 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 08:18:46 GMT
COPY dir:548e2ff91354155ccc5ff2b06e6682160bdc15feb1f883e9b2a88ea1d455bbac in C:\openjdk-27 
# Tue, 02 Jun 2026 08:18:57 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Jun 2026 08:18:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee5b1c855c4f36568af625337a9ca080886787f86b82f9bfa1eddf0cb1aa358`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e1d1014bb238a96e2f7d71ccfbccb47178c7a9726f573aea574c30e6cb670`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d56f2446008ed6afe3eb7d13b862ae3f2b77ad8234972b9e4b9a79f8182955f`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934bde933921b90adc5b74264bb92c1e885bc523ea938ce6eac27b25c578f886`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 73.0 KB (73047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c25ce84d5e073c7849c0229d16beb69204ca62117dbc8fcfcea2f2f00b257e`  
		Last Modified: Tue, 02 Jun 2026 08:19:02 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0ef84e66da0a21e3537162108376dcbfb385dd736df98c085438cf63162332`  
		Last Modified: Tue, 02 Jun 2026 08:19:02 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd316955136e0d9d781fc3234e536b0d18cca50da00a1e03cb3d7afb56ecfcb`  
		Last Modified: Tue, 02 Jun 2026 08:19:18 GMT  
		Size: 223.0 MB (223026502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ca450ba1f341142cb1e03b4f2da8e65c00767822aad6c6407f994e23b95602`  
		Last Modified: Tue, 02 Jun 2026 08:19:02 GMT  
		Size: 103.9 KB (103877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5544ae9fa9d0b8c912d006f37026111bc92d1456238cce7e2b2c6c78d1d1e81`  
		Last Modified: Tue, 02 Jun 2026 08:19:02 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:18af2af9411b81670990374130875256f10177990422f2952df3076f653c40a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350271176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c71d4b56c720deb8a09c9cf50bb522291be0b11f29dd73504feb9648d81c1b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 02 Jun 2026 08:17:34 GMT
SHELL [cmd /s /c]
# Tue, 02 Jun 2026 08:17:37 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 02 Jun 2026 08:17:39 GMT
USER ContainerAdministrator
# Tue, 02 Jun 2026 08:17:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 02 Jun 2026 08:17:59 GMT
USER ContainerUser
# Tue, 02 Jun 2026 08:18:00 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 08:19:55 GMT
COPY dir:548e2ff91354155ccc5ff2b06e6682160bdc15feb1f883e9b2a88ea1d455bbac in C:\openjdk-27 
# Tue, 02 Jun 2026 08:20:07 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 02 Jun 2026 08:20:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782992fa9978ec2f51b99320653fff9dab2b7c77299a32693d0c0b082a303c4c`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5797422af52a581cc9c9eeb1fc057e31485285be218dba1eeb319fdf43e817`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4774acd8c5222949bd1648c6ce35974a18d0c840080c74a0be75b851584cb866`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e894b1743bfa76f05cf5236f1949479958a269216b2d4faa9fd869dd9a0adb1`  
		Last Modified: Tue, 02 Jun 2026 08:20:14 GMT  
		Size: 72.8 KB (72803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae81b1c58cc2fc6f3076d7231d84664f4167bf5a9625bc9f23e2b7db5352ac71`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb03b05c5824ffe7aeabaf0aea93d59a2c039e0f81597df91a25d8557d85b25c`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689c6f5af23a22ebb4b1afafa759e8d3cec999319dbbd61d5a2be1b33a219129`  
		Last Modified: Tue, 02 Jun 2026 08:20:27 GMT  
		Size: 223.0 MB (223026333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9732d5c32e22b322d853145a82b3f0244bb540b68edcd1cb418c6261a018600`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 126.9 KB (126910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0355085c9c658bf1974a0fd8bb02aad365c97707568da9f52efcd1bfac7913`  
		Last Modified: Tue, 02 Jun 2026 08:20:12 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
