## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:b461cd12ff0d1af5f52e08c309bea63992ffcf53b1d598e2cdb516f2346475e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull traefik@sha256:2c0964975088240d92d0e1cbb5c2cc5991dfdc6f7dbe6ecdc908b547cb0f1a32
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1506494607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ea7f80482088ca28b66348f300ebacf22b423774124faccfa565d9fa7ab180`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:03:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:04:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Sep 2024 00:04:14 GMT
EXPOSE 80
# Wed, 11 Sep 2024 00:04:15 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Sep 2024 00:04:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03344b4cf86453cf6d4d23c750e7da921a5c787e86c885b7f4acedffc640df53`  
		Last Modified: Wed, 11 Sep 2024 00:04:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1108ef64219f9687a073584fdf0f63aab94cf1b863f9e3243b0c3d8212ab9dd6`  
		Last Modified: Wed, 11 Sep 2024 00:04:23 GMT  
		Size: 44.3 MB (44297034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d31b6ee21ace7c641f4055d21bd3dcaa961aa1300272c423951aaa353a24cf1`  
		Last Modified: Wed, 11 Sep 2024 00:04:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250b74c65f45e72ce0f62c87d13351d2a4057b71155374f99c796c02d5a17832`  
		Last Modified: Wed, 11 Sep 2024 00:04:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4832555f17eb65e787c2106a1793777856ad67a0189985502ec61d69d1b9ad`  
		Last Modified: Wed, 11 Sep 2024 00:04:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
