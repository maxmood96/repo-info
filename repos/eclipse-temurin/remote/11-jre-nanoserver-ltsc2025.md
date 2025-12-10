## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:48917002a26db72d4a180887beb3ed1ac1cc5518f42dbbe9fd724c1a06e4a675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull eclipse-temurin@sha256:882ddbbb7e1fa8211a0b405fa17cb7a1cc7d10bfb38934626663e8a17a91663d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242751973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd91ce30e2ca72e397a8c9867aac8f166497b29be524cdda2526f938dc3a7b4b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:12:48 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:13:50 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 09 Dec 2025 21:13:51 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 09 Dec 2025 21:13:52 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:54 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:14:00 GMT
COPY dir:4835e564d5b678d207d3850b6f40a90e0afa12e9d665c48e7909a88923b1a7a8 in C:\openjdk-11 
# Tue, 09 Dec 2025 21:14:03 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acfb819e594e1d08813b5a2124af39d689e54a1c03ce6e66c31fd39ac284a05`  
		Last Modified: Tue, 09 Dec 2025 21:13:34 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92538597b644a5bded4ada76feac9383f1903693691331622dcb04cbea99d6a6`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3f7194e141046278c81057a302dfdb82bbbf481a33690b5d3a5be2167ce119`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e571492590b91fddb2747025849d98c327cec4b53a1017b18f9203f693aa8184`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46d7941954cddf1c594bb5b5541e2ff83d0bc4f9e5920562dd7b5878df4c047`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 73.2 KB (73178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c345a342845558490ce483e520c8b0e86f8c0568d2045f37fb46451dfb85c98f`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723736a3894778a49a1e825327450020780a315ce6e741e7f122c84628697b62`  
		Last Modified: Tue, 09 Dec 2025 21:14:26 GMT  
		Size: 43.7 MB (43695073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61eca5aefe9cc76a9eb96e6a8990dd9fd8a4559cd1197fc7f52acace7c6f3558`  
		Last Modified: Tue, 09 Dec 2025 21:14:21 GMT  
		Size: 104.4 KB (104442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
