## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e1296fac04f3e298f16d288e1b71fc164dd7b70904dc82a5bb3f4e53e81dbcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull eclipse-temurin@sha256:19f19c1aa0dcf9797365183bdf704243e448033d999def7f632d5f5dea42e2b4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160781543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7191a6c58f0c9b162746e04c49dce996ff614a3e7385549cdb88063287e71ea4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 00:50:29 GMT
SHELL [cmd /s /c]
# Sat, 22 Jun 2024 00:50:29 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Sat, 22 Jun 2024 00:50:30 GMT
ENV JAVA_HOME=C:\openjdk-8
# Sat, 22 Jun 2024 00:50:31 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 00:50:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 22 Jun 2024 00:50:43 GMT
USER ContainerUser
# Sat, 22 Jun 2024 00:51:21 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Sat, 22 Jun 2024 00:51:34 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c04e6fe7f33e5ed7b73641c362d031eb0404b55967c9af2b8fa6f2269d9f92`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b174078aa7a66a8b622abdc2a54e532be01686cada8b14b73b36ea06415eb6cc`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ff4188cf271748f13726e82487fe15353b089142d1af3090ccb2c007885b0c`  
		Last Modified: Sat, 22 Jun 2024 01:06:26 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ef3ce5545b1eeaa16986a08c1644cfcf0acdb70e03c9613088e7f5a3588271`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8445abea445ef1c0fe004a0b917c558137e71f35550eb457adf5f148f579d83`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 94.8 KB (94840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a8432058d09db20b0fe84efd2d8c3eb4c5371e198e6b9cde3fee1535706bb3`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6669f7301398516655daa649b0c3a9af1ccaf71beb7a29b09a71111bc4b4ff`  
		Last Modified: Sat, 22 Jun 2024 01:07:04 GMT  
		Size: 40.1 MB (40112824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70664acc2afb3344a8be4c7128f2ac8471543e7a78a7db148e71a76807bbe256`  
		Last Modified: Sat, 22 Jun 2024 01:06:58 GMT  
		Size: 68.5 KB (68524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
