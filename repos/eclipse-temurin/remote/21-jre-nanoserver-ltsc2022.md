## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:654d1380fd29e6431e3919dbc8f6e571e0286c52d63e0fa631ea47b0deb55cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:174e70d6c0df4678bd86fef82c2535e30216cd3b231afbc147fc941a5007d668
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169328690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffb5166c9675526dbba35e1367b286af2a5ee6aba6df23f013e6020c1c84a47`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:09:06 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 11 Sep 2024 01:09:07 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 11 Sep 2024 01:09:08 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:09:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:09:18 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:09:57 GMT
COPY dir:6441dab14d212c21b2c8fcb6fc00e95950b0c66ee3c049dbfd71b18f09e541f6 in C:\openjdk-21 
# Wed, 11 Sep 2024 01:10:09 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d37494348c9f0c3dc4712fe54e54161f8e2b0bda7769a69c1c11e74cff80d9b`  
		Last Modified: Wed, 11 Sep 2024 01:35:18 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9e9f140007c0567936ebbeeef2fa1c892ca487870bc4cca712593eb076fb44`  
		Last Modified: Wed, 11 Sep 2024 01:35:18 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde01b60b204ad3e323821d5b0951406a12e2e9ad293887fce102341720ec43`  
		Last Modified: Wed, 11 Sep 2024 01:35:18 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41387b66ef5cd39a47b9083edb50b1324df3f1f69d1f1d594e9e6b8de2b0753d`  
		Last Modified: Wed, 11 Sep 2024 01:35:16 GMT  
		Size: 82.2 KB (82243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558ee7b13ccd2688c7f23ecc770e31683af1dcec2ad28ee81af7f40ecd9c943`  
		Last Modified: Wed, 11 Sep 2024 01:35:16 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b47d01a981175f14ca0d725eff5c28e89b144d9dec13596e60205814f6b03`  
		Last Modified: Wed, 11 Sep 2024 01:35:52 GMT  
		Size: 48.7 MB (48666783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7511b519e7cf0b86389bc74ca27bdd8b20abccf5a70e41203928c0abd321e5`  
		Last Modified: Wed, 11 Sep 2024 01:35:44 GMT  
		Size: 64.4 KB (64354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
