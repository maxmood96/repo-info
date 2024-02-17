## `openjdk:23-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:389f06736f6fb44fe28c363e084ab1462db7b9e34ab2700a5e44a22e2d160b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `openjdk:23-ea-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull openjdk@sha256:a9bde3f03d7832531f224ba03223a4a74cab2d11acca3ff62fed4fff5c6bd838
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306158364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e1830c4256212dc3e6836772f69cfce08b8903fd0901b9e22648ced78afba5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Sat, 17 Feb 2024 02:07:00 GMT
SHELL [cmd /s /c]
# Sat, 17 Feb 2024 02:07:02 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 17 Feb 2024 02:07:02 GMT
USER ContainerAdministrator
# Sat, 17 Feb 2024 02:07:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 17 Feb 2024 02:07:06 GMT
USER ContainerUser
# Sat, 17 Feb 2024 02:07:07 GMT
ENV JAVA_VERSION=23-ea+10
# Sat, 17 Feb 2024 02:07:16 GMT
COPY dir:0fe3fe081c7f2de728697b0fc6c894047c9c46b890051330802234037fb3f838 in C:\openjdk-23 
# Sat, 17 Feb 2024 02:07:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 17 Feb 2024 02:07:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8c8859ee6d409d9b4cf951ebd8655766454a4b681980b78973578f4c116ed7`  
		Last Modified: Sat, 17 Feb 2024 02:07:28 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd90887eb5ba0b2828615bbe747eb00434ffbb1f4fcd4ff0185c524c8c348d91`  
		Last Modified: Sat, 17 Feb 2024 02:07:27 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d3a0861a4cfd7bb4cc1b05c3b8299df9209069619adfaf5cf0e3079bf20836`  
		Last Modified: Sat, 17 Feb 2024 02:07:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1941e85c9e7a0dd97568482021e141699147550cfdbbe8f0ebc7ec2c0aec397`  
		Last Modified: Sat, 17 Feb 2024 02:07:28 GMT  
		Size: 83.9 KB (83882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8762d9d40bb4d10277c94df9ec0bb16d9dee521de966cbeca54e89ca41497a8c`  
		Last Modified: Sat, 17 Feb 2024 02:07:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d24f488b34f2ef105e2ff5197cf7863a4860a4008062014f53d0150f602e1`  
		Last Modified: Sat, 17 Feb 2024 02:07:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddb73e17ef42b6e37aa948f63e8c0b614c99c07344d9d66393a063000eb56d0`  
		Last Modified: Sat, 17 Feb 2024 02:07:39 GMT  
		Size: 197.5 MB (197539598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a035322ac6ed3bb012b6c945b0b02d3cbadd8289fbf003567c08d613a293cd07`  
		Last Modified: Sat, 17 Feb 2024 02:07:27 GMT  
		Size: 3.9 MB (3906812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaa59d0459cc412dc0ed47f06b28ff3d7af7edcff332cbf0b12ced40c2f0bd0`  
		Last Modified: Sat, 17 Feb 2024 02:07:26 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
