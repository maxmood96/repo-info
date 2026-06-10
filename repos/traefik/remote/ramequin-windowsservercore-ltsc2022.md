## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:fd5eaebf0256341047bc8a9d4d8d6c5a9d8f966410a358e33937ab2b945a5736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull traefik@sha256:63ad21f6ed7a57518dec12f3c7baa2cb69de2d952451b9de4eed0d0e8aae1743
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2182191602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da234a001603ab1e85725ab64f00978eb7699a1d4cb3313cba5e977a160ef95`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Wed, 10 Jun 2026 18:07:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2026 18:10:17 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.21/traefik_v3.6.21_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Jun 2026 18:10:18 GMT
EXPOSE 80
# Wed, 10 Jun 2026 18:10:19 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Jun 2026 18:10:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.21 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cae37f6f139af2b515cab8d238ddde93a6e6ecf3744bb76788394f75f470373`  
		Last Modified: Wed, 10 Jun 2026 18:10:25 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3371c7c0c996fd6831ccc5dcf2bb455e08ebf735967541a66f5959f6708c28`  
		Last Modified: Wed, 10 Jun 2026 18:10:33 GMT  
		Size: 50.1 MB (50060841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8383b61e494580463f91361a67303e71d428c5c953c0494b0e8981e4c017a36e`  
		Last Modified: Wed, 10 Jun 2026 18:10:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc43d07987fefba1207b54e9af63f0626d8f6e8c9c7ef163466cb93624570654`  
		Last Modified: Wed, 10 Jun 2026 18:10:25 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865d183f7b8657b4c28043dc6103646f393df49ce1e5ae9f9c51355bf438c994`  
		Last Modified: Wed, 10 Jun 2026 18:10:25 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
