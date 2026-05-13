## `eclipse-temurin:21-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:4b66de186071fbdce8a14843fce39af654bf70dab502197615c65b8b9f9dc6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:21-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:2f0b3a7db0839b2d9c915e55436b055fe051bd9989994ac0d0cf0b7364d845e5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401799718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f461aeed653e2463d2abb3aa48451189219f9162730db9770d8bac42e6544ab`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:29:19 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:29:20 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 13 May 2026 00:29:20 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 May 2026 00:29:21 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:29:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:29:24 GMT
USER ContainerUser
# Wed, 13 May 2026 00:29:35 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Wed, 13 May 2026 00:29:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 May 2026 00:29:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035ec944d63267a8e4aa5146a939b10f7a9d491c5a3495bfa8c55ce5767b0f4`  
		Last Modified: Wed, 13 May 2026 00:29:47 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd5dd9173397197d6504dbd9b90d30570fe6f9ced841ba8fdcfcdc57131f29b`  
		Last Modified: Wed, 13 May 2026 00:29:47 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01850fd519469e9c93610ebeae645ad6c7f01a109de4ddfd921b8af3e82bf279`  
		Last Modified: Wed, 13 May 2026 00:29:46 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127c1f52dc33ea63e5d5bae0d22839e0479c869d1245a3aa1f6e043fc6abf727`  
		Last Modified: Wed, 13 May 2026 00:29:46 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e2bd196a4c79243b8f32caa003ad67755243b1aa7c7811c8703a929a043740`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 75.8 KB (75845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb683ad1a0e16d506447c1ca1f07ffb9615509bb51ea3a05032d1183b5b05dd`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a937f3089b19344664f2c870edfc59a179181449b8d3f6464d4189b331ab2f0`  
		Last Modified: Wed, 13 May 2026 00:30:00 GMT  
		Size: 201.9 MB (201875807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05de6d05129f18ebebc7f77fed544a9fe6ed178f91a0a9bf23d8f43ca515c5ac`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 102.6 KB (102636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18baf1047a73887ce529bdb2d37257f31726857e232581abc93761eae4e7d9cf`  
		Last Modified: Wed, 13 May 2026 00:29:45 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
