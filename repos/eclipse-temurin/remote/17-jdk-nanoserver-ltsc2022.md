## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:609eafdd38dd9639c595876d75ea29f3baee4a1e58d617e6db496cbeef51164e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:78e888ab29c4dfecb1e78f73a3827a230efddac0cb4414ccbc6dd31bb646841c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cdd35ee46682586f7cadbf60b336fa5ee2cab7f9a4d7908d0ff23a75098279`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:07:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 11 Sep 2024 01:08:00 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 11 Sep 2024 01:08:00 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:08:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:08:09 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:08:23 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Wed, 11 Sep 2024 01:08:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 01:08:37 GMT
CMD ["jshell"]
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
	-	`sha256:3021472a8e25674fd1e2edaffc9035ecc67f7fff59688db85cb268ac0bf1c0d7`  
		Last Modified: Wed, 11 Sep 2024 01:34:36 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bbb0629480851b9c01ab54847fe0fd454a054dbed8c2737492fc9b837e84c2`  
		Last Modified: Wed, 11 Sep 2024 01:34:36 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39578ebc4c5f739baa00595b756d93ca29d27a7bd955082e767d6d8b39a9df77`  
		Last Modified: Wed, 11 Sep 2024 01:34:36 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b37c4887ed0e155262e27bba83e5297d7c1be1e3b033c75ca59680a919d813`  
		Last Modified: Wed, 11 Sep 2024 01:34:34 GMT  
		Size: 76.2 KB (76193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ca761024e3880368ef22acc0dbb413cfd6402fbeaed7165730f565b0465112`  
		Last Modified: Wed, 11 Sep 2024 01:34:34 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f22f153e42f16308b852d06af854bf26da438af710125d3f2d4a33b8928b3f`  
		Last Modified: Wed, 11 Sep 2024 01:34:51 GMT  
		Size: 186.5 MB (186458753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91634048cebf7662fbbd5270ec9ccb1db16cbea01bc7cbc1d57bab266eae551`  
		Last Modified: Wed, 11 Sep 2024 01:34:35 GMT  
		Size: 63.3 KB (63259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb581bf15b88b7f440c20ab480563f06a613e9662ae2e4fb4a7366b0f2ab521`  
		Last Modified: Wed, 11 Sep 2024 01:34:34 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
