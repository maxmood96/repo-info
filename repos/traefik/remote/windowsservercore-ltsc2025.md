## `traefik:windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:72ae7d87e9cbbcb8c9711bd7f773a8e35bf9880ed26d44f68759ef34eb07c4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `traefik:windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull traefik@sha256:9482baeb0ceb89f6d1549ac6c8e46b2c933d3bac269cc01ef765d1780f445e98
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179640296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3e286a9ba37c18941addb9279360333dc5ecd40ef76f218981f096bc707580`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 05 May 2026 19:13:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 May 2026 19:15:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.7.0/traefik_v3.7.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 05 May 2026 19:15:28 GMT
EXPOSE 80
# Tue, 05 May 2026 19:15:29 GMT
ENTRYPOINT ["/traefik"]
# Tue, 05 May 2026 19:15:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538f28edb93c7cc553ecd80be1ad338e0181d3490d28987d84067dbf33d4a07f`  
		Last Modified: Tue, 05 May 2026 19:15:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6f7dae797fc0807fcc18c9164c7018d18cb68abf74c797db20715819a52475`  
		Last Modified: Tue, 05 May 2026 19:15:48 GMT  
		Size: 49.6 MB (49649014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c2e65ba2fbf50d9103bbd75988d156b9c32e30b81836ebd0f600d4a0f12368`  
		Last Modified: Tue, 05 May 2026 19:15:41 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9a6fb2493a49071b8910284024460b83990a7f3667708c89d0c8ec4add7540`  
		Last Modified: Tue, 05 May 2026 19:15:41 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b2eda71bf19e2fc7160cc39794bd98638233b27ec4cb7c71de761ec0f86b6e`  
		Last Modified: Tue, 05 May 2026 19:15:41 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
