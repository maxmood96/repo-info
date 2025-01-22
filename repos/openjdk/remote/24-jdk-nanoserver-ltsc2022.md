## `openjdk:24-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:63d9dd105da5c662b45c0d39317c3007b2f0c4b4d242082458ac9dad6dd845a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:e14e67657134d6d0902a71af72393fdc40b66dc5107adcdd267b15e8800ccef9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329320214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863282a030a2aa1629d5ba845e292d0274124a8a1c33aca77346707a1cda269b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:30 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 20:44:30 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 22 Jan 2025 20:44:31 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 20:44:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 20:44:35 GMT
USER ContainerUser
# Wed, 22 Jan 2025 20:44:35 GMT
ENV JAVA_VERSION=24-ea+31
# Wed, 22 Jan 2025 20:44:43 GMT
COPY dir:ad771fa0c4659d73c3b630b6d3ca25a6a36b0b9af26b2bc144bd47e6e5f888f6 in C:\openjdk-24 
# Wed, 22 Jan 2025 20:44:48 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 20:44:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4da790ce7e0bc9bc5527502aab7f8d02d68ddf1e0926b46fc3112ac27f69c16`  
		Last Modified: Wed, 22 Jan 2025 20:44:55 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656645a5f3ed4ee1b9e56df8c9e0507033d6534b1a05e31f02fd9d7dcd00577f`  
		Last Modified: Wed, 22 Jan 2025 20:44:55 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341999707437ae6dab279f47451366859af9298e9a49c1e5e5b75e6b11601a42`  
		Last Modified: Wed, 22 Jan 2025 20:44:55 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1181fa3b7074075922c7979151ec5b0c8b59692b45f76d9eb1ee689e850725df`  
		Last Modified: Wed, 22 Jan 2025 20:44:55 GMT  
		Size: 78.0 KB (77992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073e983b8eede664526e1d871b997c236727e0f045e6f00e12e28362f29b1f21`  
		Last Modified: Wed, 22 Jan 2025 20:44:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1991888116fcf5ebe1cfee00371456e6f2b0f47d8c75847a39d72953f9aab885`  
		Last Modified: Wed, 22 Jan 2025 20:44:53 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4cd0021cd371cb24b7f138f645b4ecc34812efe3ab6b2e2ee5f5fe36ee5009`  
		Last Modified: Wed, 22 Jan 2025 20:45:05 GMT  
		Size: 208.5 MB (208467432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674a08e1b51c9ef604dddc93d8307837d816c57236e911b1c55f4cb80957579f`  
		Last Modified: Wed, 22 Jan 2025 20:44:54 GMT  
		Size: 107.1 KB (107069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f241ef8f6ffa94527cf9be59d7250b6326c0b963594e48efc9b8fd8fabfee7`  
		Last Modified: Wed, 22 Jan 2025 20:44:53 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
