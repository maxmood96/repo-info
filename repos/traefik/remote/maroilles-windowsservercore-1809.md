## `traefik:maroilles-windowsservercore-1809`

```console
$ docker pull traefik@sha256:7c233c425c02be64e4d02c6ac904f8fd586214173652667ed12a6cbe40b35251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `traefik:maroilles-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull traefik@sha256:3cfa84be7d7e57c654a1a3b8e4c41b7ba5f3c5c550cb0174b550c2db0c88be3b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726409092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe8cd7f2792b2846bba0ec097dd8b13686688eaacc32a4e789952137e619ede`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Sep 2022 18:24:55 GMT
RUN Invoke-WebRequest     -Uri "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_windows-amd64.exe"     -OutFile "/traefik.exe"
# Tue, 13 Sep 2022 18:24:56 GMT
EXPOSE 80
# Tue, 13 Sep 2022 18:24:57 GMT
ENTRYPOINT ["/traefik"]
# Tue, 13 Sep 2022 18:24:57 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fef8fcae363c967cdda31871dbfcc00b3f35458cbfcba05f7a6d1552c3b9d83c`  
		Last Modified: Tue, 13 Sep 2022 18:25:55 GMT  
		Size: 22.8 MB (22838714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14ce042369487448642ab933c5aaf18199baa6713c317cbae8067107daeaeca`  
		Last Modified: Tue, 13 Sep 2022 18:25:49 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1836085afff7fe0b9beb9748abe6f34d94003944e2981312832ee76886845d5`  
		Last Modified: Tue, 13 Sep 2022 18:25:52 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24edcfd0e075a20e436658f609f8aa0212feb2c0739e613d2cd95a333639bfe3`  
		Last Modified: Tue, 13 Sep 2022 18:25:49 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
