## `openjdk:14-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:17024476ed1c555a6d9d41416fd711321e48649a88d1e6e80ba84d582c61aa6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:14-ea-jdk-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:f123f68b58fcc0fcb8ec1600d476eb9144fe4e53b1fa6362ce4cb1a02d0009aa
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298510533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e5b71196fb7b0c1efd9f329241fe4a809a9372a5ea92c841e330002b72afec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2020 00:05:42 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jan 2020 00:05:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 00:05:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jan 2020 00:05:57 GMT
USER ContainerUser
# Fri, 31 Jan 2020 18:00:34 GMT
ENV JAVA_VERSION=14-ea+34
# Fri, 31 Jan 2020 18:01:33 GMT
COPY dir:ae790bb2cddd4da21a50247b1b2f9d27b80c58ca31c76918ac7f1bed89c73d22 in C:\openjdk-14 
# Fri, 31 Jan 2020 18:01:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 31 Jan 2020 18:01:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f3a5df9926db070e4016e42e49a7d9ce0131f528e644ae4388774831b6b46e`  
		Last Modified: Wed, 15 Jan 2020 01:58:21 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c21d67a14cad5558f706984eed7f97aaa2665e4b4cf1a7a1d21888c5e2c02a2`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ffd38236cfc5913ab84e035b74a0bddf197bbfffdd8e9e8b151cc30bbf8adb`  
		Last Modified: Wed, 15 Jan 2020 01:58:20 GMT  
		Size: 66.5 KB (66486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8510d836b27dbac14cee7131c4209ebf2081c2ba957f75e05cbeff605e5320`  
		Last Modified: Wed, 15 Jan 2020 01:58:18 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cda5c51efd3aafcb58a7f92a2932fee11ccf8b3f8c90c9f1814f8bc737f96a`  
		Last Modified: Fri, 31 Jan 2020 18:13:40 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72b1921d9b618cb56ab77ab554fa1dc5cf89f6689f31d3b2cb31c8bce00d36c`  
		Last Modified: Fri, 31 Jan 2020 18:14:19 GMT  
		Size: 193.9 MB (193937550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67732616165146f22201563672573dab1c74e2f8adfe70aa559293c3e6ba3d1`  
		Last Modified: Fri, 31 Jan 2020 18:13:41 GMT  
		Size: 3.4 MB (3446571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e187536536e2331e14ceafc514735534ddd0c932c63b246d11ad88ca05de76d7`  
		Last Modified: Fri, 31 Jan 2020 18:13:41 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
