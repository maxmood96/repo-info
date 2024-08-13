## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:2b3401bfb226fa7d4636416a68ff421013a684970805ac0253f926736d6ae007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull traefik@sha256:7bb2153d5b0443761f4befa2a0274288cc579721ac0a6fcd1ca73876e90d42f8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186020385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5104a96a9c7d049c7e5d836eab6dfb70bb07569d011e9d85f271907fcab0b1`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 19:35:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:55:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 13 Aug 2024 20:55:03 GMT
EXPOSE 80
# Tue, 13 Aug 2024 20:55:04 GMT
ENTRYPOINT ["/traefik"]
# Tue, 13 Aug 2024 20:55:05 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e300ced4fe41f30e1e3ad2f70267371105499fbbd08c968b2a967fd27e5859`  
		Last Modified: Tue, 13 Aug 2024 20:27:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f95b5372f8a4434ed7032091c1b3efca7770064280622dcf633e091d2ba04b`  
		Last Modified: Tue, 13 Aug 2024 20:58:15 GMT  
		Size: 44.2 MB (44249869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3561bcae42ca202c51d5fddc776bff203a8c72be7cc51378df62588431462784`  
		Last Modified: Tue, 13 Aug 2024 20:58:08 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56458ed1d901cb4df02a651480ae8630bc025a3c2d72cb5fd51fec50eda11428`  
		Last Modified: Tue, 13 Aug 2024 20:58:08 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863c0d7fc16c78ac112b665608aa7ed30e166d794bf05c249e3575dde46b415a`  
		Last Modified: Tue, 13 Aug 2024 20:58:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
