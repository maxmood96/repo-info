## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:ee30c559c0b9dde84a88daa33f8afdfdbe4e7c39598a1e1efef62d172a76cef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull traefik@sha256:9a2cbeb502fa9f9364b080d830f895f2b0d5f04d0255099b05bd64b6c814b4d9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884717352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c9c3fb4a6eed8d5784a720a4e4fbe0bfbcb0e23871b27825bb16a58e6abdaf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:52:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:02:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.6/traefik_v3.6.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 13 Jan 2026 23:02:55 GMT
EXPOSE 80
# Tue, 13 Jan 2026 23:02:55 GMT
ENTRYPOINT ["/traefik"]
# Tue, 13 Jan 2026 23:02:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23bc3ca2680b957e34cc3091ac9144824a7199ca3cacec82251cc10fec8f7a7`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3029ff9f680a9cfa264f06099aba73519723172a6808f1c70d2cb27cc802cd7`  
		Last Modified: Tue, 13 Jan 2026 23:03:26 GMT  
		Size: 49.1 MB (49052944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c727645df1b566764d8e6286059fbdf10460aa94df79ff282f28d57443b08316`  
		Last Modified: Tue, 13 Jan 2026 23:03:21 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5a1b0296d39bf225671a851ac1ea6bc69c5db7b5a62990bfa2d2a8214f8b47`  
		Last Modified: Tue, 13 Jan 2026 23:03:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fef8cd718b6720d775e9671ca1025c7602978042e8161c3c07cac9485c97f8`  
		Last Modified: Tue, 13 Jan 2026 23:03:21 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
