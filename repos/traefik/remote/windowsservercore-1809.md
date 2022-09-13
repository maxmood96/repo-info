## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:84b80d25f3a2267384a31d438bea47b75256258fe5c7d2d458312c5b35842792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull traefik@sha256:b7c78f8739641f8fb17ba16db5d4467fdc984239aea8c15a6a425d61a5a63726
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2733827197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c628896d0a4bd9460b62a375fc22a99bb1c32bac428e3c5f3143bdaa85116816`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Sep 2022 18:23:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.8.5/traefik_v2.8.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 13 Sep 2022 18:23:35 GMT
EXPOSE 80
# Tue, 13 Sep 2022 18:23:36 GMT
ENTRYPOINT ["/traefik"]
# Tue, 13 Sep 2022 18:23:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.8.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:0a5a7a7fc317e347125a1f57626cf99448c897d1e193cb39b3389d0309790b1f`  
		Last Modified: Tue, 13 Sep 2022 18:25:31 GMT  
		Size: 30.3 MB (30256782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f48547d8e38f8f77d5668596e89f09cec313c88209ad1cb20cc912c938b6e2`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2c407588e5d1afb60580e8e82e167721e88544f91ff4e62a263ad4f7fea54b`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68faac36cb0c791f445fba14ab5ebe23ebca7a8e86628366c62aac87d03183f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
