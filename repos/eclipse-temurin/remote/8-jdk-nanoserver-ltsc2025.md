## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:4f6e95425f8cafb7c80d1fffc06cb0f6eae0fc2e21418bbe26a05ed079579b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:750daee6b4b657a15583c333ed8ef1c8c74c9395263522a81044f7b0977f85dd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292775803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fd56d3d9fa492d2ec7cce0695bf6f9134d2cfc63ea464e1d54395f1df83170`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:15:00 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:15:02 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 18 Apr 2025 04:15:04 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 18 Apr 2025 04:15:07 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:14 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:22 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Fri, 18 Apr 2025 04:15:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b846898af65c899215abe37a5261070d807f5348c3e51850e34f0763502704`  
		Last Modified: Fri, 18 Apr 2025 04:15:34 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95dfbad90b47c2abe7545417d06d636a04f30a9ec032930b4887f67c6b74cec`  
		Last Modified: Fri, 18 Apr 2025 04:15:34 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebf9c40498b67b8a218474bc61ee1466c06c16ea8e527d8600359af2b21d16a`  
		Last Modified: Fri, 18 Apr 2025 04:15:34 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcf0d3c09c0a915dc3ba93afd27a02a277abeb50e1fb8a9b45cf3baf0829b04`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba17b81f64738b28e3ec624a36694b1aeb44f1bb7113e98f27fb608aad175528`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 76.1 KB (76101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7976a261f53c7551d16b8ac722e8461af47657db6e1fece0704a36ab2ffe2f08`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6715f4303d46b2574aced974b9aab1db305cea9975f8b438f721b0320355c32a`  
		Last Modified: Fri, 18 Apr 2025 04:15:39 GMT  
		Size: 102.4 MB (102434476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1658310c618945bdc255331cfa5758456769351733e0ffba90c9c7f5c925b8`  
		Last Modified: Fri, 18 Apr 2025 04:15:33 GMT  
		Size: 117.8 KB (117823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
