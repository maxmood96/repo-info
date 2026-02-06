## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:558fb3994f22e9f6b48b38869d354a56ec7ccdd65bc5a6a0e79c6ecb9a54459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:5256df677257cd4074d78c9af786f924b48ca42481f1b51d331dd568ecb49f79
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.0 MB (401010483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e4de3a3275bfac4430f532099b203335e663f2cb96591c42b937401eb38ea0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:40:01 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:40:02 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:40:02 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 05 Feb 2026 22:40:03 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:40:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:40:09 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:37 GMT
COPY dir:a00a0ee8f4ae82aa8e2b5d2b9cb5c2941887de3e7b021ae64d7924c257e6915c in C:\openjdk-21 
# Thu, 05 Feb 2026 22:40:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 05 Feb 2026 22:40:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb0bcf60bd949a1b49cc50fbba16be62f32d655c18bfea6e123aed02b16dbe`  
		Last Modified: Thu, 05 Feb 2026 22:40:49 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308a9230f3a2a69304969d4bc5687419ac3503ae3568b01a6a0f2ed6141aa9c6`  
		Last Modified: Thu, 05 Feb 2026 22:40:49 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d366b10ae243f72a1405c4ff85b8accc81b2fbb3d2836af77d3b62fcb8ca72ea`  
		Last Modified: Thu, 05 Feb 2026 22:40:49 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1e12beb448f5e8471de7decc4edf98fa602f96bd8ecc4836a1886fd68a8705`  
		Last Modified: Thu, 05 Feb 2026 22:40:49 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc55bd6fbc68b22e5d83801d8524178ca6f83a3eb1369cff37f3d9685debff3c`  
		Last Modified: Thu, 05 Feb 2026 22:40:47 GMT  
		Size: 71.8 KB (71753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed2dcaaac30b91b52497cd89b07add6990b3fd0db52bf5126b2ca634cf20cf`  
		Last Modified: Thu, 05 Feb 2026 22:40:47 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc753fe5ed7b1465deaa61e70c09188bc8d37d7e6d809be031848227462f4b`  
		Last Modified: Thu, 05 Feb 2026 22:41:01 GMT  
		Size: 201.8 MB (201752544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dacdc8fc409db5b454b876579fcf3bb6419db3a0f3744ddeffc06045e9d12d8`  
		Last Modified: Thu, 05 Feb 2026 22:40:47 GMT  
		Size: 103.1 KB (103100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88230a9bf2462e53fbe0d4bf03d9872361aa1982a2aeb13cac796daa0de11d8f`  
		Last Modified: Thu, 05 Feb 2026 22:40:47 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
