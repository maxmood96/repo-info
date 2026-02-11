## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
