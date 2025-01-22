## `openjdk:24-ea-31-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:7d534263f38710015723af04c58c044bc787c2ad35540f66ebf79a18d88a0e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-31-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:22347b85360b5ac22f66bd34efaa40d73f61bb8da6b3342868d3fe35b74a44a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407709589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456d7bbc0035627f78e42fab405ec7ac9f9a44ecc41ca803d4f0f96247c9b25`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 21:15:32 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 21:15:32 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 22 Jan 2025 21:15:33 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 21:15:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 22 Jan 2025 21:15:36 GMT
USER ContainerUser
# Wed, 22 Jan 2025 21:15:36 GMT
ENV JAVA_VERSION=24-ea+31
# Wed, 22 Jan 2025 21:15:44 GMT
COPY dir:ad771fa0c4659d73c3b630b6d3ca25a6a36b0b9af26b2bc144bd47e6e5f888f6 in C:\openjdk-24 
# Wed, 22 Jan 2025 21:15:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 22 Jan 2025 21:15:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c196df0dcbcad7b28b77333688a4566bacda5c8060ecbca3e4dedf0f73ae69`  
		Last Modified: Wed, 22 Jan 2025 21:15:55 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7066d7aef230373fd2ece23b3654d905755c90bab7533adac3537944906747c5`  
		Last Modified: Wed, 22 Jan 2025 21:15:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d1002e26ba4c288d7212a99039899ac7a637a7d0c0c3c3d9e3656005f368a1`  
		Last Modified: Wed, 22 Jan 2025 21:15:56 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a5a84c3d5935b91fb5f89514d48f2d032bb6e855f692844267d96ce279d093`  
		Last Modified: Wed, 22 Jan 2025 21:15:55 GMT  
		Size: 76.3 KB (76310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d486900c52932c1190a08cb73f2a6682f3b130d4a1cc473c9ce8af7e335b25d`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11373a7808bb0589ca1a854b84a8b3ff5eba92e64e75e9fa862c34525f4cbc82`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e37ca5c11b0f8220657fee9587cb27337a200182594406a73348f127993e07`  
		Last Modified: Wed, 22 Jan 2025 21:16:06 GMT  
		Size: 208.5 MB (208468406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755a41c3977e36d93887a306686faf4b05c07716172b13ec790c4fba1c927ab1`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 104.4 KB (104383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ae810003214249113253104ea0f49582fafc8d526af908cff1e0c9e2b8e836`  
		Last Modified: Wed, 22 Jan 2025 21:15:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-31-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

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

### `openjdk:24-ea-31-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:e26d6c8235e6f4128871340ee19e3fc5174bda17290c5963691fefbed071c7af
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368262008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1279a7d7ef7f11a9f35d440d7150d8a23809e21e19a881d0a35e601519570d63`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:05:01 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:05:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 15 Jan 2025 18:05:02 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:05:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Jan 2025 18:05:07 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:05:07 GMT
ENV JAVA_VERSION=24-ea+31
# Wed, 15 Jan 2025 18:05:14 GMT
COPY dir:ad771fa0c4659d73c3b630b6d3ca25a6a36b0b9af26b2bc144bd47e6e5f888f6 in C:\openjdk-24 
# Wed, 15 Jan 2025 18:05:19 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 15 Jan 2025 18:05:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c81d60765e8ef3a34c2e37a6a343e6c2db73bed6637ff9d1b22855ee436660`  
		Last Modified: Wed, 15 Jan 2025 18:05:23 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf33d9a8a8a26b5fca4a76a239956d252027bfbea2bc5d61601be4b0fb2973f0`  
		Last Modified: Wed, 15 Jan 2025 18:05:23 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c063212cfa32309e5a30c3b13323e90e49305ee2f8e7d8313cc21bb73af7dca0`  
		Last Modified: Wed, 15 Jan 2025 18:05:23 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc745b398b002ce22b02de44743450972623aa127d97cd269c1b8f8e38fbe87`  
		Last Modified: Wed, 15 Jan 2025 18:05:22 GMT  
		Size: 73.3 KB (73326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce4dfe3a9902b658ae616bf40fa50db74c68308fde91aa933c6b5ddb0c8d0f3`  
		Last Modified: Wed, 15 Jan 2025 18:05:21 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf6e3d0e1fb366023266234f1d33e891fbbaefc80cfcdf5451f0c3830c4bf0e`  
		Last Modified: Wed, 15 Jan 2025 18:05:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491a68b735dc354553722cd6cb051a4e7d610508ef3e5003cf3ea3a2969fe06c`  
		Last Modified: Wed, 15 Jan 2025 18:05:33 GMT  
		Size: 208.5 MB (208467110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e617b304dfb3b228b779938a252ba51d4fd567b2571353474ac8af8edca0d87e`  
		Last Modified: Wed, 15 Jan 2025 18:05:22 GMT  
		Size: 4.4 MB (4447823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b3d8df019e10cbba1810cb4f2483bf162169bc6d6faba29ced1c5ef650a71`  
		Last Modified: Wed, 15 Jan 2025 18:05:22 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
