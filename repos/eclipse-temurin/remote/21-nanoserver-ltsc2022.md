## `eclipse-temurin:21-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0938be8049d85a8f0d46cf079a4cceed78d71c69d5ea7d42869c85c4660a30a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:21-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:a22fb75d041de441bd87249772e758a3aca9a1105673974f2ba05c81bf7bc36c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324317634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e29ff9d0d7ec0e94ab1a8a358e8106a079cd79a9d74c142fe6bcb7eb74063e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:21:02 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:21:03 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 14 May 2025 21:21:03 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 May 2025 21:21:04 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:21:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:21:08 GMT
USER ContainerUser
# Wed, 14 May 2025 21:21:15 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Wed, 14 May 2025 21:21:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:21:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedd84aee1625a6fb286eb4e52210c28051c7da71ad8043503a85dc0b76ff7`  
		Last Modified: Wed, 14 May 2025 21:21:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9069cab3dd72f7a589ff52d4d5d034eab7ab4218ebae88795d6354eee1fc39f`  
		Last Modified: Wed, 14 May 2025 21:21:27 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021a07171e30786c2115302d21eea6874a7325b355abc6e27bee82472d2cd1d4`  
		Last Modified: Wed, 14 May 2025 21:21:26 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b7e1372e1ed8cb1a5311ff77b9da6aa02ee61ee915dc47e8c0b41bc9ba7614`  
		Last Modified: Wed, 14 May 2025 21:21:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ba4748a0bfcaa6ba75646972f3e55a9f293f052de118ca532d183bf398be4`  
		Last Modified: Wed, 14 May 2025 21:21:25 GMT  
		Size: 76.2 KB (76205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2862f20c7c4beb93c2a2641e1e03b93a12880d55903f55dcb17f79924c8f48ea`  
		Last Modified: Wed, 14 May 2025 21:21:25 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2feea30433009b6149a96ad3d74d799d4038e2f410511a13ec700630d6190be5`  
		Last Modified: Wed, 14 May 2025 21:21:36 GMT  
		Size: 201.6 MB (201551242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577e9a7fc2afbf0b72361e52e984e7cb1fb88ef0feb1b508f43cda164513e88b`  
		Last Modified: Wed, 14 May 2025 21:21:25 GMT  
		Size: 107.4 KB (107386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132d8eab90b4863b8a3bfe3513a8d969e6b952fc2c40330b28fe231b60774777`  
		Last Modified: Wed, 14 May 2025 21:21:25 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
