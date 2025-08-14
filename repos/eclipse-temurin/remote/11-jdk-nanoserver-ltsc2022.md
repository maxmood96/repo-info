## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:997a9f9c8a23f03c562e4bcc426567010d01dd917110eff0c2bf405e4f2ff79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:373023e0c42e5b8099ca86ba07913c2f629ec10f34be818c94fe1f290e7bc5bc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317482369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5208c50df134a02028e1349678ebbf47e0d3c325373636db8274d1393bdb9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:50:36 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:50:37 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:50:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 12 Aug 2025 20:50:39 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:44 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:52 GMT
COPY dir:8b5aa3450b5ed8de1b2c81f4388b1a437f54688a5e8c6d990bf0f6727b917a6b in C:\openjdk-11 
# Tue, 12 Aug 2025 20:50:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 12 Aug 2025 20:50:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74c81e4e9f8fb70d2c94bb1a2a222984c71b6444f1cceeffa739cb2f8fe7ea`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952ecb4fbb04f8ebe06614ac6bbe684e122c5322a98e48b49cec394f67979c74`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb5a3da1cdd83972318d32ab4c749dd519437c2125859e292aac2f987bee95e`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f791afe4c7ff0892b329a82c7988c7fbf22a72c408610a6634b37340cfa55fe4`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feed461223af0c64276e424c3cae76bb5ef12b6c06c86a19d22f7a5d54ff9327`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 79.3 KB (79297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb84cc67daae841c6a563d21c6fda7cc64d1c4e6a2b22f40943c958c28656af`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a371e0d0642100b256e461588bb5fe718df396320a7e5f119021a65d0460ed5`  
		Last Modified: Tue, 12 Aug 2025 21:14:04 GMT  
		Size: 194.6 MB (194618531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af600e9a17e6778b1cb30b6831fdb317abcb3f608726f5c8b25aa86b1599dc4e`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 118.0 KB (118031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a78bc4979b646e175febf3586f29d6a37386a5c7dddcd71067965bf99cc1ef3`  
		Last Modified: Tue, 12 Aug 2025 20:51:57 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
