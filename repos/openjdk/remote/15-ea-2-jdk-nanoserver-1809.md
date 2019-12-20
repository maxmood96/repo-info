## `openjdk:15-ea-2-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f975b2688ef9a7ef8b514ca4d32cdfe40e5bb7ebec0db883fa4154021a7c8366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.914; amd64

### `openjdk:15-ea-2-jdk-nanoserver-1809` - windows version 10.0.17763.914; amd64

```console
$ docker pull openjdk@sha256:7a5bc5f5c1a3137983c2b8e517e5154e5137ee6b10e428fbe3bde3ba09afeefe
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298519540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6855db4aff1f5a6d0e322a1878f042717d36420b7787506010790744e757c606`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 28 Nov 2019 13:16:41 GMT
RUN Apply image 1809-amd64
# Wed, 11 Dec 2019 18:49:48 GMT
SHELL [cmd /s /c]
# Thu, 19 Dec 2019 01:29:02 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 19 Dec 2019 01:29:03 GMT
USER ContainerAdministrator
# Thu, 19 Dec 2019 01:29:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Thu, 19 Dec 2019 01:29:16 GMT
USER ContainerUser
# Thu, 19 Dec 2019 23:28:45 GMT
ENV JAVA_VERSION=15-ea+2
# Thu, 19 Dec 2019 23:29:47 GMT
COPY dir:6d5fd3921fd73e114531174facad140d243e0a2fdaf89f9cdd00c060291c7582 in C:\openjdk-15 
# Thu, 19 Dec 2019 23:30:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 19 Dec 2019 23:30:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1951f408509ba9ddcf240ef5d838c72c5596f97a05b063446508f2ba15d510f2`  
		Size: 101.1 MB (101106116 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:163d55b77f49371136083ba8066ddbec4afad6e1f4fbba77fa4ffebc99a8098a`  
		Last Modified: Wed, 11 Dec 2019 20:01:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63bb05b94288d5ea0447e7c6b75a854704f420c56d3b13acab4d9b2e03cc3f4`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 914.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64927380268ba75b4d8445c6eebea564ad1af3f6ffcd0ab9856b348138b44532`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca8bce76a22921ecaa2f6065834a3d494b61f569022c5b64bf0c9fa9c5bc63c`  
		Last Modified: Thu, 19 Dec 2019 01:38:08 GMT  
		Size: 71.4 KB (71377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b95fb661adc21f04050381ea3e21b42927fa5df24d3b78a394b6e71e7992c12`  
		Last Modified: Thu, 19 Dec 2019 01:38:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8afbee53ed21155f7ded3baf732317a184dd6b04a744cf62ea0119a91dadc5`  
		Last Modified: Thu, 19 Dec 2019 23:46:19 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1da52bfab9118d3020de558d36b53e61dc81836ee7d967bac76b9144cbe8f9c`  
		Last Modified: Thu, 19 Dec 2019 23:46:41 GMT  
		Size: 193.9 MB (193892701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4796cd07f29f024c52f7b1f9f7978392df2f8331d29cc2e52473f8d72183704`  
		Last Modified: Thu, 19 Dec 2019 23:46:20 GMT  
		Size: 3.4 MB (3443743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb184173e120753fe3becfcb0932b2cdea3fad7eeb2bd740dfba532be1d7771a`  
		Last Modified: Thu, 19 Dec 2019 23:46:19 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
