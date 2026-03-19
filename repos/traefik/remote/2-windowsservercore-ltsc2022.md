## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d8cf5a508af5d035ac243e148979696c5471c459dcbec121c9e8aad6ebe01716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:b03226b4baf75ef09652b8fe411a320108b338e8e9d2e361f08fe940cd47645b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030574600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fddf159a4a905b9708d44a95b158259fd3fda7c1e0981ce75a1fc7b53aea1cc`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Thu, 19 Mar 2026 19:14:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2026 19:35:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.41/traefik_v2.11.41_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2026 19:35:07 GMT
EXPOSE 80
# Thu, 19 Mar 2026 19:35:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2026 19:35:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.41 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfca1b3eee0ad2020b43322ec6aa430b31bcefff963532774db87b930057f5c`  
		Last Modified: Thu, 19 Mar 2026 19:16:37 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbefa4ca21abbe2387165afd79fd354ef3a270722a11aa7e22396e2d08ad289`  
		Last Modified: Thu, 19 Mar 2026 19:35:57 GMT  
		Size: 48.3 MB (48287965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edca91cdd343c8c5a978a0a89c1872094266b8cd78d479cab3a384c6f861141`  
		Last Modified: Thu, 19 Mar 2026 19:35:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef538a2297e94865c7982add9f71c6c508ae8b7d718da0a08a2d9146f5f1cf6`  
		Last Modified: Thu, 19 Mar 2026 19:35:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7323889a642341e4d52a36628a4903a74a030b14b77bbe6d039b4124472d989`  
		Last Modified: Thu, 19 Mar 2026 19:35:13 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
