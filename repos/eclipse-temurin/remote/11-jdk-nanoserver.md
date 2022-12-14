## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5cbdf1bd59d493a728052492b2deb3161772f05721451581062f9e0a6313cf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1366; amd64
	-	windows version 10.0.17763.3770; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.1366; amd64

```console
$ docker pull eclipse-temurin@sha256:8678f3b8c0fdd84a3461aeb9f1007154d16af5afac87658b6cd0dfd97e74d63b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314787654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309234383eaacdf7df9085b67d2f102d99e57068052a7c29ef16f58713a05a2a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 Dec 2022 09:19:21 GMT
RUN Apply image 10.0.20348.1366
# Tue, 13 Dec 2022 23:42:18 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:43:52 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 13 Dec 2022 23:43:53 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Dec 2022 23:43:54 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:44:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:44:07 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:44:25 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Tue, 13 Dec 2022 23:44:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Dec 2022 23:44:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70d3e1cc3b0ea172dcc93064fe6fb9f1f2c8fec6962c90e39991fe89a3c1ca03`  
		Last Modified: Wed, 14 Dec 2022 00:08:13 GMT  
		Size: 122.1 MB (122108200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8147315b2e02d672b57634f58ed466ba0f8747ed03b8d3d40b71ddb17275cf`  
		Last Modified: Wed, 14 Dec 2022 00:07:43 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb94d83b63b52ad108115f9f418e8e892eba45f96177f5fc313292b015bc683`  
		Last Modified: Wed, 14 Dec 2022 00:08:42 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d9005d9a7cd8ec9093aa3eee2fee7817562bfae5e8904ab28c81e3ec335dd0`  
		Last Modified: Wed, 14 Dec 2022 00:08:42 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2165df34ac053d89d45e349d186b50eedd9f3cac512257edc6caab4d25dc4d16`  
		Last Modified: Wed, 14 Dec 2022 00:08:42 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52739d4fc84669becc74b1e504faf4bb34f213b9ce78766adc5ece4154d05c99`  
		Last Modified: Wed, 14 Dec 2022 00:08:40 GMT  
		Size: 75.8 KB (75769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fae8e48107aaf4a924d7597a62d28f75b362ee701e63d11dac65622a2faf012`  
		Last Modified: Wed, 14 Dec 2022 00:08:40 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4081bfa7c96bbee0aa5c64d58b22327a1e8a2f2fd98ade974bed7535952e4724`  
		Last Modified: Wed, 14 Dec 2022 00:09:01 GMT  
		Size: 192.5 MB (192524479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f678c1333f197a15362a0650826384d63bd0e55baaff5be0f78f7435e0376b81`  
		Last Modified: Wed, 14 Dec 2022 00:08:40 GMT  
		Size: 72.6 KB (72609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a186dced065bd40a108b970bb690fd51fa249bccb8ab12d18db2bd76ff2ee813`  
		Last Modified: Wed, 14 Dec 2022 00:08:40 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.3770; amd64

```console
$ docker pull eclipse-temurin@sha256:e4005a1ce590f5218213f64b4041179ccf33be157b57935a51e5f38f8bf1c23e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299347755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfe0f426c0cdabbd8c5bf251ede8d5c38badb041dbf97defae8dfc033d1c6fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Dec 2022 07:45:27 GMT
RUN Apply image 10.0.17763.3770
# Tue, 13 Dec 2022 22:53:34 GMT
SHELL [cmd /s /c]
# Tue, 13 Dec 2022 23:06:46 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Tue, 13 Dec 2022 23:06:47 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 13 Dec 2022 23:06:48 GMT
USER ContainerAdministrator
# Tue, 13 Dec 2022 23:07:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 13 Dec 2022 23:07:11 GMT
USER ContainerUser
# Tue, 13 Dec 2022 23:07:28 GMT
COPY dir:cba9eceeddb80383417f5e5518328c343fc4183981a343fca253ea7c2e4dfda5 in C:\openjdk-11 
# Tue, 13 Dec 2022 23:07:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 13 Dec 2022 23:07:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7442c6014cd8a0820e2009cde1268b6ce4b8f86bc314ba287cc01fab93174fd6`  
		Last Modified: Tue, 13 Dec 2022 23:57:28 GMT  
		Size: 106.7 MB (106671057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fe06cbef5ac46e54edd743daf1bc2bfa36b294c7ce9104837061c41a4bde7b`  
		Last Modified: Tue, 13 Dec 2022 23:57:01 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cb8524c91bdbf6a7a33e8c0ad6dad828d186e06a513c2edc0678733ecb0f99`  
		Last Modified: Tue, 13 Dec 2022 23:59:52 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f983c21c22b46f2e7d5dffede9b9dfbd2cecbcb93b6f9c23bf737df01f17c8aa`  
		Last Modified: Tue, 13 Dec 2022 23:59:52 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5445aa3c23341b2d8090d1feb4c090e6cd90823d351d51e4ba41cb0e54b6f771`  
		Last Modified: Tue, 13 Dec 2022 23:59:52 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea8c2e4adcdc5be061df670c2a0ef13fa38bcf5974b92a3e082a835cdc352cb`  
		Last Modified: Tue, 13 Dec 2022 23:59:50 GMT  
		Size: 66.3 KB (66268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62b804a7a14a42abc99335def4bac7efc35e7ccfa62f76bdfa64c00727ecc1b`  
		Last Modified: Tue, 13 Dec 2022 23:59:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e78cfa42a7c57960a075a7d82439cea7741bec6444269688b7ec9c9679be2d`  
		Last Modified: Wed, 14 Dec 2022 00:00:17 GMT  
		Size: 192.5 MB (192523236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d9410cc297a373b3aeb479f602097ba6eb4943499c1848955a45edaee0d409`  
		Last Modified: Tue, 13 Dec 2022 23:59:50 GMT  
		Size: 80.2 KB (80227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb88661ef8ea61a2353c709ffa0972142333081e9defd92d421a46ba0d5f39ad`  
		Last Modified: Tue, 13 Dec 2022 23:59:50 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
