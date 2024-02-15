## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0a6ae8faf9316b5b2f35343eaef2e45972c9990e23d7bb2351e97bc74182454c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:5fad7e6ac15cb843900520bfd941187e1d4b0c575393d9fc3202a8b696c35a6c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322014935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc91d959409194bc499ddc1c8a13bb8816ac697242c167ccf0cae92671438cc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:21:03 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:25:06 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 14 Feb 2024 20:25:07 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Feb 2024 20:25:07 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:25:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:25:19 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:25:37 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 14 Feb 2024 20:25:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Feb 2024 20:25:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a8b9610542d9f544621b5b605f3c73832b279a3681d70286c37473fec95b2`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbdac88a025f13a3d52a2c41f868ef6a818f96d83f7f1bffd097f5d6e8e1ed9`  
		Last Modified: Thu, 15 Feb 2024 00:18:41 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292e726426433285b45b2c16fc8c88e0e23960f6d07d9090e6246d79a8bd41f4`  
		Last Modified: Thu, 15 Feb 2024 00:18:41 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65995336618fe22920f72d475ef7da8c69d8bbc48214ce78aece1c38c5b5cb43`  
		Last Modified: Thu, 15 Feb 2024 00:18:41 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384e406daa042a2f6e649bc4c5784219ae46b5cce7b446be355e99d53d3962e0`  
		Last Modified: Thu, 15 Feb 2024 00:18:39 GMT  
		Size: 85.3 KB (85253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b7fc31ed1b05b2eb54050ee8a646cc9584a6417e835b1b491ebf02d7f5059c`  
		Last Modified: Thu, 15 Feb 2024 00:18:39 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439ead5f44138e5340578838404fb450ba9c25687ee7797ae7a46a140ec67619`  
		Last Modified: Thu, 15 Feb 2024 00:18:57 GMT  
		Size: 201.1 MB (201125620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76b46baeed0bffad0acf1f0a61c10eb8231f26432e4375d2baba5241fe464d1`  
		Last Modified: Thu, 15 Feb 2024 00:18:39 GMT  
		Size: 62.0 KB (61995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e895840ebed243a67825dce0a0b5027d21ecfc031b40bf32c2d84f0cedca1af6`  
		Last Modified: Thu, 15 Feb 2024 00:18:39 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:e47ff02ab0e9073e79ff0fa224952501c909b111eae7aec5f7f42efb6bf7b0ab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309638907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a13302880dcc1014640845eb87cb08693bbb0d79433da2a83b5f0e8d8cdff0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:41:52 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:14:57 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 14 Feb 2024 20:14:58 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Feb 2024 20:14:58 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:15:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:15:08 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:15:23 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 14 Feb 2024 20:15:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 Feb 2024 20:15:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddfc54d18bb5861232283d3ff2ca5e214ade28a46dfcf6c1e7c7243809e5e85`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b5ac0c0039279c81ef8a0b73777c70eb0f4154275b16090c8d8dec0b0b5f7d`  
		Last Modified: Thu, 15 Feb 2024 00:15:02 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36850236406ffaebeaf74d5c2af7a8bb2637218fb04780435d349be93ed40816`  
		Last Modified: Thu, 15 Feb 2024 00:15:01 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417a71895a6404699264769031380768677b589482a450b1e835203f3ab11b4d`  
		Last Modified: Thu, 15 Feb 2024 00:15:01 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6471b0637a32e9a57c629c854d2e57b0626e0f458f9b191e94eb4bff975d5551`  
		Last Modified: Thu, 15 Feb 2024 00:14:59 GMT  
		Size: 67.6 KB (67568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797ef2bc893d6f044556f13a437c95f1432144cc0f7b015cbb179b2344846182`  
		Last Modified: Thu, 15 Feb 2024 00:14:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69c20a384c933e3039a4efc9792075a04c02bb8d4b6c8c3201ed69bd824a334`  
		Last Modified: Thu, 15 Feb 2024 00:15:18 GMT  
		Size: 201.1 MB (201125617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6922956b4c8749c5cd1a8534eb085546c0763f8575b38a3e60b543b5e5257641`  
		Last Modified: Thu, 15 Feb 2024 00:15:00 GMT  
		Size: 3.8 MB (3817204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380c5502454670c4a5a654f13ae915b110ece4ffeccbd78bab69c6fa1dd937d5`  
		Last Modified: Thu, 15 Feb 2024 00:14:59 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
