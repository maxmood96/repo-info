## `openjdk:24-ea-31-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8da73bb8f1080e50107a09649cc6f66befe7b6b198b0c371ab94f83633c8498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-31-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

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
