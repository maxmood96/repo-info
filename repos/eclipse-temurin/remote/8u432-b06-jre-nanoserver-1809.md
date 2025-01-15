## `eclipse-temurin:8u432-b06-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:370bdeea106954ebdfc19a457f455e07c01a51c4571b25bd0fdc52bef20dc2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:82dc188d959209d104b7c78066d59264ab949809ed6916f2df8c4c61040355ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196519221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de1c4ce9bd47e7b2997dd10f95e1ef5916c72bcd0f39194069edd1975692de6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 17:58:41 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 17:58:42 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 15 Jan 2025 17:58:43 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jan 2025 17:58:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:58:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 17:58:46 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:58:48 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Wed, 15 Jan 2025 17:58:51 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d7ac732d9af88f4f82aeb855ba97f0cc297052598bc329c5c87c2fff3fa005`  
		Last Modified: Wed, 15 Jan 2025 17:58:55 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a0bb08d2952620f4ca5acea4cefb1adae71ef495f6fc31cfecfc212a6f6d62`  
		Last Modified: Wed, 15 Jan 2025 17:58:55 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38b3a414471d97b8181e56d43a4ef47697eed70c00abec4819ec6e9023b3ad9`  
		Last Modified: Wed, 15 Jan 2025 17:58:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d94c00b1f342c4f6b6874c6b13a2085e3a56fbc69fedae1f46e05fc0eed40c6`  
		Last Modified: Wed, 15 Jan 2025 17:58:53 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c85bf2eeae8a5156c7d36227dc69183ea44185f43656aa168391eae184dc96`  
		Last Modified: Wed, 15 Jan 2025 17:58:54 GMT  
		Size: 75.7 KB (75697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2714f600010a08dac7be5a89f68bca82ecf979b8aa1b31a04a92a9438e1a3e65`  
		Last Modified: Wed, 15 Jan 2025 17:58:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c7e35a885976b2290fc20fa6d0e78262063fd6c7282be853657227bcb47681`  
		Last Modified: Wed, 15 Jan 2025 17:58:57 GMT  
		Size: 41.1 MB (41061272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017113251d8c4e47c3b130c88290bba5e82a4104bb517eafbddf0217f3076228`  
		Last Modified: Wed, 15 Jan 2025 17:58:54 GMT  
		Size: 109.5 KB (109482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
