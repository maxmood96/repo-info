## `eclipse-temurin:8-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:5c31db00751506cc0c1eeeeceba37aa9b692b1adcbf7bde2e5ee89eb8ba26128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:2cb86955f95174c219423a458873ddd9e4f3a492f3f65036d0b488f82e4b016e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258681605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246e038e67488ddef1dc864d1fcf4b2f9049c1f8a07641f2eda86ad57468adfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:52:33 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:34 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 24 Oct 2024 01:52:34 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 24 Oct 2024 01:52:35 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:52:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:52:45 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:52:50 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Thu, 24 Oct 2024 01:52:55 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25246ba89bb6930b57810825092cd580d4efc83a7a2361f14b61cec4e189c73`  
		Last Modified: Thu, 24 Oct 2024 01:53:00 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d104fc45c5c71c6fb8edc27894076c6422ec621c1f900004262c23407b760d`  
		Last Modified: Thu, 24 Oct 2024 01:53:00 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182df4e2380a7a5f4dab7919ee6270ac7c54afafba1c74db1b4f4f28704a5cb0`  
		Last Modified: Thu, 24 Oct 2024 01:53:00 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577b1cb294fab36faeb9cba9a557340e4b0277690a33f679006ead20258c18e6`  
		Last Modified: Thu, 24 Oct 2024 01:52:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3afc7b3ae934f9075a344d148db662b310f33174b22c9ce52eb28d1927d6fb`  
		Last Modified: Thu, 24 Oct 2024 01:52:59 GMT  
		Size: 66.4 KB (66363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87be22e52bbaaab22de919b83769d92e55856b9c5f8efaf6dd2eb4684d557719`  
		Last Modified: Thu, 24 Oct 2024 01:52:58 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a98ac6435c57e4c7271fc258ca10924dda22fe163179b1492e7019b1901c02`  
		Last Modified: Thu, 24 Oct 2024 01:53:05 GMT  
		Size: 103.4 MB (103441501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9c79a5baf395a31ac2070eb5dc97011692ab5d13e1d36cad66d39a0262f5c5`  
		Last Modified: Thu, 24 Oct 2024 01:52:59 GMT  
		Size: 74.9 KB (74873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
