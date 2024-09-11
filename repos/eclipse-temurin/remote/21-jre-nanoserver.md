## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:72464e785d771e62bc2e6f8db7084ecb64fd5fc706cfe8cd08d36bc4ddaae787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2700; amd64

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

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:fdc85301d62fc1dd5656ac1b149eab207be692b63fc8329ba827fa895a5e01cf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207196322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f1f0e3fe0ccfd55be3c897e75720c9e494884634fd89e029452b57dea3571e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 00:56:26 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 11 Sep 2024 00:56:27 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 11 Sep 2024 00:56:28 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 00:56:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 00:56:36 GMT
USER ContainerUser
# Wed, 11 Sep 2024 00:59:43 GMT
COPY dir:6441dab14d212c21b2c8fcb6fc00e95950b0c66ee3c049dbfd71b18f09e541f6 in C:\openjdk-21 
# Wed, 11 Sep 2024 00:59:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b92e12c8f6ec07a21a2271d3953b9e4199d822f6336369d764ad7fdc1bf812`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab47d59758ea3159f4898e3cd3a8372bd6483dd1d570fb9bfe683d653a042c6`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d00b86dc2ec21fdab4595f7240c2ff0ff21ff173e345376c512154bea1054b9`  
		Last Modified: Wed, 11 Sep 2024 01:28:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08c629607bc5b9c1be71f291aed5469a2a49e901959d71212f8677ed9de5382`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 68.4 KB (68440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfa7f4fb49e97d65a836414e690c0ab71ac0f6e67d8f65a912dc39cc2932f7`  
		Last Modified: Wed, 11 Sep 2024 01:28:56 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe955d33ec6a0d0889c4e692db9bae2fa2ae9c0857d193402097a37241a1acd`  
		Last Modified: Wed, 11 Sep 2024 01:30:33 GMT  
		Size: 48.7 MB (48667142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dae604d4b790700971a1efcbf05c0bcd157faaf0eb0cef429f8c9a02118a3a`  
		Last Modified: Wed, 11 Sep 2024 01:30:25 GMT  
		Size: 3.4 MB (3374136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
