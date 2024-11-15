## `traefik:comte-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:0b49d7c5c747776369a7807f250002a34372fcb2c610a4429d6d6b917eb36d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `traefik:comte-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull traefik@sha256:af799d37c775934668bbdc255e43c583adc197585995843bcf4802deebafd8e4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299923813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0952354fa64192a659d07331a320dda5082dcee1f3041a2748d1366f53fd1461`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:20:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:20:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 14 Nov 2024 21:20:43 GMT
EXPOSE 80
# Thu, 14 Nov 2024 21:20:44 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Nov 2024 21:20:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84e195bfac84095938b63c65af6344eaa6ad5f539330cd73c64fd93ff8a5230`  
		Last Modified: Thu, 14 Nov 2024 21:20:48 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff02eafb6bbdafaf02a88b8e14dbcab21979af1a5e0291f91337dde9be879`  
		Last Modified: Thu, 14 Nov 2024 21:20:54 GMT  
		Size: 47.4 MB (47434445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1286672a5f15f6b859df382f17559a104e4f79a50fb1160bc64fddc251a677`  
		Last Modified: Thu, 14 Nov 2024 21:20:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87abcfa18f2b169642829487868f68cd68fbe7ded30b08bcaac1daee1ef6acc2`  
		Last Modified: Thu, 14 Nov 2024 21:20:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a6aa26fcee86000e96658d38f662002836a5c4214801998adb4af6ac6eb166`  
		Last Modified: Thu, 14 Nov 2024 21:20:48 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
