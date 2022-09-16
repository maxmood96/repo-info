## `traefik:banon-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fbd2965947bd1bbffb724752b1af26bfd3c2bcf61a36f169bee5d0356347362e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `traefik:banon-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull traefik@sha256:87875e822ffe342ac7a1feb6788e720ff7b6a88765e195e52869bad9bc1ac0eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2733959298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e8f0775dc9296bf7fea874a2c3ccde4292deecce73505068aafb98ed2c7546`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Sep 2022 18:17:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.9.0-rc3/traefik_v2.9.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 16 Sep 2022 18:17:28 GMT
EXPOSE 80
# Fri, 16 Sep 2022 18:17:29 GMT
ENTRYPOINT ["/traefik"]
# Fri, 16 Sep 2022 18:17:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a45b83fca0335f3155ed420888474fc8c244febd127a53e4ea6a759d721ec86`  
		Last Modified: Fri, 16 Sep 2022 18:18:28 GMT  
		Size: 30.4 MB (30388898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a642cc4ac7c54eedc57165cde0dd587dc0d74093d4350d4dc02bb195251359b`  
		Last Modified: Fri, 16 Sep 2022 18:18:21 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c87e10a6c846b34d402067281acf136665b3c3f6aa33412de6c29ea9e18b24`  
		Last Modified: Fri, 16 Sep 2022 18:18:21 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7723f1113e3fe6c83a21fa62fcf01e134f3669ac26ed3bfa76ab72818279a5e1`  
		Last Modified: Fri, 16 Sep 2022 18:18:21 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
