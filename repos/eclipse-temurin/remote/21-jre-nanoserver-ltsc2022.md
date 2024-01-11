## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ff9c268acd4640a5f9c5a0c5e0058d4a21a2f8dbb50ac8c37d8f4f4075d85d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:0a59c7ef83a40d30c20ef992a3835292164f5c0e1cba5c8ba4af02c2a5823608
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169603284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422e58a686d99017e827438bb3882cc2862654d097dee9920c61673986cd089`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:21:04 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Wed, 10 Jan 2024 23:21:05 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jan 2024 23:21:06 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:21:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:21:16 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:22:04 GMT
COPY dir:a5a397b00294543a7015e10bed54514e1c5f8af5ed3eff5933ba2b604ae103c1 in C:\openjdk-21 
# Wed, 10 Jan 2024 23:22:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb0820211400dec4e153c1886927282ab505977cf5c264b923c75db3505330c`  
		Last Modified: Thu, 11 Jan 2024 04:21:15 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95aff2991b8667c66d40974dc6bf32c04ed96d6225e5cb7759c418f68a6edb37`  
		Last Modified: Thu, 11 Jan 2024 04:21:15 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf3bc46f30940d81e38a97c0cb0383d2a82784e1543bf5e8febf0d5903d5505`  
		Last Modified: Thu, 11 Jan 2024 04:21:15 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a532a318c9949ef279ad340461a67508a00b13ee829f7d49d80a2b2c68cef80`  
		Last Modified: Thu, 11 Jan 2024 04:21:13 GMT  
		Size: 83.9 KB (83908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5936bd13281cecf6165dbc08623caec1e1a756b44deb81a196b0c87713de4310`  
		Last Modified: Thu, 11 Jan 2024 04:21:13 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4bbfd26b2fbbe7e5b55aeb43215d9e410661f96eaba35588c9fd888db8a9b`  
		Last Modified: Thu, 11 Jan 2024 04:21:55 GMT  
		Size: 48.7 MB (48689656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1328db2b3fb8eb4e0ee1e9e69993fc5fe3f3c86560bdd6b6aab54205bd89578`  
		Last Modified: Thu, 11 Jan 2024 04:21:45 GMT  
		Size: 54.7 KB (54651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
