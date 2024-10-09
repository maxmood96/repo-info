## `traefik:munster-windowsservercore-1809`

```console
$ docker pull traefik@sha256:250ccb94c94473e91a138af57ad13f9dd2e369d704602ed13a030c6361686485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `traefik:munster-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull traefik@sha256:2bd200b67bfd8d8814799e97e6324fd67d546c25c9114e388c5ba7c00ade1610
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1767531915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1946e1a4a29129cead23084118a041aa4c976131c620fcb41447e0f75b0a8a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 17:56:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 17:57:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.2.0-rc2/traefik_v3.2.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Oct 2024 17:57:53 GMT
EXPOSE 80
# Wed, 09 Oct 2024 17:57:53 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Oct 2024 17:57:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba58e8f3830792f9d37d02524c816cc859bd98ec460caead98a5f1c0559ab4c`  
		Last Modified: Wed, 09 Oct 2024 17:57:56 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac591409370fb60a4242ddb0c19d68729e13e84c6682bf6d3d236a451808587`  
		Last Modified: Wed, 09 Oct 2024 17:58:02 GMT  
		Size: 47.3 MB (47258350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88ac543cf5d5f28fc092fb816bfde0541b513245a5674af748021900d92bc98`  
		Last Modified: Wed, 09 Oct 2024 17:57:56 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7f09834eeeec86b7cf7abb3dad9d9f97f8143e774fe3462518f8d7033ddf28`  
		Last Modified: Wed, 09 Oct 2024 17:57:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc6ac200ecee198066b5e34401e377af574728db0e49b527e18606a705c481a`  
		Last Modified: Wed, 09 Oct 2024 17:57:56 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
