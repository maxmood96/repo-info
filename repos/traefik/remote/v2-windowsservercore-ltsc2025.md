## `traefik:v2-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:075b594e182cfb3f62aafb2c48094181ed3926cae9d75c714de2c93c1d009bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `traefik:v2-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull traefik@sha256:fa03a619e1bfde32d670738002169bd3c6faac058006aa47c9caf155b662676c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180029731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923cc5ee4bf7e0ab1892a1d273b716e378e6f3502e921693aeeb2cedbd4309bd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Mon, 11 May 2026 21:45:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 11 May 2026 21:46:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 11 May 2026 21:46:47 GMT
EXPOSE 80
# Mon, 11 May 2026 21:46:48 GMT
ENTRYPOINT ["/traefik"]
# Mon, 11 May 2026 21:46:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ca95988ceb655ca35fef05dd049af08dff346281ce93089f853a456893c0f487`  
		Last Modified: Mon, 11 May 2026 21:46:53 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869f2d22c5f79ed3bfbb7594c06160a511cf362ef2bf6b9b9233c6f8962d8dd2`  
		Last Modified: Mon, 11 May 2026 21:46:59 GMT  
		Size: 50.0 MB (50038455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af7ee03c05c2d0d72dee863859049cf89041a10c44ac829c1a01cc466e1cf5`  
		Last Modified: Mon, 11 May 2026 21:46:53 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a342a3ea5a833b15cbc308cfc692beac104bbb52e88a14d81cb8fe80d8746d6`  
		Last Modified: Mon, 11 May 2026 21:46:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fad32bf94aa17b626d960a0a63ee9fb58ea046b838ebe45beb02e983bfcca41`  
		Last Modified: Mon, 11 May 2026 21:46:53 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
