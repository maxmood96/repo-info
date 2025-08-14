## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:de1ecb449808a2c7097cb624021ed9dfcdc3dd65213f2944015874b81c9c4d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:c22a48802644df9c81179844d5505140507ddbda6ec6ad763156473477400ee1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237313641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769c0b98612d8c1c5c44b911ce8b874e3039879c03a583d03a5348e3264ef9ed`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Tue, 12 Aug 2025 20:50:12 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:12 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:50:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 12 Aug 2025 20:50:13 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:15 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:18 GMT
COPY dir:5e90fa740143d3cf8b62ae0c044ab32f16062893edb04b6ca1ccce56733f632d in C:\openjdk-11 
# Tue, 12 Aug 2025 20:50:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4de521e368d423965e81aa3bc557eec962714e99c884fa2c05a8e442724d51`  
		Last Modified: Tue, 12 Aug 2025 21:53:44 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e99bf49594004c5f3a8d157a14b239acd88db7f7c6dae5399b7571b1aae8438`  
		Last Modified: Tue, 12 Aug 2025 21:53:45 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb610e2503d003c88eaeaa821504ed90b3762b2b339f0a3d652b7b4cb64cf77`  
		Last Modified: Tue, 12 Aug 2025 21:53:45 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3a952d95e5b206a72dbd09a2323b7e52fd61349ad4bb3d978150daaab6ca2c`  
		Last Modified: Tue, 12 Aug 2025 21:53:45 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bc54cc99f7164261985c4aad3c7ae5a013ca9dbb20e6051fa2bde6221300b3`  
		Last Modified: Tue, 12 Aug 2025 21:53:45 GMT  
		Size: 75.6 KB (75649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4a418b90adcc81cab8bca3e70d994a25e7db8c111a7f7eab5dc1d1b83df8ee`  
		Last Modified: Tue, 12 Aug 2025 21:53:45 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8aafc5c85b52588aee8291ba6992379b8ca493ec93b1ae18898e118cb5059c`  
		Last Modified: Wed, 13 Aug 2025 00:15:36 GMT  
		Size: 43.7 MB (43667310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d742508d99d534b3d4dbc81b320cf637c44185c1986b7405d0f8a871f0a1cd`  
		Last Modified: Tue, 12 Aug 2025 21:53:47 GMT  
		Size: 95.9 KB (95940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
