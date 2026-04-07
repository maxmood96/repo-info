## `traefik:langres-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:4591d16b51c6cc0be8e39d65568db4444111089beed0147a07dda64ee4fef110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `traefik:langres-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull traefik@sha256:138f46a5e3dd2da2e11fbb2dccdb4ba5cec5cf42ec5f7c3456da38265863eded
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130465445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e368b02a1ab7392164b98ed21f4084c535689a22c2c7ee4e97913face90f1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:42:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 17:44:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.7.0-rc.1/traefik_v3.7.0-rc.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 07 Apr 2026 17:44:08 GMT
EXPOSE 80
# Tue, 07 Apr 2026 17:44:09 GMT
ENTRYPOINT ["/traefik"]
# Tue, 07 Apr 2026 17:44:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.7.0-rc.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:94fa5d4d40c81e6964cffd8393b08eed40660be1e3978e992afce43715a4ad14`  
		Last Modified: Tue, 07 Apr 2026 17:44:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabf810361f0454be8b94436e484af40ce72766f5d86eb0e5770568548be75b1`  
		Last Modified: Tue, 07 Apr 2026 17:44:38 GMT  
		Size: 49.3 MB (49264182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612fabacf6c858c6a3867e7a7c034596a310da0c5ce167cbd659d12ebf6736ed`  
		Last Modified: Tue, 07 Apr 2026 17:44:14 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592daf48c329281ca8a60d429488707356b0133f34bd0fdb0480c9985aa16e77`  
		Last Modified: Tue, 07 Apr 2026 17:44:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49754f28d223395f1a48feac5915376ce4ce8212a0d7f57c7c76d5a69bc2ee9`  
		Last Modified: Tue, 07 Apr 2026 17:44:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
