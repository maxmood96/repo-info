## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0b25cdaae45e98f0e40c08f09b873b25eee15404eb8971b10e480d734a408959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:d489e9adad5d2c120f3057dd155df3405244179d4e81cf4d739fae95e26f2d1a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296641975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a629d9fbe4ebd15d9e1be673bab8c3202bb432366f3b0209bb1e37b97725e1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:13:25 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:13:25 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 14 Oct 2025 21:13:26 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Oct 2025 21:13:26 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:33 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:44 GMT
COPY dir:184da149c84a7d26eb59eea9818ea043a400cd17024f2fafd00950f1891aab87 in C:\openjdk-8 
# Tue, 14 Oct 2025 21:13:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc124661de915548586b5dab37d8e8e2bd84c95235e4b4ee6b7ba8d3f3fceff2`  
		Last Modified: Tue, 14 Oct 2025 21:14:41 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6a77592b34bb8d346e10a507b1866bfba95578ca2df253dabec1d482a166e2`  
		Last Modified: Tue, 14 Oct 2025 21:14:41 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7c69bad1bf2fd70bee6c3f9263ccd1d7c05a27aaada168c159b6c24d819f91`  
		Last Modified: Tue, 14 Oct 2025 21:14:41 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1e582cfdc9d325f081f93665d30a3a0d2b5c3dbb39e41a64dfb772d0f210b8`  
		Last Modified: Tue, 14 Oct 2025 21:14:41 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7e80b3f6fe7ff8924178146e9c54091fe35e78f764d12880f68b09ae5ae4fc`  
		Last Modified: Tue, 14 Oct 2025 21:14:41 GMT  
		Size: 71.2 KB (71207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4faf4f65681437beaec4cd9786eb4fda3d9222822dd8cabcdabb2db4aa586c9a`  
		Last Modified: Tue, 14 Oct 2025 21:14:41 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583227e7fc0859e7058999ccb2be92898a6e7b16783219661618f333ac7a1822`  
		Last Modified: Tue, 14 Oct 2025 21:14:50 GMT  
		Size: 102.4 MB (102434711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7537158486f069bf9237911101a2512d41cfbfd5dc0e958d354a3bb3c2670529`  
		Last Modified: Tue, 14 Oct 2025 21:14:41 GMT  
		Size: 104.0 KB (104002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
