## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:004aad053d5c7963fa073d30a88f67db67b88394730391c3c0fcd535283f4237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:c5b3bd441de306c8f59cfeacf4a078c02f695b6ad54ea31546f00dc4cad3d099
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207194585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35158701992620b44fa7c00c2b8ac0269af471a64e5f96313f053a43964a14ac`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Tue, 23 Jul 2024 00:27:42 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Tue, 23 Jul 2024 00:27:42 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 23 Jul 2024 00:27:43 GMT
USER ContainerAdministrator
# Tue, 23 Jul 2024 00:27:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 23 Jul 2024 00:27:50 GMT
USER ContainerUser
# Tue, 23 Jul 2024 00:31:29 GMT
COPY dir:6441dab14d212c21b2c8fcb6fc00e95950b0c66ee3c049dbfd71b18f09e541f6 in C:\openjdk-21 
# Tue, 23 Jul 2024 00:31:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbf574c8643be142a434d3320463979f63505cb12ea751eaf2afb4f62ddb2af`  
		Last Modified: Tue, 23 Jul 2024 00:40:27 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330806fe0fd7929a9920c95862329e67f77d28ac66efc279e05c844a680b876`  
		Last Modified: Tue, 23 Jul 2024 00:40:27 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efffd37584636aa53a833b5c5846dd62625e18d372075bb4ce58b572783acbd1`  
		Last Modified: Tue, 23 Jul 2024 00:40:27 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597250a8581cffa6ddffb62b6517fa77145cb20926a760daca98a333b83f8385`  
		Last Modified: Tue, 23 Jul 2024 00:40:25 GMT  
		Size: 69.1 KB (69142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0beaac908c6bf94597150808a1bc0e0f9c0503d799d08cd4b747e88e4f297b6b`  
		Last Modified: Tue, 23 Jul 2024 00:40:25 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415493aac386ee17df647e38fcb8e5e5a9083c17b491fe0c043018320419fdad`  
		Last Modified: Tue, 23 Jul 2024 00:41:33 GMT  
		Size: 48.7 MB (48665186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ab0ceb3a509057ce7b0920e2347dd441a6c03f943a95fb8a52c694dd243c9`  
		Last Modified: Tue, 23 Jul 2024 00:41:26 GMT  
		Size: 3.4 MB (3373234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
