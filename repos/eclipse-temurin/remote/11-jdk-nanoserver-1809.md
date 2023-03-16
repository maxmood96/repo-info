## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e415143c7f7c8b21cb8c351a68eade9c5fbc387a632e6cbe9ca878a1ac745370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:0ea75863de7823c288418a6ee61ab2f84c584354b8ab731db880280fc5846b1c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299761483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b81b3c7392b6166712c56541846f9eb6774911eadbfba9b7c2043f9eea4bf0b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 00:58:15 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 00:58:16 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 16 Mar 2023 00:58:17 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 00:58:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 00:58:29 GMT
USER ContainerUser
# Thu, 16 Mar 2023 00:58:45 GMT
COPY dir:3631bd3b4ae70db635b51d6f7ad3f3254aa758db5b0d079379d506c898ecba14 in C:\openjdk-11 
# Thu, 16 Mar 2023 00:59:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 00:59:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4489e5e9e00e2088cf3904d72bfb246bc5175bae482a80d8d565a2f186c4891`  
		Last Modified: Thu, 16 Mar 2023 01:46:02 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5633a59a03648a04e485134a919ee482f5b58b087127f720192f136b0d02cde8`  
		Last Modified: Thu, 16 Mar 2023 01:46:02 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcaca59b821b969afe3c0b7d6b30ea23fc1ee85f15f692696c78c98e1fa2573`  
		Last Modified: Thu, 16 Mar 2023 01:46:02 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3acea1d02cfafafd3f0cfad4254518f54dae3fc9af2ae19c89f60883bcacb6`  
		Last Modified: Thu, 16 Mar 2023 01:46:00 GMT  
		Size: 70.3 KB (70259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3420e98ef0887397043d9d94ab02746cfa0a49d5f0baf8389af04600e23e62`  
		Last Modified: Thu, 16 Mar 2023 01:46:00 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9af4cc433b0dd9a051aa2e37254bc83e3067d1342e6e2c201d89fd90b334fb2`  
		Last Modified: Thu, 16 Mar 2023 01:46:23 GMT  
		Size: 192.9 MB (192904526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b5b5f5d766cf4cd9e10b24ae954043f6c69cd34678335d58c8484da7a4bf61`  
		Last Modified: Thu, 16 Mar 2023 01:46:00 GMT  
		Size: 95.5 KB (95532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da116b1c0d23aeb6b079cc3bdc5c65da2fad12505b11e052df365048864eb90f`  
		Last Modified: Thu, 16 Mar 2023 01:46:00 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
