## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b14bdcc0be071107c17471710c52399889babcd0ff1b11589206973de2b15574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:e3d7e488f96ed9ca90c9877db2e50493d0a9a14bc9dd52aaf3187b75e045d79f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166655530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd82762d67add87d1b58aa804f67d8f17c3946db1c39c86a8af5781db42817f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 19:17:37 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:17:38 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 19:17:39 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 08 Nov 2025 19:17:40 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:17:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:17:49 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:18:07 GMT
COPY dir:6bccbcbb352f3cf6e189ef0696470e3588f387208e54e5af3934c804c91ec072 in C:\openjdk-17 
# Sat, 08 Nov 2025 19:18:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7042b3250860a11dda92ed454adc0a818752c23eaaa10deaaeedf2077949db`  
		Last Modified: Sat, 08 Nov 2025 19:18:32 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25d8495d28495dc140877473aeff3ac4704624408195e70d5f490788a905709`  
		Last Modified: Sat, 08 Nov 2025 19:18:32 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d367aab2d7688b425476491572fc277173ca4b3cf5cc6dde9cc66efbaccdb8f9`  
		Last Modified: Sat, 08 Nov 2025 19:18:33 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7126cab21b818d2d004db3305572db9ce27e843024f45085432bdf5080db5d72`  
		Last Modified: Sat, 08 Nov 2025 19:18:33 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af22fbfff12cf83092bf648ba04a9db0a7f3dcdbf027f5e4fc7eae90a955f75`  
		Last Modified: Sat, 08 Nov 2025 19:18:33 GMT  
		Size: 79.3 KB (79334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6fc6eae8d1d5c1782e830ea04ec2d13c46d04122cef3f9c560d44b011147e1`  
		Last Modified: Sat, 08 Nov 2025 19:18:33 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f00ae3ab3368e037ea4b50e822aadb001da1ba23c563d9f66a25a9ad703557`  
		Last Modified: Sat, 08 Nov 2025 19:18:38 GMT  
		Size: 43.8 MB (43796258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f095b74005d3764221d10acc54543c987dfddcc2b36598a5924c3ca568be7396`  
		Last Modified: Sat, 08 Nov 2025 19:18:34 GMT  
		Size: 90.5 KB (90515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
