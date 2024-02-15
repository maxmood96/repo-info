## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ab2905c8a5f779298e715c4d8a869639da7799307ea8fe6e48adf0ff91ea289c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:353c4288a347c8ae6ed649736956ebb2dcc53e6d5f0b639d37d07a69063d2466
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222581502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5226fa57a8319fc2effefc1bc4eb991591e130db2cc2c54dec323edf18876`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:21:03 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:21:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 14 Feb 2024 20:21:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Feb 2024 20:21:05 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:21:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:21:19 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:21:31 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 14 Feb 2024 20:21:46 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a8b9610542d9f544621b5b605f3c73832b279a3681d70286c37473fec95b2`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320c7f4aec5883a29011e6e9f92ddb22af540f7c4ffea76399db2f2e482da79a`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b236d5717e24cb1456735c67ed3334020e2dfb2d9b085f9908382d2b644f523`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab249bb6a4cb870af2fcc419628a502aa14f8335ad1e8c860421de5ac822d80`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d029d4a51c18b6e328ce712709d3a800ffd3838d1405bb11039e7b50db11a`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 80.4 KB (80434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de18572ccdee2cf25d4ca67517fc6a7d6cd78cfdd2f34fde0b0ed0a959d57c0`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b6f43eed8ab6412f807865eb849181f48eb9f5b8d249099bc264699ef1b60a`  
		Last Modified: Thu, 15 Feb 2024 00:16:39 GMT  
		Size: 101.7 MB (101699111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc62a9b8420beef74005d3f5dabf4d4f0e0ad50ce484a5dc4b445361ef330ce`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 61.1 KB (61071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
