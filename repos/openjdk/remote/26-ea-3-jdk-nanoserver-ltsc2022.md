## `openjdk:26-ea-3-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:bfcf749b6164678f15a54e93cd8d4a7c4aa6309749a5f4cf2df0c84dac3f733b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:26-ea-3-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:bf5bf79ed5d7203430400d1abacea82e74d06c573bd3ff0629da875da8513c81
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341142523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4752cd10c1c76d4dc71aedf75f2d38a8eec1c63ebff1dd098430925384ab0036`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Sat, 21 Jun 2025 01:08:09 GMT
SHELL [cmd /s /c]
# Sat, 21 Jun 2025 01:08:10 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 21 Jun 2025 01:08:11 GMT
USER ContainerAdministrator
# Sat, 21 Jun 2025 01:08:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 21 Jun 2025 01:08:20 GMT
USER ContainerUser
# Sat, 21 Jun 2025 01:08:20 GMT
ENV JAVA_VERSION=26-ea+3
# Sat, 21 Jun 2025 01:08:29 GMT
COPY dir:b52ef9dbe4c9943445d4965998b2dc917b23121cc15ee03d8e7d3bffb0fe3291 in C:\openjdk-26 
# Sat, 21 Jun 2025 01:08:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 21 Jun 2025 01:08:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beeb1c99ff6235300473a98ed7ee280b76e2d1250c15f8d6075c6ca87471adde`  
		Last Modified: Sat, 21 Jun 2025 01:15:35 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2651848c779db5c5622dfd103b39df87e5e29c53d957a4ae653efc982bc4dc8`  
		Last Modified: Sat, 21 Jun 2025 01:15:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2d515e30d9a97a809f527e5349952c5618be40497ab838a1b631d6238e3565`  
		Last Modified: Sat, 21 Jun 2025 01:15:42 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5da6d2f5c6f61dff8eb846dedb2d0dc3a1e665ba1a27e8a841967238521a58e`  
		Last Modified: Sat, 21 Jun 2025 01:15:44 GMT  
		Size: 73.4 KB (73436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dfe7e8f0064ad2ff811a761edddfbb271dfdab3a88a57ce3ce544a5bfef80b`  
		Last Modified: Sat, 21 Jun 2025 01:15:48 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244d445adf0a9da2c9c00254c2dd090e097f8351bd93b8fde76ba1c35586e8bb`  
		Last Modified: Sat, 21 Jun 2025 01:15:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da902566499d1780b495502bd9d9f89841514f978ea593aa13f618c104702aec`  
		Last Modified: Sat, 21 Jun 2025 03:26:08 GMT  
		Size: 218.4 MB (218424355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178a28652e4d5f248ca6b85d16dd8c7d89a8972b58a0d9a9941659eb4b67d9c7`  
		Last Modified: Sat, 21 Jun 2025 01:15:56 GMT  
		Size: 98.0 KB (97989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8910c94977d5d34b1f190e2a3947e51832fffc8ee9df3cb650c023e1f073f8f6`  
		Last Modified: Sat, 21 Jun 2025 01:15:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
