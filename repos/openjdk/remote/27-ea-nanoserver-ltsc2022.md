## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:798d803b46f60828d0cb39627dab29a2a7020d20f6d37df576d14f7742ae33dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:5d49f47b138e8bf5a20a279df8ed94bc2d81a45faf7d91257f750626da9d9de8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351141434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a341006d8b064831d9134cfece918693c1a3bd4d4a59170b0e4492b7ca756207`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 13 Feb 2026 01:11:50 GMT
SHELL [cmd /s /c]
# Fri, 13 Feb 2026 01:14:51 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 13 Feb 2026 01:14:52 GMT
USER ContainerAdministrator
# Fri, 13 Feb 2026 01:14:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 13 Feb 2026 01:14:54 GMT
USER ContainerUser
# Fri, 13 Feb 2026 01:14:54 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 01:15:39 GMT
COPY dir:b6c1882cd38fa8bcaed3eaff150c211b52c7be8cc1588db9cefe115dd4b4e6b6 in C:\openjdk-27 
# Fri, 13 Feb 2026 01:15:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Feb 2026 01:15:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cc2da1daea54f1cf84245cd706060bed9755e4a888051af1fdd2840e00426c`  
		Last Modified: Fri, 13 Feb 2026 01:13:53 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df00c0e0eccfec9b223dec64d9c9e353cc5eeebf47966c075e19a48ca3d9b93`  
		Last Modified: Fri, 13 Feb 2026 01:15:50 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f12f32be63d4f1fbfdd52baca840f8ba2c69e86d9950392d2ff94a13f1c5f`  
		Last Modified: Fri, 13 Feb 2026 01:15:50 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264b8a2eac80d91459f1551e2ebcfad267c9873c3915178eb5e65e819e717183`  
		Last Modified: Fri, 13 Feb 2026 01:15:50 GMT  
		Size: 77.1 KB (77072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5854911d7a40c35af1f9c5517ce40c528efb6238be7585f7b83848ca86ceefa`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9c676ebd3888f17abbe68ff1f17283c4e863c263af4753d594579d70a9dc83`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b928b456cbc24738d8b6f78aa5a574e338429e9ab2f0bc485fd0001317bee48`  
		Last Modified: Fri, 13 Feb 2026 01:16:09 GMT  
		Size: 224.3 MB (224305082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691b318bbf43a2266c6de263c4db3dd1d83ab4dcf56532911ae9cba8d1badf0`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 107.0 KB (107020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6efc59978ecf395ab11d6795013e262daa7a40bc0bfaeaa70318194484bca3`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
