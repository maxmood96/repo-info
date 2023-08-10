## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f7910cd09675637a168bbb926a0c269fcf99f096ca0db1e95414ab2da2061338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull eclipse-temurin@sha256:c1fcc083c21856f04e8f709c57e08a5e737ce1d735be741c39aace70c8f41305
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150973930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8159f626ddfe8cb2401f579ce1f6dae54861ac2d2aee2165d9321f609768df`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Wed, 09 Aug 2023 23:57:43 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Wed, 09 Aug 2023 23:57:43 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Aug 2023 23:57:44 GMT
USER ContainerAdministrator
# Wed, 09 Aug 2023 23:57:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Aug 2023 23:57:53 GMT
USER ContainerUser
# Thu, 10 Aug 2023 00:01:50 GMT
COPY dir:9ca8bbfe0bd954313c0faf4fbb854bc33f4a5f49acc779e58df6b82fee73dcb7 in C:\openjdk-17 
# Thu, 10 Aug 2023 00:02:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fab2f1b4b5e09c41470cd0d00203e072902c23b641b71da208238f61b643cd`  
		Last Modified: Thu, 10 Aug 2023 00:26:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64cd068bf728932114b596526f700e39bf1adf08dc098a246fb471844711d0`  
		Last Modified: Thu, 10 Aug 2023 00:26:26 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840274b640fa771b658460543d3d998f6108b82aea947d767547f134a58cde9c`  
		Last Modified: Thu, 10 Aug 2023 00:26:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab521faa44bc1c2679dadb5cb63cfe3f14765ce8ad500d87db87123477d7686d`  
		Last Modified: Thu, 10 Aug 2023 00:26:24 GMT  
		Size: 68.3 KB (68332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8f6a20e3efb2de4106bad4cbc6f284797b67b0e69462f1a417e4ceb8db7e5d`  
		Last Modified: Thu, 10 Aug 2023 00:26:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94afb6229d977b56073a8e9a3cc99fe2ab181600be58fc3559080b77bdf09500`  
		Last Modified: Thu, 10 Aug 2023 00:27:45 GMT  
		Size: 43.4 MB (43403509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bd4e14ceb7665772de197b7ca285f1a6c69b0ff49627bf57b1922af2d28af2`  
		Last Modified: Thu, 10 Aug 2023 00:27:37 GMT  
		Size: 3.0 MB (3037408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
