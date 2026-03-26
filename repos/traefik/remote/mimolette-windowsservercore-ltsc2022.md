## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:238b8902ab394a3e061a0fc91f30b517f3822a157cb25a22bd2256403245f879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull traefik@sha256:9c8b4fd9265d7afe1319d00424d1df39817943bf98a132c3ff16469ca7f989aa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030606843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d732183cc7249d386f85c3fef0230a93b0b8cec1d56fda4d51fdf487af7d0856`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Thu, 26 Mar 2026 17:16:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2026 17:17:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.42/traefik_v2.11.42_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 26 Mar 2026 17:17:23 GMT
EXPOSE 80
# Thu, 26 Mar 2026 17:17:24 GMT
ENTRYPOINT ["/traefik"]
# Thu, 26 Mar 2026 17:17:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.42 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ff01d18ba3b1ba66ae90c488e7658bd636c52497f2da6356714ef87ccf46f21b`  
		Last Modified: Thu, 26 Mar 2026 17:17:30 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528f746fd42546e6c50d00303aae10f22e45348c78a237bff4feb263ab9f4ef0`  
		Last Modified: Thu, 26 Mar 2026 17:18:11 GMT  
		Size: 48.3 MB (48320275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9034d923e987ba58604acdb1abbb5d3e480549c557c0d987f6a6217f95c6ff`  
		Last Modified: Thu, 26 Mar 2026 17:17:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8513dd595dc9b961723007cdb3ba74d5b6f7842abb2b3d796b0ccc62cacfd4b9`  
		Last Modified: Thu, 26 Mar 2026 17:17:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827feff2d9059d28eb5f5d19edbed92f35d8b71314c9eb05f4ed07c00cf6c1e8`  
		Last Modified: Thu, 26 Mar 2026 17:17:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
