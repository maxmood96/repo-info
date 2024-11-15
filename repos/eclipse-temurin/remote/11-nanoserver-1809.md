## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:343d382209f155382663855f01d8b3512d2afee4f5070ba560845dc86582bf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:d0e20cd301363104cdae58d16755de6575868ba7d6e51153e90cb68262da4d14
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351091077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fa3acada110ec5229a6ecee01086822c0d975927ed748c8c44ae32db79a7e1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:16:13 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:16:14 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 14 Nov 2024 21:16:15 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 14 Nov 2024 21:16:16 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:16:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:16:19 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:16:26 GMT
COPY dir:92a047b71eec51fdc82b01f518237bef64c78b39e065fcc3e9561b3909a60868 in C:\openjdk-11 
# Thu, 14 Nov 2024 21:16:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 14 Nov 2024 21:16:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d807740b142d04bff218560410fd8fd9452d06ce7b80b23607c6da2718f082`  
		Last Modified: Thu, 14 Nov 2024 21:16:38 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6763c49a35ad0636518efb9b8d155fcc8218d345e72a1b4f1eb7f05d673469`  
		Last Modified: Thu, 14 Nov 2024 21:16:38 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6155363b41e9d324c7e004200e54d09bca69b7137cf441724659c20e3947a005`  
		Last Modified: Thu, 14 Nov 2024 21:16:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fc2b55bb4732f89fbe0b87d7c7a8dcb084a4496d98c01f5e6d4824adbbf828`  
		Last Modified: Thu, 14 Nov 2024 21:16:38 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7ca3de67bae9f79cad249d781a721cd1966a23b55857ccd4e8bf3216af6cfe`  
		Last Modified: Thu, 14 Nov 2024 21:16:36 GMT  
		Size: 75.2 KB (75210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4b5c3de6704dfe1bfe285074204982b60f81cc986531c3068da153b21302ef`  
		Last Modified: Thu, 14 Nov 2024 21:16:36 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff3a90ecfccc35ade4550f766694ca1bfd66f0e40fccedecd427df3f9df5ee`  
		Last Modified: Thu, 14 Nov 2024 21:16:46 GMT  
		Size: 195.7 MB (195673014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea58aaa15b9c776560906bb1792d41765663833f2952b508e6ea0c330a2664d`  
		Last Modified: Thu, 14 Nov 2024 21:16:36 GMT  
		Size: 122.1 KB (122075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f048059b7dffdfe31528e0eccf895a1514e42312b5636a83a1b1c7dfe1838a`  
		Last Modified: Thu, 14 Nov 2024 21:16:36 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
