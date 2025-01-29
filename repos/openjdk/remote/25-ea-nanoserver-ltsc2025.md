## `openjdk:25-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:513d467f94b27faf8ce2fd63a6ed38853da23da230d078bcd3d02c5cec4d4fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:1b6e76e6e20aecf631e50f45b21926916ba09dd544b0e323a6b1e682d156c8c1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 MB (406633523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37181759e4d11bc176478fcb66d077ce26ffe4bd565d2e0bd299d5cffdf62c2f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 29 Jan 2025 00:31:25 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 00:31:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 29 Jan 2025 00:31:26 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 00:31:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 00:31:29 GMT
USER ContainerUser
# Wed, 29 Jan 2025 00:31:30 GMT
ENV JAVA_VERSION=25-ea+7
# Wed, 29 Jan 2025 00:31:38 GMT
COPY dir:8eaf4d943fad5808ffdf3732eba720fc3864b955a0e8f89e481534183a904eb4 in C:\openjdk-25 
# Wed, 29 Jan 2025 00:31:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 00:31:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3ff2b1af8808ff84d19e034d7db3b7ecfd654d4b319b30c22a7ec68d15be1`  
		Last Modified: Wed, 29 Jan 2025 00:31:49 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693ba15766975b8a6ce824da321e420249dc3df005a37d3f6acf1b0372daec9d`  
		Last Modified: Wed, 29 Jan 2025 00:31:49 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c75b6640ac8fd009cfbb6b6995b70f76f08baf0fa173d890b3c31d93af9ba17`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768ee2cb955d5e240fefd10bb1e6becfcc53afd1fad9b86e26195d523e85b7a2`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 76.2 KB (76176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a2e7893e0a27a8a3b22a056a0d8ee9248dafcbc85687386a3c5facb02f4f1`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a1cc66e1347f235cfede57eb741fecad2370e5f12974e91f72b4bc39b74bb`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a77cad5bccc562b4c9b14583f51d76bf15462b6e52bcd17838f6e29f33120c0`  
		Last Modified: Wed, 29 Jan 2025 00:31:59 GMT  
		Size: 207.4 MB (207392624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcfee32c3f0a5507357797e3d514ea208fc802a2eed9654e8d21317deada3e3`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 104.2 KB (104154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49d743e5ff9ea2649aa4952fea0316fb333b139cf0abf8d6f38dfe6a330e332`  
		Last Modified: Wed, 29 Jan 2025 00:31:48 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
