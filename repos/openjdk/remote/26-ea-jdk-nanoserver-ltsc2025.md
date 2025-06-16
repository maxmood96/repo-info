## `openjdk:26-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:12f1573dcd592ec2c71c8a37242fd904e36641cf3413424f084fce8f64f30561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:26-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:636cc551e4fcca1a1862c92c917c1a4e86337a77467e1f72c6d11bee6be076e3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.6 MB (410626816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff40dc2d9b0b3c5ee4cf8a0208c5d2d83e3e518a73c746a3770ea9a481cbff22`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 16 Jun 2025 18:16:57 GMT
SHELL [cmd /s /c]
# Mon, 16 Jun 2025 18:16:57 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 16 Jun 2025 18:16:58 GMT
USER ContainerAdministrator
# Mon, 16 Jun 2025 18:17:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 16 Jun 2025 18:17:01 GMT
USER ContainerUser
# Mon, 16 Jun 2025 18:17:01 GMT
ENV JAVA_VERSION=26-ea+2
# Mon, 16 Jun 2025 18:17:09 GMT
COPY dir:fc8b81948364d0e39d95d5a838d5c247253584bf16df7749b143abef5cfa930b in C:\openjdk-26 
# Mon, 16 Jun 2025 18:17:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 16 Jun 2025 18:17:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5639861f7963e462275b0fa72a9a0b0ef4710117fd4767d1c28b620f1a2da8cb`  
		Last Modified: Mon, 16 Jun 2025 20:18:06 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575b74e30b66c8fa651cea9612e171d5ee78a1c8b41894805d9cfceb7444d0c0`  
		Last Modified: Mon, 16 Jun 2025 20:18:11 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993420a2f72dec437e94ee7682cfc63fddee3738fb8f704727387013a3205792`  
		Last Modified: Mon, 16 Jun 2025 20:18:16 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb92150c032a74a5bafa7d0eadec4df9f5823e4629099467b064da3bae1934a`  
		Last Modified: Mon, 16 Jun 2025 20:18:20 GMT  
		Size: 76.4 KB (76374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7983657840eb2faaec156b815a9215b354977d51ffb379139f2f0df0b383b57`  
		Last Modified: Mon, 16 Jun 2025 20:18:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238964e3774b05f618c8b3c1d9b60a2ed2a3b14e289c888b98a4e156d8b82838`  
		Last Modified: Mon, 16 Jun 2025 20:18:28 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf3a07ef6a2eff671a6dbda956a5c32ba5296087617fdcb9f8d9658eb3cf2f6`  
		Last Modified: Mon, 16 Jun 2025 21:25:37 GMT  
		Size: 218.3 MB (218347387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c572a9d919d2bba5caaf5655cf588715604fbcad9d29ad7352548713254c07`  
		Last Modified: Mon, 16 Jun 2025 20:18:31 GMT  
		Size: 114.1 KB (114120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c57c3fb7f14b339b37aa01109112b3c9521613d54359d22d4d2e10e01821443`  
		Last Modified: Mon, 16 Jun 2025 20:18:36 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
