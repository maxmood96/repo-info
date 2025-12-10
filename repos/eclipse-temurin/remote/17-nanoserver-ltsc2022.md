## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:cdc6669c593a6ca911c55427eb78f46c431c025fa0ac95b227b398eca4fbf323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull eclipse-temurin@sha256:375eafa2e02e31a9491b5d517e7662808c29751ff89187d6b55b0e5c0556efce
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314070388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b34df60b1fb9da8d9c8b842a3b97879c552083945b7ae9fd920aa8a2a40928c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:12:58 GMT
SHELL [cmd /s /c]
# Tue, 09 Dec 2025 21:12:58 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 09 Dec 2025 21:12:59 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Dec 2025 21:12:59 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:13:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Dec 2025 21:13:01 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:13:08 GMT
COPY dir:2018c1c9eb6dc671bed9b2018ab32e648d405ad10a017a184613d399d49818ed in C:\openjdk-17 
# Tue, 09 Dec 2025 21:13:13 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Dec 2025 21:13:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6081bd6804178009789fc41fc7b5b028534888b64e10cd0ca092b3f3c75127c3`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b7fdd2b791f338238da4b276ca4940b2299ab4527f7f75f5a490633541c898`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73358df318e7799470cc73b06da29fe0887a82582d6f307abcb79556daa1dc25`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee69fcb07bd76ece3d3e752a3618abfd202e309bfc86686fd584b57e3716ce5`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ed029240da3a6c65445259ab3b49d7cfd3cbc4a93640b0f35f0bba0584fda`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 76.6 KB (76592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad819d103429df1ab3f3fe8bf7b0a4f2df07416fd191affb0cb74fbf44fdae4`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0f60f444d406ae990002c5b1c286ec5ab7255e5c1cbd745e0c1a337dc1244c`  
		Last Modified: Tue, 09 Dec 2025 21:13:50 GMT  
		Size: 187.5 MB (187511015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb7646e0baa7104bcd94b3832ee561daf131ae1b02a366b5af6eef888fed789`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 118.1 KB (118070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ee39ed10d35941b33b676875246c0f8d62b9fea31c66190adbfedb048221ae`  
		Last Modified: Tue, 09 Dec 2025 21:13:37 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
