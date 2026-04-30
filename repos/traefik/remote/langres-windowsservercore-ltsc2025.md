## `traefik:langres-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:48f18d38f8c9a7389e0658bf9036b617bedfd0e8d0a98bcfac64ca5911cb87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `traefik:langres-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull traefik@sha256:bd314478d17013f8e4487ac0b5a17f5636269e4c18d8ee808ab9690ff763bfea
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179603509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cbed699639a6d9c1f096e7edad87ddc5513d8c3c5c7b386a8d7368a7fc0b78`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Wed, 29 Apr 2026 22:46:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Apr 2026 23:18:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.3/traefik_v3.7.0-rc.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 29 Apr 2026 23:18:56 GMT
EXPOSE 80
# Wed, 29 Apr 2026 23:18:56 GMT
ENTRYPOINT ["/traefik"]
# Wed, 29 Apr 2026 23:18:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a14b1ab823928f463b4116f5097425013fadfeafe8e1197e48a6fc31d0b442f`  
		Last Modified: Wed, 29 Apr 2026 22:48:31 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476260932a3c7f84d4dda454a50d4fb41185cb413247bdc1cf00cdb46e366c1f`  
		Last Modified: Wed, 29 Apr 2026 23:19:08 GMT  
		Size: 49.6 MB (49612245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f72b0d175ce5d98a165c00ca1ce39e83c674b3c7220a7bdb3a724805d91fddd`  
		Last Modified: Wed, 29 Apr 2026 23:19:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea79f2657d2bc798e256d5c6913dd16b1402ba9e795f4921e3e27539096a0313`  
		Last Modified: Wed, 29 Apr 2026 23:19:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef51a549713b9e93e202f7ad880677e2b977636920fe9b63d2b57662b3c2899`  
		Last Modified: Wed, 29 Apr 2026 23:19:01 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
