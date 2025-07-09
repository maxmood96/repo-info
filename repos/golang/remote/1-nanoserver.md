## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:c84b561fe34b83431f37f2d7c41b70e450c6641a928618070edee3307e34eb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.4652; amd64

```console
$ docker pull golang@sha256:d12d2ffaa3bf7438be591c9dbb98601d052f3d5f6bd609ace59e20512fd57ba4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275228347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b61a0a66de43e90aa6573c0a1dcaf6b2748e3c650b87f24322fe165de056298`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:15:05 GMT
SHELL [cmd /S /C]
# Wed, 09 Jul 2025 19:15:06 GMT
ENV GOPATH=C:\go
# Wed, 09 Jul 2025 19:15:07 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:15:11 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Jul 2025 19:15:11 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:15:12 GMT
ENV GOLANG_VERSION=1.24.5
# Wed, 09 Jul 2025 19:16:24 GMT
COPY dir:a64a2923c1fcf6909ec85d25bc3e35bfa4572d72cc3eb98bcec274153f9f9413 in C:\Program Files\Go 
# Wed, 09 Jul 2025 19:16:28 GMT
RUN go version
# Wed, 09 Jul 2025 19:16:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eabfa2732d430f09c2bfe3261b3b0cceecea60ee05da7e4334e4f545c62cc1`  
		Last Modified: Wed, 09 Jul 2025 19:17:04 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94eb53960569c39065d105b8043439c8636265b4a8f704a4908b1361a7fbcba`  
		Last Modified: Wed, 09 Jul 2025 19:17:04 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef907dead145b379d32433c3b76f2207d8ba3631bd0ab9267c9b1283201931`  
		Last Modified: Wed, 09 Jul 2025 19:17:04 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389e3bf0e22772726e82a2eb0324effd1b9784165cd7fd246d947491ef8a95f9`  
		Last Modified: Wed, 09 Jul 2025 19:17:04 GMT  
		Size: 76.1 KB (76121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee162dd8244400c71b3f7f9643b7aad8904330bc98a4d4c7717828609044da84`  
		Last Modified: Wed, 09 Jul 2025 19:17:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f770ee3d1f069f76ede26143e59dd0f7de5880461c3d97d6d895f3e085c974`  
		Last Modified: Wed, 09 Jul 2025 19:17:04 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a356eee45499469b5643f266b836696f49cc79230695f8c3261e0559e1eda4f`  
		Last Modified: Wed, 09 Jul 2025 19:17:15 GMT  
		Size: 81.9 MB (81918548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de62ca801e68909f554274e3d7b3d104e7e4126211e2d59ee9408f0679a69c75`  
		Last Modified: Wed, 09 Jul 2025 19:17:05 GMT  
		Size: 76.7 KB (76728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b72b6ccc91465074221d8c31e3b50b40ce3a07c215140b3da1f7d0955c112f6`  
		Last Modified: Wed, 09 Jul 2025 19:17:05 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.20348.3932; amd64

```console
$ docker pull golang@sha256:3ebf8ae5fde6184408bf29db0c09edef0c339589b96e4548b7e69a57f45e5110
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204684793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d3051a3357f930e021f2b7d8e6071890488aefa40e0c914e9c27672fb045f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:13:09 GMT
SHELL [cmd /S /C]
# Wed, 09 Jul 2025 19:13:10 GMT
ENV GOPATH=C:\go
# Wed, 09 Jul 2025 19:13:11 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:13:13 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Jul 2025 19:13:14 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:13:15 GMT
ENV GOLANG_VERSION=1.24.5
# Wed, 09 Jul 2025 19:14:46 GMT
COPY dir:a64a2923c1fcf6909ec85d25bc3e35bfa4572d72cc3eb98bcec274153f9f9413 in C:\Program Files\Go 
# Wed, 09 Jul 2025 19:14:49 GMT
RUN go version
# Wed, 09 Jul 2025 19:14:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96137e166ff8a1c9505b9eeaf700ceb643772065bc53ea097ed4028da42d92e`  
		Last Modified: Wed, 09 Jul 2025 19:15:25 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3367c414b51257018ad7bbe658ceb967b56ef34483c3d494143e4ac39f7b86a5`  
		Last Modified: Wed, 09 Jul 2025 19:15:26 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d4783e16791d882e03653ba8d3c04b0338ad694f224c112af1f1e34d6df2fc`  
		Last Modified: Wed, 09 Jul 2025 19:15:26 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fde4d8fd5d823f99875962352cabcf239eec8c00c87c8fbb71e7742504fa977`  
		Last Modified: Wed, 09 Jul 2025 19:15:26 GMT  
		Size: 77.3 KB (77264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155d7cf6a41c040942f42ce9e30dea0e9ab66570cb7a44409e379e928a3da35c`  
		Last Modified: Wed, 09 Jul 2025 19:15:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ceb2dad53151bce38934112a7a2cf88a00fb3d89ee6e67f5fdbcb6dff8f10d`  
		Last Modified: Wed, 09 Jul 2025 19:15:26 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5694eb72d3c54f1261192b338a5f9a342842167b5c6187856d4800c98e8250a9`  
		Last Modified: Wed, 09 Jul 2025 19:15:35 GMT  
		Size: 81.9 MB (81888605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92638dca758fc5e55f067634f7416bc5fb01c1f1e7864d80c8c8057cd966c5f4`  
		Last Modified: Wed, 09 Jul 2025 19:15:27 GMT  
		Size: 81.6 KB (81606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c840fa9ed5688ee551b1e4bf20ed3669a65014e6130cffcbe62e94020d1d7a16`  
		Last Modified: Wed, 09 Jul 2025 19:15:27 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
