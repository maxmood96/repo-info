## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:e8e64a08760982c452850c1f77dc2bdc117271e2b408aa754c0b0c421dd119b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:0e9e4a9a5a1dd2f6f756ca873275c287f83cdd9fede15f33af144f086d40f5c2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377578276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dccc0de7967d0a5ecb3bd8493b1c01734987ade56f43ded80326288a0b6a95`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:04 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:06 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 18 Apr 2025 04:14:07 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 18 Apr 2025 04:14:08 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:14:12 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:14:20 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 18 Apr 2025 04:14:27 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:14:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32d382d416f9ec3df2407aae0e3ff4ad39a3418bf6e737b85fb223177183dc7`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52f2eaba454a8595e6a40d57364b6bda57a1e25cbb0d71bcc4402ea7c47fad`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4a4dc7b84fea4b7f3ad66854cf22e4e8d068c8c20238231aea3cad7acc8be`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9f7ffba209e4310fe43277bbd1d2aa9604573d4348a7ca100c73ee4dd53902`  
		Last Modified: Fri, 18 Apr 2025 04:14:34 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c0dd667e9d63f46b8e4af6810ad2617a613782d0ffc91ae19aa78678378625`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 79.8 KB (79766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb95e8e268f36f8c2e95019e0cedffcafe81a863f5819ed97588e555abfac760`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4633b01a84745feb93227552b648df2c2ed4fcac92caea647fcd789af4d218af`  
		Last Modified: Fri, 18 Apr 2025 04:14:42 GMT  
		Size: 187.2 MB (187235525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b3b3b3c57c7aaa376423d16efe07eb7684b881748a624c65275c4084b391ab`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 114.7 KB (114656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced9c36fbdd3b9d9d6a3e3e568ff99dc8281b9c9f84945da8955a2fa7342c72`  
		Last Modified: Fri, 18 Apr 2025 04:14:32 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:33a14b9b9988d0095f52c44a9b995e57ee048004af06d527a746d4b63d1fc258
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.0 MB (309970077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb4a9760b384e9b7ac6d23997129cb183aa4aa86a0364135c6ffae920192f32`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:17:04 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:05 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 18 Apr 2025 04:17:06 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 18 Apr 2025 04:17:06 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:09 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:15 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 18 Apr 2025 04:17:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:17:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5f3cbc8df69a817dfb5dfc49519793572893c77e8dba5b76385d34c98d5b6e`  
		Last Modified: Fri, 18 Apr 2025 04:17:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45e06f0fc1616020b6caa43073fa2c06bc137bb8fbc289dbc718ee60cb9c786`  
		Last Modified: Fri, 18 Apr 2025 04:17:25 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02beb0536ade790ae2731538db6fa6bf535c7be8411840b4581ac181950941e2`  
		Last Modified: Fri, 18 Apr 2025 04:17:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304140e790068decb12561d6f1225e66ecb613a29d913b50f6abde02007bd91d`  
		Last Modified: Fri, 18 Apr 2025 04:17:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86ebc4fff43f972db01b652bbd34a67061ad31f7cccb2058e62d7f1cd05911e`  
		Last Modified: Fri, 18 Apr 2025 04:17:24 GMT  
		Size: 77.0 KB (76970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08551b3b806cfe817dc94a22ffd5c7b95c8979538c969850468409166e7016f4`  
		Last Modified: Fri, 18 Apr 2025 04:17:24 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd8798b8ea60921c5cc4df2425e4db4ba206e352098d923b4ae19cec0a53dba`  
		Last Modified: Fri, 18 Apr 2025 04:17:34 GMT  
		Size: 187.2 MB (187232987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8efe31742065b56c165c0c1a0bc67085ccb8946fdcfd2e939cedf4df28885a4`  
		Last Modified: Fri, 18 Apr 2025 04:17:24 GMT  
		Size: 114.9 KB (114857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a093d26c96aa1851677355e22ca97bbd783ee9e5919b06c5894536bc1a0a0800`  
		Last Modified: Fri, 18 Apr 2025 04:17:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:43f79138754db0c89d5e87ecfe1883b5189ed7f1926d3902f1de0cc69ca416c5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25984012b4bf08536b30bc6a20771f5958bf7355b74e3ee607550c7eec91a1e3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:27 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:29 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Fri, 18 Apr 2025 04:17:29 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 18 Apr 2025 04:17:30 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:32 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:39 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Fri, 18 Apr 2025 04:17:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:17:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ca03bf2dff56b8b5c470ba5cb4fcc68a8fb61b2421ef22d88f1e3f4db21b9`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272abc8933c8436464985b09581cf5c31265b77e51ac88850c15a82027c3ab02`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bf44a423b36f4f4ed885426b21bc963131854a13cc5ccd783076ebc9e9f6f4`  
		Last Modified: Fri, 18 Apr 2025 04:17:48 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f09be68bf98e6dc2a27b600b8f2b8550678b37a9aa4e7e93e0866e0e4eb23f2`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fe6354d11266e423f74acc53f6f475c345debf35191ce773af725af7964eeb`  
		Last Modified: Fri, 18 Apr 2025 04:17:46 GMT  
		Size: 68.9 KB (68937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18137ef8e108148a037acc8dc3b3748abc9b339284c982def8022cc8b97f046d`  
		Last Modified: Fri, 18 Apr 2025 04:17:46 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e8f461cca167b5b0b83e0900807510af08f84a808cf5ca56f0c1ecbfe90ff3`  
		Last Modified: Fri, 18 Apr 2025 04:17:58 GMT  
		Size: 187.2 MB (187233682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3d83b2cd54ce2823ff5149894bcb73b579cdfacaee049db5105e1d9c15138f`  
		Last Modified: Fri, 18 Apr 2025 04:17:47 GMT  
		Size: 3.6 MB (3623683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a77370dac691a801f260ec1a5a527a903afc221327ac4c84fba137c24174de`  
		Last Modified: Fri, 18 Apr 2025 04:17:46 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
