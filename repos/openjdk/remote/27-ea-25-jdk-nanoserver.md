## `openjdk:27-ea-25-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1ad2d79c54b6d09efe70e18cbac56071b58ce2f71f7456c491ddec8c26271c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-25-jdk-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:7b0d167564d55485654d6a2faa9edb8eb626dbd738f7658dcdc176264b48257d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350347471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd47c48c34e8ae7009896f9796c9df1acd078663a6cb112632662a541ce7ca35`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 09 Jun 2026 20:57:01 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 20:57:04 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 09 Jun 2026 20:57:05 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 20:57:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Jun 2026 20:57:28 GMT
USER ContainerUser
# Tue, 09 Jun 2026 20:57:29 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:59:29 GMT
COPY dir:2d44b60de7278e1e5741976187b08fdfd7908345a04ec10edcdba62993c11b6a in C:\openjdk-27 
# Tue, 09 Jun 2026 20:59:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Jun 2026 20:59:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76c41ebf41d5c1a290b00f524c70eb5cbfab22c5a307b49c5fb0c02269de015`  
		Last Modified: Tue, 09 Jun 2026 20:59:49 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267e9d252366ec800c6f5b0cde613427f7424f4533459c156234fa6a884a3625`  
		Last Modified: Tue, 09 Jun 2026 20:59:49 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ff676158e0d2c0d495fb2a77bd81dde1b15a6208980fdfe28bfef439b8c9c1`  
		Last Modified: Tue, 09 Jun 2026 20:59:49 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fd56bd89647ad166f26ff1fc4d8b13b67a19f5ad2d76a5432d9856a6e35021`  
		Last Modified: Tue, 09 Jun 2026 20:59:49 GMT  
		Size: 71.0 KB (71046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02268c2f34e1293dc9565b11fd98cf968cd2080784eba8cda83ecb22b6ca318`  
		Last Modified: Tue, 09 Jun 2026 20:59:47 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81688df2326b45e36c7ad5424e256748a0de2e92b6d7c95899e03d0365ac22ca`  
		Last Modified: Tue, 09 Jun 2026 20:59:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd166e88ef8c58e83e21d02e2fc2b03f9c24dc6ebd22de1b033aa3276918896`  
		Last Modified: Tue, 09 Jun 2026 21:00:04 GMT  
		Size: 223.1 MB (223095110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf43b7731bad18a43664916ae67c9e54607bbbe750679b4d658b07a14232740c`  
		Last Modified: Tue, 09 Jun 2026 20:59:47 GMT  
		Size: 136.2 KB (136162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfe8a90de40ba2bbd19f6e55bcd35bd36b94818e6e5793fe87c66c052a57ceb`  
		Last Modified: Tue, 09 Jun 2026 20:59:47 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
