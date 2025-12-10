## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:7f67e5b98b4b9dafc6182b43f7ceb70facdcad9561d1f00d6cf50fdca388671b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull golang@sha256:3a9f8b914044e82c08e5be3e650e6ae648fc004151b6d0c62d90fe56b2999a49
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260947263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487dfb4a21ab27f7887482259aac304cb6566289a780e8783eda162044bb6e50`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 09 Dec 2025 21:16:31 GMT
SHELL [cmd /S /C]
# Tue, 09 Dec 2025 21:16:31 GMT
ENV GOPATH=C:\go
# Tue, 09 Dec 2025 21:16:32 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:16:34 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 09 Dec 2025 21:16:34 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:16:35 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 21:17:46 GMT
COPY dir:88c362617e5a6c2a31b1694bcf871ea0c6e4eea9f08403024fec2c23b6b3826c in C:\Program Files\Go 
# Tue, 09 Dec 2025 21:17:48 GMT
RUN go version
# Tue, 09 Dec 2025 21:17:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4452878655f0a55c9a73f005b6414f027aa73dfba935a176f2a2383c8366c429`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3165d6044d5955f8a48942927d08dfaaa345f6b7681b38083bd90a8de9aa2001`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f079ec09fc2b45b2697b0b64682064ebea8b285395195d186d1dc5f2f64299`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5efd34f0cc2b5e40c6418c3e4859172260d02e669fca0fab72d80b832ff531a`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 73.2 KB (73178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d52a8172a9f208894b074325c0a87e84377e69b40fa218a89d8fd59639d850`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4168a0d9284657200f78372fbaa1b79330e9ee0f55e514f314ddd70cf4daec`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e091b2e15c4594ca491475d151a01a50737f99272678281a65848cf4ca54a0d4`  
		Last Modified: Tue, 09 Dec 2025 21:18:28 GMT  
		Size: 61.9 MB (61907464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444bef91fb85600901d719f3a005e2789300f499d4ca7e9d0a5e0c1d712e4d52`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 86.0 KB (86019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720100dbe2a8af37c16deeeb32ed07d91fac78afd3ecb82260aad8b94d7a3074`  
		Last Modified: Tue, 09 Dec 2025 21:18:22 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull golang@sha256:1874d95fe6d2f3b843ef2fa59e471e804e0a143bb4f0533a0b81cec98143831c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188432363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403068fd3ac9102d53db69af036c8cc8be95c5f485aeda329fc0f1adeee6d21b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:14:10 GMT
SHELL [cmd /S /C]
# Tue, 09 Dec 2025 21:14:11 GMT
ENV GOPATH=C:\go
# Tue, 09 Dec 2025 21:14:11 GMT
USER ContainerAdministrator
# Tue, 09 Dec 2025 21:14:13 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 09 Dec 2025 21:14:13 GMT
USER ContainerUser
# Tue, 09 Dec 2025 21:14:14 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 09 Dec 2025 21:15:19 GMT
COPY dir:88c362617e5a6c2a31b1694bcf871ea0c6e4eea9f08403024fec2c23b6b3826c in C:\Program Files\Go 
# Tue, 09 Dec 2025 21:15:22 GMT
RUN go version
# Tue, 09 Dec 2025 21:15:23 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e0c2ac78b642af3fe027ab353902810c7663da67c683cb16ca6e33b571f6d7`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2994e05f1878eff9ef0011599f3780d07d91571ed35c7afba42820b4936c85d4`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c074b9dd404d8522224906db9aae0f65300f3bb5ef3387e1c78e537b3d9f3225`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b93c1132545a8c556c3b53cbf837012e91e83d2435c3f73eb25cbf0d12d6fb`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 77.5 KB (77471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f6941d8bd0ad819e8f71c7fe17d07d5c1882abd3d98b48d67644038e9021e2`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd386243ca8bb32c588e8e14d328a9b0817de9d3f8acc1fcab0fe3b8109006e`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b08af668ae97b9a544d1aca1df3c460835af1a83049462178b518b7c7a89cca`  
		Last Modified: Tue, 09 Dec 2025 21:15:50 GMT  
		Size: 61.9 MB (61903931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9c6364557550b5134c555448cbc94e71c5ed2df318d2c48c5cdf16937b59e7`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 86.1 KB (86082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a277f9796187248d920acaec81321c0efc9a3a7f689df714357d84130b9c979b`  
		Last Modified: Tue, 09 Dec 2025 21:15:45 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
