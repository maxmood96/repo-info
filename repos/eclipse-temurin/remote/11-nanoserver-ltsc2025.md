## `eclipse-temurin:11-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a61b02021ad0fe60b6e578c74fb637c195a7329adce683ae15cc26e880446f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:11-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:2908c11866f8e587e0f1e8b4f2ec3daf936d0ff1d2c0e2d8a6c381ee085eab6d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401055879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2506bb66a4fac0d391bc23efb3a6266fb7021a1d3d96da66e16e9d24fb41e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:04 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 19:17:06 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Mar 2025 19:17:06 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:09 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:16 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 12 Mar 2025 19:17:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:17:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d153dfbd73dbd7445361ee4abd0c925b3782b941f2cb10da810deae12f18f`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bae8217fc4e3f853c1d8e924733ec62171a6351c553cdd9ef1c40902c481638`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5bad9e1dad86eed81cb376a494a6adb3986943ef027566aec156c1f249dc43`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73346353498cabcbc9aa5cdc24f14a05bbcd114a2f7e035ee001eb515310770`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb841fc19f548316554c038c90da823b0289452e18d69322a93a44f89351dfb`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 76.2 KB (76156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5eef1acf6ac6b58b44ce0092be89738768ea5ca4f18939a5d57af7037e0b9`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098108396781f50b453dc7320c678473cdcd355a8526a655d1a0398671d1b0ed`  
		Last Modified: Wed, 12 Mar 2025 19:17:48 GMT  
		Size: 194.6 MB (194556941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea2850a8379c200c7c2ed1c174013a31a2cf3fb0dffa2c82fb9d7b46ae3c969`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 114.2 KB (114227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc21f030bc45b02fced89861dfabb43561de952018859b1ddb778dd713b9559`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
