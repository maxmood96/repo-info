## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e242d72781114c7470c33bed00e5863c8fca11ea9c65498b17a4be6254489401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:eb2c4cce41771173ed8e326167ad75d45d3e2941e7248df153131e23144e3915
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818037274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d16ca057934757876a99f3d9b5b8d06fb4c12168387885cd3e2c356552cdb3`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 13 Nov 2025 19:24:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Nov 2025 19:25:06 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.31/traefik_v2.11.31_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Nov 2025 19:25:07 GMT
EXPOSE 80
# Thu, 13 Nov 2025 19:25:08 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Nov 2025 19:25:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.31 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd60500bd54f2c8f4b479ab0318882c864fff054ffe6770329aced3b3783f82`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bc8d2506261d13851b73aa8b955c1b9307169a02ab7df4fddf95e70ea4749f`  
		Last Modified: Thu, 13 Nov 2025 19:25:58 GMT  
		Size: 48.1 MB (48070511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b376a84a2d0a70c6e7929f071071456c58f27c3ed16177b5a95e507a7b1b39e2`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6e9ef2151a88935d67becb6afdce774e2f0318cce3c78440f3a7719119541b`  
		Last Modified: Thu, 13 Nov 2025 19:25:49 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3d2f0a500b546e15e2fb7b59d9e49c4beb10399df2bac93ab3b5feaa190da9`  
		Last Modified: Thu, 13 Nov 2025 19:25:48 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
