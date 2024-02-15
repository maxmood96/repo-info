## `eclipse-temurin:8u402-b06-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:35eedb8faaf82df250e33fb3e07feffe0fd093173f3c8c8a8f1998dd2a5144c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:8u402-b06-jre-nanoserver` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:f1bd0a79baaf4ac96c8f8246e8944dcbdfecb8dd5c0d08b7dedaf5bb878f10d6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161003482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa5ea54fa6a24b4f1d756bbb9f6f52bda4a4d8d5eb6131b7eec25923ee90132`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:21:03 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:21:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 14 Feb 2024 20:21:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 14 Feb 2024 20:21:05 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:21:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:21:19 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:22:02 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 14 Feb 2024 20:22:15 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a8b9610542d9f544621b5b605f3c73832b279a3681d70286c37473fec95b2`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320c7f4aec5883a29011e6e9f92ddb22af540f7c4ffea76399db2f2e482da79a`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b236d5717e24cb1456735c67ed3334020e2dfb2d9b085f9908382d2b644f523`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab249bb6a4cb870af2fcc419628a502aa14f8335ad1e8c860421de5ac822d80`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d029d4a51c18b6e328ce712709d3a800ffd3838d1405bb11039e7b50db11a`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 80.4 KB (80434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de18572ccdee2cf25d4ca67517fc6a7d6cd78cfdd2f34fde0b0ed0a959d57c0`  
		Last Modified: Thu, 15 Feb 2024 00:16:28 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d5e3c01d077264be4c19645c07e0b7000bbacb8473ad21f03ea69d11beddea`  
		Last Modified: Thu, 15 Feb 2024 00:16:57 GMT  
		Size: 40.1 MB (40121159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623fed8c371bd218f97b0dc935860d655ef9adad1f74234b0667d2703d6a179d`  
		Last Modified: Thu, 15 Feb 2024 00:16:51 GMT  
		Size: 61.0 KB (61003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u402-b06-jre-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:d4a250be85569267c7ba577a0a96a10ded6a574a38d7f438f996afabb26ae18a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144904335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df38f7a8a5aa8ef9587a0662cbdb43e8fefdd8f1814132fc42d96a0862ad7f88`
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
# Wed, 14 Feb 2024 19:46:58 GMT
COPY dir:db8ed4bc6cf3fc1a9a530d737bd8bcda792821f4f1e3e610cedaee77629ebb36 in C:\openjdk-8 
# Wed, 14 Feb 2024 19:47:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:037059051756e2c8806b4cf7e23fe7271cd088f10fad53bac3e9756693bc0191`  
		Last Modified: Thu, 15 Feb 2024 00:08:04 GMT  
		Size: 40.1 MB (40113552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68680b92e59989435cdb8dac3951554318e0dca63b0106df94cc1309c4a7713`  
		Last Modified: Thu, 15 Feb 2024 00:07:58 GMT  
		Size: 87.5 KB (87482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
