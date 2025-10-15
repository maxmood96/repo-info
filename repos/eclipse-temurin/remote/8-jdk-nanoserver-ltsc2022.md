## `eclipse-temurin:8-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cfeacadb9c261e1b000b70b5b89be5d7070ec84f80178f3d1e7cb8e30fb08306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:b160919fd7f5ebb9a29b013c35b52ef7433e899c8dede86401ad0005a64956eb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225296527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae62305f586262e495ed35448a5a95bd17bec459a77ed41b2e15003b758841f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Oct 2025 07:34:08 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 21:12:07 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:12:07 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 14 Oct 2025 21:12:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Oct 2025 21:12:08 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:12:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:12:14 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:12:30 GMT
COPY dir:184da149c84a7d26eb59eea9818ea043a400cd17024f2fafd00950f1891aab87 in C:\openjdk-8 
# Tue, 14 Oct 2025 21:12:33 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:f68a3bbf3ee20b515c5b8b801e5627a9dac3782ef264e37060c34ed80e5d8874`  
		Last Modified: Tue, 14 Oct 2025 20:41:53 GMT  
		Size: 122.7 MB (122688886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97004b1f45dbb42e74fcf45291378b73026f24a385f84780f274b7ff65e64f78`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a5e2e840ed858975f259029021871b39be11c8cc90d8615d545573be18f0bc`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edaf4113dfe39dad00ef2e74586bffee7cee3ffd3ea9ac1c2d0c84755e08535`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d12589893c1c46d2334bf0311c52558a5a8f62a3ed47fa79b74e411a0e6428`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2811401b9d364cadc60fb742c8f3fd8200d7b613ee40dbce5876ee91f17fc1`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 70.9 KB (70909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593d65fa2caa9ca7012af127613232ff44009e96d790cc7c916b0b7ae3773a1c`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b196cb61631dec766e3e9a22b6dbec08c76f6a87b0a797b6c72af83fe7c8c1e`  
		Last Modified: Tue, 14 Oct 2025 21:13:27 GMT  
		Size: 102.4 MB (102434522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c54dd3c4afad67a783afbcd064983a67429bca4e31ca728d40b807fd0c37f63`  
		Last Modified: Tue, 14 Oct 2025 21:13:14 GMT  
		Size: 96.9 KB (96896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
