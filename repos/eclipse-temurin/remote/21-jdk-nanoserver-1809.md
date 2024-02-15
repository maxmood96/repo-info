## `eclipse-temurin:21-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a46f27d4a24fca05a601fb670a8884ae5c719857a7b55b18ef8974c44dace46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:21-jdk-nanoserver-1809` - windows version 10.0.17763.5458; amd64

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
