## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:990a2c4d4a988419c771d3448d33dae848c8ee254ace7dd74928deb4c58fd062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:b33004007bc4aad2bb4ba7db34ca4b89303c47e6007cef7bb57fc3b0744020a3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146215812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69f909593241a52a3ea3067a71940ec3f7c1b3ee1de567beb5e6c7d3007130a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 18:36:26 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 08 Nov 2022 18:36:26 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 08 Nov 2022 18:36:27 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 18:37:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 18:37:02 GMT
USER ContainerUser
# Tue, 08 Nov 2022 18:43:46 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Tue, 08 Nov 2022 18:44:03 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c44dbc7f003b29fa4e1abb69635a1a6354a2c0cb49f6a9ff6dc4d1b639acc98`  
		Last Modified: Tue, 08 Nov 2022 19:44:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fb91c1a718c599d124b35a4ba105c41d65f391d68beed1eeb58e06660d8136`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b16510d59ce3bbef885f91367330f07ac32af4e3bbefee8ff015cd414d0646`  
		Last Modified: Tue, 08 Nov 2022 19:44:50 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63890e522e464b0c794c02a6277fb28ecc0bf6f1982be903f1f405e81d4c7490`  
		Last Modified: Tue, 08 Nov 2022 19:44:50 GMT  
		Size: 76.5 KB (76518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bffeb8602a05ed27d48cbfd978a4c71319ffe1209858cbbeda69470b489563`  
		Last Modified: Tue, 08 Nov 2022 19:44:50 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6977b8f346a3190ee1b0b6fa0fe918cebb1dc16d7b4298909acd7896c7823bfb`  
		Last Modified: Tue, 08 Nov 2022 19:46:24 GMT  
		Size: 39.3 MB (39322731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28eff27834061fb4970e8de216397ffe8e20e3872b534733735ab1dc615f7e1`  
		Last Modified: Tue, 08 Nov 2022 19:46:16 GMT  
		Size: 87.8 KB (87814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
