## `openjdk:24-nanoserver`

```console
$ docker pull openjdk@sha256:7a0b7a777ab201bdf834a19a10f8ca1d929516375b4bb64a4fc9c0ce7e33479e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:b81d156901ae1e80001c5d76d1e0451d18859f8f577006acff6e449efaffab9c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367274873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fa9aa83db2f99f5b262410dfc7ca0a03ce431790433068e83e1dba4c354e09`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Thu, 29 Aug 2024 21:50:17 GMT
SHELL [cmd /s /c]
# Thu, 29 Aug 2024 21:50:18 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 29 Aug 2024 21:50:19 GMT
USER ContainerAdministrator
# Thu, 29 Aug 2024 21:50:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 29 Aug 2024 21:50:31 GMT
USER ContainerUser
# Thu, 29 Aug 2024 21:50:31 GMT
ENV JAVA_VERSION=24-ea+13
# Thu, 29 Aug 2024 21:50:43 GMT
COPY dir:2b85fbead721240234e1d9883f0dc389a2320ab86c5b670a91322ca179f85034 in C:\openjdk-24 
# Thu, 29 Aug 2024 21:50:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 29 Aug 2024 21:50:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97776373b2514c4d508129b4c9cc30baf32fdd7d5b2698bb703ee9351bebb0b`  
		Last Modified: Thu, 29 Aug 2024 21:50:56 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9919ed3ad386315ccae109faa9517c17c5a8ef102094bb9bd61b7a8036c9d3d6`  
		Last Modified: Thu, 29 Aug 2024 21:50:55 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00b5e34c4d0865da7b2a8eca419338b311c22cad4bd23efb3ee47c1494d4e0f`  
		Last Modified: Thu, 29 Aug 2024 21:50:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54b0151327e219e0462b3b343768e7091889a8a75fd78a476076b24c0c27253`  
		Last Modified: Thu, 29 Aug 2024 21:50:55 GMT  
		Size: 66.5 KB (66523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c8e8c702aac4036aeb23b8f7ee60001c9d8bb73d5fd5dd005ab436afa640e4`  
		Last Modified: Thu, 29 Aug 2024 21:50:54 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8ab65b64cbac27e43d029a96eaf800b6f9882f533ee07b393c76ef38bcae06`  
		Last Modified: Thu, 29 Aug 2024 21:50:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f98a1f60c2c98adb0ea15db452ed3d7ce21da567649474cddc688ae3afd1cc8`  
		Last Modified: Thu, 29 Aug 2024 21:51:06 GMT  
		Size: 207.6 MB (207628529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fff4664947e5dd1be33cd6b0372413b0f825b35efcf9d5dccbb48174e766f6`  
		Last Modified: Thu, 29 Aug 2024 21:50:55 GMT  
		Size: 4.5 MB (4490414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a68e77f5deede6a5f06aa70963b75a44264b56ee6dd1c838f99477cbec809c7`  
		Last Modified: Thu, 29 Aug 2024 21:50:54 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
