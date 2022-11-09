## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:fc7f1107103b2ae2fa0994d00adf6449cb325d68bb714cd8676b4828bad51a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull traefik@sha256:9e831c3e34a7ba03b26c220e70f18be9185063c19dc327dc042114488488e1d3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2814256590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a46a6698c0d6de9e6c83ceeb3eda68120d771f525827ffae038f5b01f80fcb`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Nov 2022 19:38:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.4/traefik_v2.9.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Nov 2022 19:38:08 GMT
EXPOSE 80
# Wed, 09 Nov 2022 19:38:10 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Nov 2022 19:38:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1457b5602c76a5bee2862f07b1b43f115cf4d8eb57db1efd704949cd44e0ddf1`  
		Last Modified: Wed, 09 Nov 2022 19:40:25 GMT  
		Size: 35.7 MB (35664347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318f18a5dff4fd50f36989efdcaea2ce96bb76f0e27155ebe945b78ed9c54493`  
		Last Modified: Wed, 09 Nov 2022 19:40:15 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0efee0efe52876c56d9d88d913c87aa07c31780df61b3e5d39767967c8f92c`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1f7d7d03b62b82ed6e5a9a0bcd5f8eac821ee45411f9b690c71ff5cd7b5832`  
		Last Modified: Wed, 09 Nov 2022 19:40:16 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
