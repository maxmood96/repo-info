## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a288e61d066ff235c21c33170e74807f51d7dc4f561a6e43874ecc47d01a7411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

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
