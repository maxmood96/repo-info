## `eclipse-temurin:8u432-b06-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8fab5ff3efc8376a64d0acd756299cb9fbb6763a545c47c8c84a11b0b9373cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:2a4896672798d9e22f6b98344f58de17957ecdabac36ccf355e7f177ff3f7293
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161906156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47140edf5656a8b674d6481b8a0de424c9468defb2fb4cea3c35d08a7f79087d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 17:59:01 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 17:59:02 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 15 Jan 2025 17:59:03 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jan 2025 17:59:03 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 17:59:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 17:59:06 GMT
USER ContainerUser
# Wed, 15 Jan 2025 17:59:09 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Wed, 15 Jan 2025 17:59:12 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2dcc68c8190c6c730edc7183b99c15898530242f3496b572704fae973be86f`  
		Last Modified: Wed, 15 Jan 2025 17:59:18 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9807304574b3e98edbe104e1bcfba356488059003af87d71d270f05fa978448e`  
		Last Modified: Wed, 15 Jan 2025 17:59:18 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6655ca1afe5cd4f3072affa191fb22830512f4dd97be10e7ca6ee1ea58dcd9bd`  
		Last Modified: Wed, 15 Jan 2025 17:59:18 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e160c97803b0bef0d82818a147a60872f68c2e2b069c17ea604deca72405be`  
		Last Modified: Wed, 15 Jan 2025 17:59:16 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fbb7d63bc031394bee52eeace3461c478655581f47788691f14f1c79dcf7f2`  
		Last Modified: Wed, 15 Jan 2025 17:59:16 GMT  
		Size: 77.3 KB (77330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfbdc343821ec945b64577962ddad9e16344cd125f5ff683f371c963ced044e`  
		Last Modified: Wed, 15 Jan 2025 17:59:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a88b3a6be3a17238385695d56f000a19532e54646bf8c4aa95595b663c04d83`  
		Last Modified: Wed, 15 Jan 2025 17:59:20 GMT  
		Size: 41.1 MB (41061168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ddfdf87742669fb733effe910b1e4ef78b95842bf3d448825bed891159efc`  
		Last Modified: Wed, 15 Jan 2025 17:59:16 GMT  
		Size: 101.0 KB (100958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u432-b06-jre-nanoserver` - windows version 10.0.17763.6775; amd64

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
