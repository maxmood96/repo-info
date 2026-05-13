## `eclipse-temurin:8u492-b09-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:af8a2199bddbb121425ede49a5e69008bc80019f991fcab0412239c454f094d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:8u492-b09-jre-nanoserver` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:1ef29f3902703ef81497dd38b39b70b3c9dc653a0b450c81bc7135450d5e6b43
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239886035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7931cb791fe9b92f49c7b1dfefcf0464605e6e85a86dfe7b4b5becc3318398dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:28:44 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:28:44 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Wed, 13 May 2026 00:28:45 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 May 2026 00:28:45 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:28:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:28:51 GMT
USER ContainerUser
# Wed, 13 May 2026 00:28:56 GMT
COPY dir:deea9cd49fa78c2b910137007aed467626dd46389507789da1635093de3df40f in C:\openjdk-8 
# Wed, 13 May 2026 00:28:59 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b5d573ecd2cc5dbfd049cf26ba2043a753921d32d2ec7b82741d8e4730dec`  
		Last Modified: Wed, 13 May 2026 00:29:05 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d86173f24d34a74db32980b6b9d39743452ea3ff17c9d0e25dc649d4a52b61a`  
		Last Modified: Wed, 13 May 2026 00:29:05 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15655cc2e1bdaeb11c0628e7bd14dc05678a5a7e56dbcf695a6caf665c627455`  
		Last Modified: Wed, 13 May 2026 00:29:05 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09093736270ff77a2107e5248b7c212706dff639f08f90e8af889b25220a073a`  
		Last Modified: Wed, 13 May 2026 00:29:03 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e767e4c0bea40e22577050a3cd3d7fd5140fe0caf200ebc9a102eec74f54f1ed`  
		Last Modified: Wed, 13 May 2026 00:29:03 GMT  
		Size: 70.5 KB (70467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f484823c160b55b92090de4673105f10ff576e8fb624f5e955290066d123b6`  
		Last Modified: Wed, 13 May 2026 00:29:03 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162d6cc8b305a0cdd3b2252af2c4958605f2027ac86af409a62bcfe554b2b1b7`  
		Last Modified: Wed, 13 May 2026 00:29:07 GMT  
		Size: 40.0 MB (39988201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22a3c5576993c88afa087f24e818b0b3c0c7ab5837d721b8d2a5265163d9ec`  
		Last Modified: Wed, 13 May 2026 00:29:03 GMT  
		Size: 83.0 KB (83034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u492-b09-jre-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:c0fd1194ccc47b4de0926a6e284ecafdac02aa7023a30c8956a2ce0cf7d8a149
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167209134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65088753802241f9db89326ca7a901e87075d13802bb700453323c0f1f24f0c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:23:32 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:23:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Wed, 13 May 2026 00:23:32 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 May 2026 00:23:33 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:23:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:23:34 GMT
USER ContainerUser
# Wed, 13 May 2026 00:23:37 GMT
COPY dir:deea9cd49fa78c2b910137007aed467626dd46389507789da1635093de3df40f in C:\openjdk-8 
# Wed, 13 May 2026 00:23:40 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03cbcd303d3a3d248ab22d617e183ed76d01abedfee5c52cc9fb7f6a87170f0`  
		Last Modified: Wed, 13 May 2026 00:23:46 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4020417b724f038256992f00d0653eb817c5c2ff378c86fa3fe4be98f6f1fe91`  
		Last Modified: Wed, 13 May 2026 00:23:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c372e048e07ebfd58d41d756111d1aca474cd806c8c2c03b12d84fd752a3be`  
		Last Modified: Wed, 13 May 2026 00:23:45 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2afd2ac20279088abcaaa5fd1abc6ea2ccc40ad1b39a398ea3aa17b3ab09ff5`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b02e47ca82f4366df01b94f395b1e69820f1237d0d044c7178eacf2cb94936`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 76.7 KB (76688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e7e09994fa92b3e25c93f8e88e7168fbb9672755ea1ceb67cfb91bcfa5fc07`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9bab70c8817dfb95dc76e820df1c7e443299cef44facaec09dc95685cde65`  
		Last Modified: Wed, 13 May 2026 00:23:48 GMT  
		Size: 40.0 MB (39988105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfad307f0b72b79f8517124f044fe2492fb8e47eb6a0756ed4a0df015606dd7`  
		Last Modified: Wed, 13 May 2026 00:23:44 GMT  
		Size: 100.2 KB (100240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
