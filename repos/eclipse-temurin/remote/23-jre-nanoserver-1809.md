## `eclipse-temurin:23-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:4ff0e253bd074e905335fa92b01fc73920d51ffcad5dadf18f5c01b08aaee1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:2beca7113d9383fe5269c7ae5433d176fcab2a4c09bfd85c5c676f9aa6249249
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208586683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcfc33e71ba1902c7abe5930f440403d10994ac1de16e0269d3328298a8b5482`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:02:52 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:02:53 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 15 Jan 2025 18:02:54 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 Jan 2025 18:02:54 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:02:57 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:03:01 GMT
COPY dir:d9adc234ed2c06cd6b72c0beb8933c6d824941dbd1cece41e4fd2578b0632fbd in C:\openjdk-23 
# Wed, 15 Jan 2025 18:03:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271099d9fc07361c7ee5424ed4e3f2633a57c2df934ab6fad8cb38265ef51da8`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec35dd57f9568791e0c284bfa64bb0239d30cca05ea2e72eaa23e15fa764dca`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e453b87d5a5bab86ec00fe10f07bf2af16126c030eb6b0e3175419e5838d1a`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7478aa215fca8d7511b9849e4a2731577c996e04512db378a03b1b7a98adbb49`  
		Last Modified: Wed, 15 Jan 2025 18:03:07 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4b66c6a7d831a892ae694426580be6471a11950c53c7eb6a8c870d17ae7c41`  
		Last Modified: Wed, 15 Jan 2025 18:03:07 GMT  
		Size: 84.2 KB (84200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbadebb5746a6a35bae9b4083461167077970795aac9751db498586cf92c14c`  
		Last Modified: Wed, 15 Jan 2025 18:03:07 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958c0b70ec0d9156d2fe4643a70db9ab31e62efed40387c7fcb2be3e2ec725f6`  
		Last Modified: Wed, 15 Jan 2025 18:03:13 GMT  
		Size: 49.6 MB (49609157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b995af88185f62a09c4c3fc83df7d548156dfd3fc38eb5a1577ce85dff15a4`  
		Last Modified: Wed, 15 Jan 2025 18:03:08 GMT  
		Size: 3.6 MB (3620532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
