## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0ed04b177a546a361bfd75017f2065f80b815f7e0b1453bb3ac417da421207bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull traefik@sha256:5497ffbe18f4216eb5cef67a215d8cbc7ab3567f6b44f2f482de457de91ddca7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1845463443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb058ec4b6dfa04c0273b8d320db9d878961a1ee6de93d10baa33d42e0742ab`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:10:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:10:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.6/traefik_v3.1.6_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Oct 2024 23:10:43 GMT
EXPOSE 80
# Wed, 09 Oct 2024 23:10:43 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Oct 2024 23:10:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.6 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f581fca17de08118af57bea2305641658405b027bc3336ed73d1b7660f122054`  
		Last Modified: Wed, 09 Oct 2024 23:10:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc91c57da9295443fa5fe4f82bea42d2a4957b2568b9864de817ad08939c7e28`  
		Last Modified: Wed, 09 Oct 2024 23:10:53 GMT  
		Size: 46.1 MB (46116759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b7d55f86fb2f331495208a0c5fc6f2f3edb2dda1b4af56a3522c507e062b2e`  
		Last Modified: Wed, 09 Oct 2024 23:10:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029b1101b4fae3d1f3c5cb5d5f4661ddcb3e6b7a43b0ef22e5695812e02cc4c5`  
		Last Modified: Wed, 09 Oct 2024 23:10:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932d344c79149fb4c0faf1f1a979b8b90189fd1939be983960ecdd45feaa9a32`  
		Last Modified: Wed, 09 Oct 2024 23:10:47 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
