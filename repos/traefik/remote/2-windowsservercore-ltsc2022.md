## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b8da8d31174e16863dbcbf41bec1954b92c974d03b808c2ec15db6790e1838d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:2ba7d309ed05e9b744163632494559fb3e8325606c820c16be6857c548ecb107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030559824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f73a1a59c457970729649e0f645268d41f51c7cb3f52a34058455f3916d6405`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:55:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:49 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.40/traefik_v2.11.40_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 10 Mar 2026 22:05:50 GMT
EXPOSE 80
# Tue, 10 Mar 2026 22:05:51 GMT
ENTRYPOINT ["/traefik"]
# Tue, 10 Mar 2026 22:05:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.40 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d6d5e3e0ff6e92ce7cae76c8671079083e197ef5ac43484b480278bafe25a4ce`  
		Last Modified: Tue, 10 Mar 2026 21:56:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45af5fe2d2e89f1a23cd1b3304ade2b49529c3642512eafdb9e979b09c2c0fc`  
		Last Modified: Tue, 10 Mar 2026 22:06:08 GMT  
		Size: 48.3 MB (48273206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e583d146b3c8c8f237e48412bad481f189e1b5d3c5085892a2ea504eb8f012b`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5298becfec44cd855b95089f6e4f8ec037c56d2e2d4153b8dd15aadc40c2263d`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ba5c6f2cd11273e5a0678d0c86b8c11bb84dbafd86bc9d3aa0a574e4dbcd4`  
		Last Modified: Tue, 10 Mar 2026 22:05:56 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
