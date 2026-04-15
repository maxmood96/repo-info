## `eclipse-temurin:8u482-b08-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:97e1e105ee589db79e27985285a51dff19403d31ac0bdf86aa665b886b05cf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:8u482-b08-jdk-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:aaf342f36262592fe6288629be35060c9514c151975ff30c757e6e55d06c666a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301812141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5050a95c38f3037c07c4ae7e07be6205f1095f78d635733953369ec9f7da969b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:13:23 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:13:24 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 22:13:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2026 22:13:25 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:13:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:13:32 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:13:59 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Tue, 14 Apr 2026 22:14:06 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f75102dbc967c514401912472229865fc8a42a71e920f5c7f8949885906cdcf`  
		Last Modified: Tue, 14 Apr 2026 22:14:12 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fc454b272b7499e304ac8d8781f2de90382c68cd2f5e8f20835129922bf50f`  
		Last Modified: Tue, 14 Apr 2026 22:14:12 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17430063c00c464419ca12e17754dddb0fcf21c989b0e448b70b766235c88f8a`  
		Last Modified: Tue, 14 Apr 2026 22:14:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125a1a8e1322d914ca1ff17143df3c59f8aef5007437dd2c53decc91267c616f`  
		Last Modified: Tue, 14 Apr 2026 22:14:10 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ec6117fcf1213c648e66a2fb5795317b64c9958d0e99712e43a5fce6efefd9`  
		Last Modified: Tue, 14 Apr 2026 22:14:10 GMT  
		Size: 76.9 KB (76858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb677437c33c6d292682705b873e0cf8040f303d1ef5f3b28d74d0fdad72e66`  
		Last Modified: Tue, 14 Apr 2026 22:14:10 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d66a9e4af480174834569b478f2c74b582721453c9a561d1803e7d8f8b8dec3`  
		Last Modified: Tue, 14 Apr 2026 22:14:18 GMT  
		Size: 101.9 MB (101908769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bbf46a868cecf16464541174277a642bae3855f6491effe53f4279ae48e080`  
		Last Modified: Tue, 14 Apr 2026 22:14:10 GMT  
		Size: 104.1 KB (104069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u482-b08-jdk-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:9dba135f3a62878818348b749c18e9627f36de27cd4d2c227a94f4c917d0c5f9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229057069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae59d826e2f75fe479b6a14732b6f1212f8fda857783c678acac164db7f22ab`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:10:58 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:10:58 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 22:10:59 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2026 22:10:59 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:11:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:11:02 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:11:07 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Tue, 14 Apr 2026 22:11:10 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca91647e48c8f734915ba8e1d5f9edea1563ca4c872069115650f0dfe102a26`  
		Last Modified: Tue, 14 Apr 2026 22:11:16 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faa9a641d6a0bf2181d70274985ceb9e4be0a87d6442ee204bb2ca43f1cff69`  
		Last Modified: Tue, 14 Apr 2026 22:11:16 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f09f7948e258baeb12889f60833e3d81c9ec8176a004fad823e00e06e5103b0`  
		Last Modified: Tue, 14 Apr 2026 22:11:16 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d76ec6fb1aec54ceb4b921af8bc6bef7fc1910eeadad1da43f69396936c51a3`  
		Last Modified: Tue, 14 Apr 2026 22:11:14 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d386e0d2bd12c54b7464e6a51dba6d1513d4effced934a377f90b50c3fd4009f`  
		Last Modified: Tue, 14 Apr 2026 22:11:14 GMT  
		Size: 88.1 KB (88145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7b916dd5817be457729b338cc71da4a97cb21952fe7f5983b4d78514157f8b`  
		Last Modified: Tue, 14 Apr 2026 22:11:14 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4efa63f4c782c20ee386df6ec7463391bec54cf080be9cec33c3f5909bd5ec1`  
		Last Modified: Tue, 14 Apr 2026 22:11:22 GMT  
		Size: 101.9 MB (101908415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d407c8661a71bb01e3379a24e1e44ceeb0c151a4d79c7eecb6008270f357ca6`  
		Last Modified: Tue, 14 Apr 2026 22:11:14 GMT  
		Size: 99.2 KB (99203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
