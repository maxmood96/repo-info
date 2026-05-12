## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:157fe073b3d5e9982b3152c38387fab0ccb22fcd0b0ecfac1a1f9505e8d30f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull traefik@sha256:3bdea514924ab8e61f705793510aba4abdbbc09854f7c874a632579834f7ac0b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2120040338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a5c69bf294225bfac422d2191aab80dce5fc3def4e9a599405f72ef589a1d9`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Mon, 11 May 2026 21:46:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 May 2026 21:47:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.7.1/traefik_v3.7.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 May 2026 21:47:31 GMT
EXPOSE 80
# Mon, 11 May 2026 21:47:32 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 May 2026 21:47:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:59bce1e29b114db5563fcd892d2c84957519a6bbaa25acd04961c7db9af87fd3`  
		Last Modified: Mon, 11 May 2026 21:47:39 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abcd538048523c3daa573c978e72f5e1abb6b1ff3a250fee73d91d5673869ae9`  
		Last Modified: Mon, 11 May 2026 21:47:47 GMT  
		Size: 49.8 MB (49823846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7efa03855c4ead47bda184db72a07b94b9ed7672af17a36bf549006e69f6d2`  
		Last Modified: Mon, 11 May 2026 21:47:39 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5563d8e0ae421447628fc9857d863d0bbfd0f5539c6f2920aaf3f3f98969534`  
		Last Modified: Mon, 11 May 2026 21:47:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c37272063a9e47f0855872e8ca0d77088c97325785208e8ce7965e9e3d4f5`  
		Last Modified: Mon, 11 May 2026 21:47:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
