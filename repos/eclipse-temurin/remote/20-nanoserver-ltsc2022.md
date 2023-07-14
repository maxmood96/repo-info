## `eclipse-temurin:20-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7d544a1c0bcf347f6dee5cd216bb23c3b7e0ee8d979260faa2eb857b60444613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:20-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:d2c3762206366656ffce80d0a1e73ac9af12b7565860d56058d34d776021a085
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315480883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605f3eb350bf5ca8886a1c72a54ff7684e4aae2449d6221832fe0338b115d93b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:14:47 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 13 Jul 2023 22:14:48 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 13 Jul 2023 22:14:49 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:14:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:14:59 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:15:14 GMT
COPY dir:f42e28541c92f419d16f8f9260ba58e12cc63ca253028a61fc42e8a28f91cd69 in C:\openjdk-20 
# Thu, 13 Jul 2023 22:15:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Jul 2023 22:15:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11750b624a775aa3c21a13406dfc54458855b8684e21efba5bbb9b27ee0b12`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94bb0d0af753bf3fddc242471d62baa7d6b5bf9406352f90954681f021e614a`  
		Last Modified: Thu, 13 Jul 2023 22:30:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a594dc68da02e168f45e7595f8362f0ed780c40efc668ce6fd506ed4562ab55`  
		Last Modified: Thu, 13 Jul 2023 22:30:53 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e929e087fdcae2fed2b893cd030871bd95008fe41ac19b832facb0809fa8a`  
		Last Modified: Thu, 13 Jul 2023 22:30:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e876294035e02c2a9afcb9ff43cdcf09839ccd787032e5b50c097803c6806a`  
		Last Modified: Thu, 13 Jul 2023 22:30:51 GMT  
		Size: 80.3 KB (80254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3800e7a140cdf6e9dd3e205c30a36aa7c9fa85870a2889a49adc351ce6ba212c`  
		Last Modified: Thu, 13 Jul 2023 22:30:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aa6fa78c730a307b47eaa8bc0e73d8472f0a42bf1c9b77e5bccdc91db332eb`  
		Last Modified: Thu, 13 Jul 2023 22:31:10 GMT  
		Size: 195.3 MB (195276723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5d2b4b18f18c3c58d31b8e9415695461bfb9d29a47cd2ccc40cd2a7a3b9030`  
		Last Modified: Thu, 13 Jul 2023 22:30:51 GMT  
		Size: 61.0 KB (60968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d698009ffaa588c2076be8087454ac386172e5662d81543b2adc0b599a7962a1`  
		Last Modified: Thu, 13 Jul 2023 22:30:51 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
