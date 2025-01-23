## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:66394f3ed7e0039147b8a94f163885b22deb05e095f9780493987857b4e531a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:c36212abd185c3e85811b93dff09e9d2e9b4da05ce9095c6d20020bc0322d692
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240293073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53773286b069a26d7a617970297b9784f6ba7f623eb17f811a74858a664a813e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:18 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:18 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 19:34:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 22 Jan 2025 19:34:19 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:22 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:34:24 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Wed, 22 Jan 2025 19:34:27 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2800bbfdd74fb337f34757e25867402876293c2e974757cfa673ea1fe5f6ea`  
		Last Modified: Wed, 22 Jan 2025 19:34:31 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7348d714fbcf9c97c113ce7014a2c87816501cb1b919f52db831046749ddb2ca`  
		Last Modified: Wed, 22 Jan 2025 19:34:31 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb380d63d698a7b18be16ac945e3eedb1a344b9f9f478de9daf9b380625fe33`  
		Last Modified: Wed, 22 Jan 2025 19:34:31 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9394e0c8d553a22749862fb83f2dca3a9a9fb9fcb8a95a30ca1fb4fa3f5d428`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a70d930018d636903a48d07d479589c26c94737bd5302a532b5a8f6d24f2d37`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 76.3 KB (76270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ba1fcd41b7411bca59f5e70d7c5a2e18945a32d7a5ed004c550b435a765b6b`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a8650fc7c0ed92c581289f87f8c2705d534b6e44e632f48eab8d8b38d7306b`  
		Last Modified: Wed, 22 Jan 2025 19:34:33 GMT  
		Size: 41.1 MB (41061457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6582b7d3264f41f49af1fe5c16de85fffe0aa6147d2d0331cbddab9b13bc8c6`  
		Last Modified: Wed, 22 Jan 2025 19:34:30 GMT  
		Size: 95.8 KB (95788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.3091; amd64

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

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.6775; amd64

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
