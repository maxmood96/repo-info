## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:dcec3000efc0d552358fd44f95644e5e908de7d472a63df0edb574de81517645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull traefik@sha256:2988f00eaf0aeedcab04b601936c36fb3f454008611b35134e846a5f4e26b158
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818121188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31715b9a396950e980e3b2579d073169b112b7a318a9ac5c170d1f0e3edc930b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Thu, 04 Dec 2025 19:23:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Dec 2025 19:25:37 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.32/traefik_v2.11.32_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 04 Dec 2025 19:25:38 GMT
EXPOSE 80
# Thu, 04 Dec 2025 19:25:40 GMT
ENTRYPOINT ["/traefik"]
# Thu, 04 Dec 2025 19:25:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.32 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:94bf6b095296831cd4d5f34d58fa0959fd7ef42e2dc9efd551c55d16e533b161`  
		Last Modified: Thu, 04 Dec 2025 19:38:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bac6613489c4597256f38308be766d6b69566e37eae1ec90fd75668f5ddd323`  
		Last Modified: Thu, 04 Dec 2025 19:38:29 GMT  
		Size: 48.2 MB (48154462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4a3d7b533059c5b4c90f6ad2b5cf3cf561ffd5341fa82b23cb2200e3604e15`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578f85135e09953edf14105875b914705d2e9163f065e361f6df0548ce9a9ce7`  
		Last Modified: Thu, 04 Dec 2025 19:38:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de324d8f25e723e0020dda62e746d4c7d464d758c0e6ecf94b2b5b741d0b25d0`  
		Last Modified: Thu, 04 Dec 2025 19:38:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
