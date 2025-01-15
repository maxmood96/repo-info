## `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e902684a0ffc7c9f8c1a86fa3a90fd185ae5f6258e980a8a3b6d95ba30e8c378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

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
