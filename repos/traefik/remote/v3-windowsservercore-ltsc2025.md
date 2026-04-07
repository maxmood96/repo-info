## `traefik:v3-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:a98869ab069ed3c136add61c1f9e297ae147141d0feb91f81c9501e48ac11fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `traefik:v3-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull traefik@sha256:b95e210c711353ec8212f1d6b1118d5698d64b8dd872b2140fdce067a5bba092
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130733096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eba163d880e578f6d6e8b9f9c5ee6660adb2cf7b068c8f742fbf98ab7b27121`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 17:47:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.13/traefik_v3.6.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 07 Apr 2026 17:47:19 GMT
EXPOSE 80
# Tue, 07 Apr 2026 17:47:21 GMT
ENTRYPOINT ["/traefik"]
# Tue, 07 Apr 2026 17:47:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.13 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68a5c25fbe51cb9c318ab8b65ff5fd811e531ca794772a1e3d3880e4b4e222d`  
		Last Modified: Tue, 07 Apr 2026 17:47:53 GMT  
		Size: 49.5 MB (49531849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9beac51d3220bc367ff2753eaa85159f4770d123430991a988e7f087d09f0de8`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baccdc1f30d0f911576f10e076fbc322abcd8753d3d396858a7d1bfd45e01d22`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0b62ed59dd77b8e890646c48f96aae8a7b07c9e3d79749c423f42ec6e655c`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
