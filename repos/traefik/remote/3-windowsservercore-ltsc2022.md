## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:604c6c8ac8c4782f26c3e823b8013f0c81ddfc8595d2ea31cad0e09877ce1755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull traefik@sha256:74dfe41e06004b04bf5706b7d03dc59d242646d9f8fdd93fe117cb8b066537ba
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2119847749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc8059256ae9ab0d71e70521e631d884220341c74b2595126b5e8c7186802e5`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:08:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.13/traefik_v3.6.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 14 Apr 2026 21:09:00 GMT
EXPOSE 80
# Tue, 14 Apr 2026 21:09:01 GMT
ENTRYPOINT ["/traefik"]
# Tue, 14 Apr 2026 21:09:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616e36967dd130f4fa6e3aa26638accd4a1f4597db6ce1319d77811d453a647`  
		Last Modified: Tue, 14 Apr 2026 21:09:12 GMT  
		Size: 49.6 MB (49631259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed8eb6c6a263d7faab7ff1b839a3397226eed94305c81bf47f7de6fda017402`  
		Last Modified: Tue, 14 Apr 2026 21:09:05 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a9d267798fd967561ca288a442123434aa9a2515a7302f1479b9d67cb4218e`  
		Last Modified: Tue, 14 Apr 2026 21:09:05 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a656835c09aee1c18c85b98ef8863063302f91eb505e08beff9696e7b7484892`  
		Last Modified: Tue, 14 Apr 2026 21:09:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
