## `openjdk:16-nanoserver-1809`

```console
$ docker pull openjdk@sha256:86eaf0ab44eaaf9b216b5999ec3a12e9cab93a0b2fb9cfcdedbfe6852efdacdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `openjdk:16-nanoserver-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull openjdk@sha256:4b05448801d13a47132895de056711203e1fede197d8eaca8c3387e810a83b7b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297094205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c18bcc757c4f5574e19ed2635d86357f9be07c1457304f9aa9bbd1c9e7b415b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Sep 2020 12:08:18 GMT
RUN Apply image 1809-amd64
# Tue, 08 Sep 2020 20:13:38 GMT
SHELL [cmd /s /c]
# Tue, 08 Sep 2020 20:13:38 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 08 Sep 2020 20:13:39 GMT
USER ContainerAdministrator
# Tue, 08 Sep 2020 20:13:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 08 Sep 2020 20:13:54 GMT
USER ContainerUser
# Fri, 25 Sep 2020 21:50:22 GMT
ENV JAVA_VERSION=16-ea+17
# Fri, 25 Sep 2020 21:51:01 GMT
COPY dir:103fbcaa51bd1609748b0ac1c731bc2d5e38d0f9f65746a4688f04b13a4618c4 in C:\openjdk-16 
# Fri, 25 Sep 2020 21:51:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 25 Sep 2020 21:51:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecf9bb62dc6eedea9fd367628f8715dea75b7d2053afa4b5121e7809aa692139`  
		Size: 101.2 MB (101239122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f72ec155bceaba8b4a5cdbd7aa79586c7296a801af5364a691c46191c910e2da`  
		Last Modified: Tue, 08 Sep 2020 22:29:01 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b2192657885f813dd6fa78d8ba65d02e35934c0c45121f5cb3004298998876`  
		Last Modified: Tue, 08 Sep 2020 22:28:59 GMT  
		Size: 866.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe914594cd5b7b9a0b5c0080fe6c643b51eecedb3197955dbea30a0005a9132`  
		Last Modified: Tue, 08 Sep 2020 22:28:59 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4324dc65079aab4e95e3a823193385145a250bbb9e13cd9c5e02a35844069217`  
		Last Modified: Tue, 08 Sep 2020 22:29:00 GMT  
		Size: 65.1 KB (65142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bee2eb45cc55aae1760d1937d9de7b70abd95c9488b97a8288d08b472684fb5`  
		Last Modified: Tue, 08 Sep 2020 22:28:57 GMT  
		Size: 862.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0001a12354a357e7127034dd5ebea662149b1bd60b20446a7bffd7d1ba3151`  
		Last Modified: Fri, 25 Sep 2020 22:01:01 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840f7268b85668ba72a97218b67be9d12e55de0f17ac50aa30e75c49ed6b815c`  
		Last Modified: Fri, 25 Sep 2020 22:01:21 GMT  
		Size: 192.3 MB (192292352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96ee06318eca223d8a996905c33f5a07605ade6a17310842de7091bafda952e`  
		Last Modified: Fri, 25 Sep 2020 22:01:03 GMT  
		Size: 3.5 MB (3492303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff32e2c3c330610b1517799b533f1c19803071fedd032ce65058999aa6596a87`  
		Last Modified: Fri, 25 Sep 2020 22:01:01 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
