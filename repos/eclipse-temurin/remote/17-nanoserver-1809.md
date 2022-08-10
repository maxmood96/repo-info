## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:49817481634bcaa53a02021144638deeb16cdf8396846d39342bce3ef46d0ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull eclipse-temurin@sha256:a0b495d26ceb33782686f6ebc34e769e1d4c1b2b416c1772892a9002b7d22273
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292251141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed34968a9bdd0d25a9aa6e129d1b5b0c31e05d5bc83596aafdd5b9281873e28a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 15:57:07 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:15:01 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Wed, 10 Aug 2022 16:15:02 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Aug 2022 16:15:03 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:15:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:15:12 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:15:27 GMT
COPY dir:be8ac85d984fd6d07ec942e6824366b313a501643dad7e29e6805d4aab47b44c in C:\openjdk-17 
# Wed, 10 Aug 2022 16:15:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:15:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0f4438539876006761cb687527bd8cb94cc7a273cf8bb47563981044f2e1771e`  
		Last Modified: Wed, 10 Aug 2022 16:38:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8036b9d6d653f3f49c26c75410a8bc5fa7343a801bdd59844aa0af69c4fc5d27`  
		Last Modified: Wed, 10 Aug 2022 16:44:11 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fc4dad1fb9cdc0eb7d42893a9adf6aa618a5f2368b429838f4f4584a320b72`  
		Last Modified: Wed, 10 Aug 2022 16:44:11 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082b31e68276496e65afb15a5c0e469d935d91cc39d500ced948654c5e28525`  
		Last Modified: Wed, 10 Aug 2022 16:44:12 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9b55f1dc603701feff149984c13ed1bb2a780e935b3a967ea6e2b257d9bf79`  
		Last Modified: Wed, 10 Aug 2022 16:44:09 GMT  
		Size: 74.0 KB (73984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9c75f6dbbdc460cf364a2088e3a384a624fbdb085141d8fe768d0b64c0ece7`  
		Last Modified: Wed, 10 Aug 2022 16:44:09 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52e00e66b4749caa0fc829d9567bcbe127edd5574fc5d24f545fe9f825eedf7`  
		Last Modified: Wed, 10 Aug 2022 16:44:29 GMT  
		Size: 185.3 MB (185341991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba70e86a78a88b58ca49909fcc46d5e7fb3f83d7386dd84b83f6cce728b816d7`  
		Last Modified: Wed, 10 Aug 2022 16:44:10 GMT  
		Size: 3.6 MB (3624064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eb12d6490d21cf23b2369c8bf4ea984e35e011e3d6156772ec02698e559a93`  
		Last Modified: Wed, 10 Aug 2022 16:44:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
