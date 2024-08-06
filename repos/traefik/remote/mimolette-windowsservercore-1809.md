## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:b08ba4567e6f68d1d68cd0149471ff9dd82c9470aa8f1e3df8de765b9e064bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull traefik@sha256:001edf5d736b731937df83d664e3a0891d1f21701a38ac42212fa2a5a74b3ce0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2282861485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4f513fdc6e01b11fb08bb053e1e968472bdc3dba46fe432ac1ef48e16561ea`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 16:36:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Aug 2024 20:19:43 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.8/traefik_v2.11.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 06 Aug 2024 20:19:44 GMT
EXPOSE 80
# Tue, 06 Aug 2024 20:19:45 GMT
ENTRYPOINT ["/traefik"]
# Tue, 06 Aug 2024 20:19:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396e1b977f1ec2790de6e1bcdd9b0272d3ab46f70fdbef2ae277b7f99b83d0b3`  
		Last Modified: Wed, 10 Jul 2024 17:26:34 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bed07833e643f27acef35a4087d24d7f1f61958dfb5667fb929dfa5c4f800d`  
		Last Modified: Tue, 06 Aug 2024 20:22:11 GMT  
		Size: 44.4 MB (44426615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c22a757ab9cdbe650c8d9571617871118cf24d40f179c055fba099d37a4e593`  
		Last Modified: Tue, 06 Aug 2024 20:22:04 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878777534ca1d39df27364ae2f8140c56b95b297accf2d85e2b2c8988804805a`  
		Last Modified: Tue, 06 Aug 2024 20:22:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17164f9b8a61075a91c6c05fbe0e6fd3803cb49a25e5594948f448fda0860a27`  
		Last Modified: Tue, 06 Aug 2024 20:22:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
