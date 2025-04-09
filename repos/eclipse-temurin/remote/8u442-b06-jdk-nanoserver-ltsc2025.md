## `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ad64a1be0f645e3bddb6df5ce8b34a5f6be7b240ec32698ecb6d8ebeb5d03614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:fafbc38e6689e5edb6df3f2bb443b54d967d78e2008b4c4f6376888503fe0605
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292746098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b797dd15b560b4ccc98736d246d01a5a1b2e837e83ab7dca7b3994364a14c7d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:46 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:47 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:17:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:17:50 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:55 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:03 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:18:12 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fc009319f48c85cb127de3610b7a59f9b45f9d8512290eef0e8cec1525a0f3`  
		Last Modified: Wed, 09 Apr 2025 01:18:16 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdfdf016b75ab466d2219b5ab7d022b17dd5246979f93b8b050202b7af0a032`  
		Last Modified: Wed, 09 Apr 2025 01:18:16 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be9bcd4d09eb2acedf5ef13a2b7dae962d2bc56ddfa1d2ccac47bcf884edc82`  
		Last Modified: Wed, 09 Apr 2025 01:18:16 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12cc880161c0b61e1a3bfdf6aa052b959155ce28a3c01d8cb803859563710dd`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc4b8040355ed6a1d9c3bbd169252ba241d58f9cbacebf3565ec2baf995b3b7`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 78.8 KB (78816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d25234e63b9661c60d019da6c2c0279f7dd0263679f78f880fd4d520149a471`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45197970a707ae43a4e27d088c8b3f3fa7d6a4cbc914f20a3a212d7f8045a4c7`  
		Last Modified: Wed, 09 Apr 2025 01:18:22 GMT  
		Size: 102.4 MB (102434201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d79cd86a2dc89700968337a2fdb8d74a5fe2636cecc0614cdd982c1f477aa0f`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 114.6 KB (114586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
