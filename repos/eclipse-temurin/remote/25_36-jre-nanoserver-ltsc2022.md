## `eclipse-temurin:25_36-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c4a0c5a8406b1aa2c31ce037219cf50698ca4eb54fbede685bc5ab93fd794cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:25_36-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:526485b19b136857b54ee12c07b040829d0b9f8f21534a5068ec009a024c1e6e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181472466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35839ffaaf1b7c8f246c994c145c691d059b022e8cbb116b0124af962b8f1591`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Thu, 25 Sep 2025 22:12:47 GMT
SHELL [cmd /s /c]
# Thu, 25 Sep 2025 22:12:48 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 22:12:49 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 25 Sep 2025 22:12:49 GMT
USER ContainerAdministrator
# Thu, 25 Sep 2025 22:12:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Sep 2025 22:12:58 GMT
USER ContainerUser
# Thu, 25 Sep 2025 22:14:55 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Thu, 25 Sep 2025 22:15:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc44f684fa662a44ac5b5fdb2c6bf679052cd2d8ffbbd0649e5c186ad49ac5f5`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c71fbba26ccdbd7a60d6ef3a48c82fbefbee275341b6784a2076f9bc61b955`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdb1175fae153d8d5bd8ef1d8927b294bf8b3db598b2c37949a160f75b4ad6c`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26916416afde07316880254c82e0a6ba3832ed32743e01d44435dd14d47e025a`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db585771e906d79dcc800547cc747763294d71921f77e1df13f53ef3c4172fe8`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 83.9 KB (83932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317ef0bf3caeb82f3ca2dd89ed5f2c21b6473555cb9a3a753888167c899fdc7c`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe5b55f211e15e492d202216cf2c40b3e450df2a456e1131316cbde3962f15b`  
		Last Modified: Thu, 25 Sep 2025 22:15:24 GMT  
		Size: 58.6 MB (58551017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126c6ac628de928cce8c51600bbef9ffae5931e6af7c46320cc0f332e9d82036`  
		Last Modified: Thu, 25 Sep 2025 22:15:19 GMT  
		Size: 112.3 KB (112284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
