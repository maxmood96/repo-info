## `traefik:langres-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:c352516f86faab479006739839795ebcc9c164edad7c3220d13ebba0727f01b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:langres-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:732671d8bef626ebad713172aca8d68892665c052dd961a26fde0ae107e9c8c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2032055998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d341417297b23076330f4c672b7895a791c5b6c68c9e9d63054a6b6e3de7594`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Thu, 12 Mar 2026 18:57:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Mar 2026 18:58:54 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.7.0-ea.1/traefik_v3.7.0-ea.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 12 Mar 2026 18:58:56 GMT
EXPOSE 80
# Thu, 12 Mar 2026 18:58:57 GMT
ENTRYPOINT ["/traefik"]
# Thu, 12 Mar 2026 18:58:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-ea.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f179d2e1a5ee1cdffa1f04b5eb040061649c700490171e9c5d151c9edd2f796c`  
		Last Modified: Thu, 12 Mar 2026 18:59:12 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10fa0b488e75dd908c4475d50e4b76b5c6744383d775a2cc3a772594a289d3d`  
		Last Modified: Thu, 12 Mar 2026 18:59:20 GMT  
		Size: 49.8 MB (49769372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499c8a7e987a6b086b49dce14e2d125908551a64bb69e2ba7d5591897358eb1`  
		Last Modified: Thu, 12 Mar 2026 18:59:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42d3dc5326be4d132b7bb9d253339f4ad57ddf75d13853c48d9d21804b55441`  
		Last Modified: Thu, 12 Mar 2026 18:59:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aadc99197ccbf3b904ee0c45e412e05208df47e5809877df6649476909da52`  
		Last Modified: Thu, 12 Mar 2026 18:59:12 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
