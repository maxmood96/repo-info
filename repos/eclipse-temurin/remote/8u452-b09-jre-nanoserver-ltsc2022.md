## `eclipse-temurin:8u452-b09-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:564e11c35de45fdc7cedf3ca1b328ce4d9c68cb1455b5746f4b3ab1c1cd780e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:8u452-b09-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:9b0dffdb19bd751d51d87119ac5251bf9cc4c756f9505d33651e45fb5cf7e533
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163273523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fae7af5c3584540cdbe57f7972d9b05691b1d949f13c6194f301d1eb13cb54`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:12:49 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:12:50 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Tue, 10 Jun 2025 22:12:51 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Jun 2025 22:12:52 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:12:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:12:56 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:12:59 GMT
COPY dir:88632ffe03bdff97c0f2931283e9e8742ceaeaec8904ee54b87f8b4347f84ae7 in C:\openjdk-8 
# Tue, 10 Jun 2025 22:13:03 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f85e6b79fb65cee18292553318c63d604abe0339c73efe73eb6ea487d3fd9f`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e93d200952c01b63e15da6669e3af841dc1c5faf762c8cfeb9c5d94473e8013`  
		Last Modified: Tue, 10 Jun 2025 22:13:34 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fa12ccdeef41adda1dbf9ee952b96f601fa91c7f632d3cd87150ecade5eea8`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb0bbbebe9dcf237d903466ce5a4bf5e85f53e0c4b8e226cf30da33b2d13bff`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7e53ab8b13c0ef004ce505ac9b8d800516670d9c1a589f9db51d94f845207`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 76.3 KB (76332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe782cd0fa9a2219a5dadbfd7a3a867d0b7821dae9abdc0c8ebb8d745081780`  
		Last Modified: Tue, 10 Jun 2025 22:13:35 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d793aeab7ee806a38c6dac21e70a166b2f7fe9e8a3f2893aba1b59ea6a50003`  
		Last Modified: Tue, 10 Jun 2025 22:13:38 GMT  
		Size: 40.6 MB (40552782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4303b2a44a2a8ab8348f10138b78057ad49bbe4e2bcaac9b3ef1bc01d676d55`  
		Last Modified: Tue, 10 Jun 2025 22:13:36 GMT  
		Size: 98.7 KB (98663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
