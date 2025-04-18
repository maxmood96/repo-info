## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:a4ccf8f2192d0437737508b822d428fc974495bdb616fed4be8fd93a7f8b9b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull traefik@sha256:6cdcc03c490deb137267843b023f82907c61842612a4f0ef25ef15808b80a653
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325760481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caae865e7402b99cdf60157c3af0ef0708b7bd37ff25c1f1af67074a2143eed`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:18:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:18:38 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.22/traefik_v2.11.22_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 18 Apr 2025 03:18:42 GMT
EXPOSE 80
# Fri, 18 Apr 2025 03:18:42 GMT
ENTRYPOINT ["/traefik"]
# Fri, 18 Apr 2025 03:18:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.22 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2930e8852743c9b5f3b7e52b3342426d0b1524e7bea713fd9706d10af1470bf6`  
		Last Modified: Fri, 18 Apr 2025 03:18:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c81ce39caf898fc1d7b63e23a5ba9d1c6a8c878f2ff7de00b7024a0b20ad60`  
		Last Modified: Fri, 18 Apr 2025 03:18:55 GMT  
		Size: 52.2 MB (52172810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a906aea0aa6d41060c7a3b8568e4e61241a481318a3727169672c1367f63173d`  
		Last Modified: Fri, 18 Apr 2025 03:18:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73831971eae17c8dfa2df587bd4b849da8c3f709fd863a7329b83a6eb7fac594`  
		Last Modified: Fri, 18 Apr 2025 03:18:47 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3e500cb617c9c234bc0af805663377968aae92992ab1148e7c7eafb2893eb`  
		Last Modified: Fri, 18 Apr 2025 03:18:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
