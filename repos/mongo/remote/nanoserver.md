## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:6293735a8239773cc2f09c0cd7be59b5ac37d73f7645e96c6ec5fd1ddac83a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `mongo:nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull mongo@sha256:7a0a1063a8e6b8ce36f69eb63fc6288cef6c60eb5f5ebafc7fa57778f0ed3d68
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **943.2 MB (943158898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1373bf7198c0bf705d8d0fd2735c5c70517c4f85d067fdcb50a8ff12415e0e7a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 17 Mar 2026 19:21:01 GMT
SHELL [cmd /S /C]
# Tue, 17 Mar 2026 19:21:02 GMT
USER ContainerAdministrator
# Tue, 17 Mar 2026 19:21:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 17 Mar 2026 19:21:15 GMT
USER ContainerUser
# Tue, 17 Mar 2026 19:21:17 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 17 Mar 2026 19:21:18 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 17 Mar 2026 19:21:57 GMT
COPY dir:2e9a39fee71c6e6ac0bdd0c42186fca338afe838728732f7c8d0e31874ce47f3 in C:\mongodb 
# Tue, 17 Mar 2026 19:22:24 GMT
RUN mongod --version
# Tue, 17 Mar 2026 19:22:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 17 Mar 2026 19:22:25 GMT
EXPOSE 27017
# Tue, 17 Mar 2026 19:22:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7639cfc8369ca7028fceba72589d8476cadc7f4369eecc6dd5d7c699da6e7e`  
		Last Modified: Tue, 17 Mar 2026 19:22:33 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717aa3f29beff0ba2a404d2c7357e7c645235adabd1a056fca627bb5b612d5f3`  
		Last Modified: Tue, 17 Mar 2026 19:22:33 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cb50646c283817db1ed2217d8d1f4a6166e94d60952f7c6b66a632d7ca9746`  
		Last Modified: Tue, 17 Mar 2026 19:22:31 GMT  
		Size: 77.6 KB (77587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8477a8e5955ca5b369d08e149d25ea0ae55fb9a8be2f84af6411a4c9f0bbae30`  
		Last Modified: Tue, 17 Mar 2026 19:22:31 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecd1cfdd5a0c202ea87a5adeafba7decdc1aa4a85847d1ed76190acc98e80a7`  
		Last Modified: Tue, 17 Mar 2026 19:22:31 GMT  
		Size: 275.2 KB (275184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11558c699946e7ab60400f67de7cddd38630b2110fc596936965a26ad41ac058`  
		Last Modified: Tue, 17 Mar 2026 19:22:31 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c8e0ac294efd2436dbf8531fc203a4a822c795aef944a816e57c2f85a3a0d2`  
		Last Modified: Tue, 17 Mar 2026 19:23:46 GMT  
		Size: 816.1 MB (816061094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf24f0ac8f75b7d1d43e0ac1e978fe8771c6082b7c13cb36ef088eae6d87dc8`  
		Last Modified: Tue, 17 Mar 2026 19:22:30 GMT  
		Size: 87.1 KB (87081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1852bcfe00fc9d30a2de2b4702b9cfb953a1f3bc0726428145b3fde1c0c29d35`  
		Last Modified: Tue, 17 Mar 2026 19:22:30 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6785885f9c7d99d6318e3a956c59ece25f582cbea0dd5cca6f34cdee180c5fce`  
		Last Modified: Tue, 17 Mar 2026 19:22:30 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de843d49f128c513d1615bd5713cf44eaa4d2a5e215c087392742fc20020ec1`  
		Last Modified: Tue, 17 Mar 2026 19:22:30 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
