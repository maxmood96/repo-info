## `openjdk:27-ea-27-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:279eebeae3c0eb716dc662690a88e5b115d502f4f9fc110974c939e10c068135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:27-ea-27-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:ebc862884e60be4d08932b721d2128819d5538654bc1e474fc71d5b3d973eff1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.0 MB (419958762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b42ec991769b24b31a5d97cf3b2b5ccbca5d997cbd57c470a9039c5336a18`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Mon, 22 Jun 2026 23:09:33 GMT
SHELL [cmd /s /c]
# Mon, 22 Jun 2026 23:09:34 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 22 Jun 2026 23:09:35 GMT
USER ContainerAdministrator
# Mon, 22 Jun 2026 23:09:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 22 Jun 2026 23:09:46 GMT
USER ContainerUser
# Mon, 22 Jun 2026 23:09:46 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 23:10:14 GMT
COPY dir:0d582b259e10424ad2a400d25138b5e85d8dcedb2869ba13c9537e008882334c in C:\openjdk-27 
# Mon, 22 Jun 2026 23:10:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 22 Jun 2026 23:10:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d76103312cc1f90a0d3bae58547d58c8326ff07fcb9676e8f34d6dc455fe7f`  
		Last Modified: Mon, 22 Jun 2026 23:10:28 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945102c5d4434d4a9170536b7ff278b464e3a1e0b335560e00d417340744d364`  
		Last Modified: Mon, 22 Jun 2026 23:10:28 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42667b73b984e0403ff4d5a23af5a061434e821b5253152813119f32456ecbab`  
		Last Modified: Mon, 22 Jun 2026 23:10:28 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08952103b8823b641eda58b567b2a81cd1331f4342195b5fbc84ad5e5489a2bf`  
		Last Modified: Mon, 22 Jun 2026 23:10:28 GMT  
		Size: 70.4 KB (70371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44e73a4f1b5d748749e35a1dcfea82a4cfaa638fdc55dcbec10ee1f1ac0f9fb`  
		Last Modified: Mon, 22 Jun 2026 23:10:26 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972388a9e6492113fcaca0bba361c643cb83395f1c8069d1010e78c573575948`  
		Last Modified: Mon, 22 Jun 2026 23:10:26 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3731deda643e39a313a73b659b4542809cbd238096bdc71007c04679e71570c0`  
		Last Modified: Mon, 22 Jun 2026 23:10:42 GMT  
		Size: 223.1 MB (223101520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb431e0fce6703b1681857211a472b75ec00fa7212c508b3e3371a924963cc6`  
		Last Modified: Mon, 22 Jun 2026 23:10:26 GMT  
		Size: 112.5 KB (112528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7df25ad100d301e9b9da20e3d7323a09cadced7ca890132919ff2be45f6eaaf`  
		Last Modified: Mon, 22 Jun 2026 23:10:26 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
