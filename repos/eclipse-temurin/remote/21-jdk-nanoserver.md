## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:34f0b60c33cbf0aeb4d32f230c97cc3ebdf54dce25d99fda3bb30a00286f29a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

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

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:01508ce7f086389f3b1929118e4991fddf68a44bb55cf91c34dbe52a52936ae3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328642523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad4b59ebcff959607d0abf5908a535d6f5b4dc726f18e3a63eaa8d359ce392`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:38 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:39 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:39:39 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 05 Feb 2026 22:39:40 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:45 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:32 GMT
COPY dir:a00a0ee8f4ae82aa8e2b5d2b9cb5c2941887de3e7b021ae64d7924c257e6915c in C:\openjdk-21 
# Thu, 05 Feb 2026 22:40:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 05 Feb 2026 22:40:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbe19ee94e573abb779f2402326286006e4c963d1c55e9884ddd75ff7a93c5d`  
		Last Modified: Thu, 05 Feb 2026 22:40:46 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05150381a323a88db5ee5aaeae375155d5b8a311e15ed91ec2c24eafc75b394`  
		Last Modified: Thu, 05 Feb 2026 22:40:46 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30c92b1386e0013f2b59e5b32735e2033201da13737c62d9659889afc7ea495`  
		Last Modified: Thu, 05 Feb 2026 22:40:46 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb52357ce624196fe96e2e5b4824b57aac2f42e1c4fc83f7fb7eb3236e8c86b4`  
		Last Modified: Thu, 05 Feb 2026 22:40:46 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b3f2c32b47561935e8f5c086461973a6c3403cbabbe2f36fbe47cfe206fac1`  
		Last Modified: Thu, 05 Feb 2026 22:40:45 GMT  
		Size: 70.7 KB (70708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46045dbb74fb463ec88be1e32b2d68f21156acc6d16fd22e9dfbd8306066a20`  
		Last Modified: Thu, 05 Feb 2026 22:40:44 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c12531fb70f963fc4e2e08a6559fcd1a71edac9f4c693cbac6c36529fc73a`  
		Last Modified: Thu, 05 Feb 2026 22:40:58 GMT  
		Size: 201.8 MB (201752669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ec7d3482f1153d77c167b2ca9f58f5e1dd9491b9ad959cee509ae93b270337`  
		Last Modified: Thu, 05 Feb 2026 22:40:45 GMT  
		Size: 115.9 KB (115900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36efc64c0af25b1f4cc3111009900d4a87f07aa75e82c2ce270d7dd658701bbf`  
		Last Modified: Thu, 05 Feb 2026 22:40:44 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
