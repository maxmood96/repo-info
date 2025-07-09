## `golang:1-nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:8e9b335ee49fa2e2705c28d506d56c1705dd1257a2e0cf735382eb8b252347c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `golang:1-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

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
