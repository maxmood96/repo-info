## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:65b442b327928024b0d21a34124363b7d75969e100f91cde908c9779b76242e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:39c0b19d6852864e81569136d8a9602a5ae489640152c25fc9c10260c8c6308b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350456614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805f6f4ebf62cd884d218adcc4e955189a4ada357975c58994a828d4b80ff175`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 01:09:34 GMT
SHELL [cmd /s /c]
# Tue, 16 Dec 2025 01:12:45 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 16 Dec 2025 01:12:46 GMT
USER ContainerAdministrator
# Tue, 16 Dec 2025 01:12:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 16 Dec 2025 01:12:48 GMT
USER ContainerUser
# Tue, 16 Dec 2025 01:12:49 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 01:13:47 GMT
COPY dir:1fbd408005587e5be2ee9227fb6a081e87d3544117c99f827373a71a72099927 in C:\openjdk-27 
# Tue, 16 Dec 2025 01:13:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 16 Dec 2025 01:13:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1534c7635137aae9170bdf1c71b679926ddb9fe813e926158a336cb217fd1d85`  
		Last Modified: Tue, 16 Dec 2025 01:12:24 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6da3179fff036355b07555c26dca8d49e6b476a210ce4b9ec39c5337c39664`  
		Last Modified: Tue, 16 Dec 2025 01:14:25 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd84c383922d370f01ab2bbac0221da629ba50d2b0ccbe5b6d5874e61097d136`  
		Last Modified: Tue, 16 Dec 2025 01:14:25 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3388583a15a00d1d7418fd3b1dc6206eb87ee25dca0b43689ca565b11bc7ade1`  
		Last Modified: Tue, 16 Dec 2025 01:14:26 GMT  
		Size: 77.0 KB (76957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370bff5d44cda22860e7d7c28d2eb89f6af621f8e408c9930639038414eaaf50`  
		Last Modified: Tue, 16 Dec 2025 01:14:25 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd5a1b58967bc414809fe2401516c97a92a115f50ece0c200e277c0674bfe8`  
		Last Modified: Tue, 16 Dec 2025 01:14:25 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6444ffdaae98861e55c088613ff2d89f27f1c2f574e4ec0fe1d865c3d1e42d`  
		Last Modified: Tue, 16 Dec 2025 01:14:56 GMT  
		Size: 223.9 MB (223873856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d3672992ebbcb335859b0ec48c673963c25165a0f3999a428f2952b9862283`  
		Last Modified: Tue, 16 Dec 2025 01:14:25 GMT  
		Size: 141.0 KB (140979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1130cd1a80bc3c6552bd5065db1b873fa143697798685df7d2c02657e133269c`  
		Last Modified: Tue, 16 Dec 2025 01:14:25 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
