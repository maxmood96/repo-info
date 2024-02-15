## `eclipse-temurin:8u402-b06-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:a9497f6d9f8e42ac501e8aa5acb6e308ec0cbe817062ebfe3c5b484a99c3712e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:8u402-b06-jdk-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:7116b52c44f82695b001ca2f3ce0e9c130f00527712b819e33d5b3f7990bd26e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206498937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ab3537f5db144ba71f37a4fcf5ab90a77ecd6a1b8dfcb5d76e935af15d0243`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:41:52 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 19:41:53 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 14 Feb 2024 19:41:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Feb 2024 19:41:54 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 19:42:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 19:42:06 GMT
USER ContainerUser
# Wed, 14 Feb 2024 19:42:17 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 14 Feb 2024 19:42:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddfc54d18bb5861232283d3ff2ca5e214ade28a46dfcf6c1e7c7243809e5e85`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50de6bbc468ce67f5c06aec96ce768f0701699d3e2e0b0f624f2414d51118ab7`  
		Last Modified: Thu, 15 Feb 2024 00:06:59 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4981285aad162eb35c182a94596307747ddb88a060134c126e380584659b091a`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcbefbe80e1c3c4fe2a0ce3b1475bc3f49b412b16db693ec97a04d8e952ad4f`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d995837ef866fa986b862cf38eba7d9b6919e0841be54a8c8507bcc20429eda3`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 75.9 KB (75858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b0ab688df4f030d11a95f25383a65f0b25a81897dfcecfe28ebdf93224e21b`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680cc5e91a9451783c3a9929194b11f0556803228d30b8cfe3815c5decd0b55a`  
		Last Modified: Thu, 15 Feb 2024 00:07:08 GMT  
		Size: 101.7 MB (101701527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e281a5a246ff148c8a7103f3053bc1f4e0543010ff3fb2cc80beafe289ebe196`  
		Last Modified: Thu, 15 Feb 2024 00:06:56 GMT  
		Size: 94.1 KB (94109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
