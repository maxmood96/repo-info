## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d5298c4fb7312f99429be7d648461976d11b4e80e01b76cfa59331dcbc2a7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull traefik@sha256:a0158df29295b8698f1610896fc10ab7edeb4ef1f4196578ec05726c63f1ff96
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310758553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd978f01f28865c75efb1886c529f4248e1a434ba1fd27eed3c9bf5e63c7070`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:31:48 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.20/traefik_v2.11.20_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 13 Feb 2025 00:31:49 GMT
EXPOSE 80
# Thu, 13 Feb 2025 00:31:50 GMT
ENTRYPOINT ["/traefik"]
# Thu, 13 Feb 2025 00:31:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.20 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973ab6226f7cc287e3031921c05a6c54e3a11fe8aa0f99bdf68ea087d59bf6c`  
		Last Modified: Thu, 13 Feb 2025 01:08:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5d22361fe26328d6c0de2f0e191f0e51c5fa5c200fcf190fe04bcd9675bace`  
		Last Modified: Thu, 13 Feb 2025 01:08:37 GMT  
		Size: 46.9 MB (46895179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd4eaf21694c85afa2267924edbb3e03a147f448bc1febc34e2bee85ad9ddc8`  
		Last Modified: Thu, 13 Feb 2025 01:08:32 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e5f26b5ce1266eaa80bb619dd46cc7553b363812a64f33da7e04b15d89c805`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6300d967adb8f24af49eb85e8d018c15defc45acb4d165e146a0710884d4ef`  
		Last Modified: Thu, 13 Feb 2025 01:08:33 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
