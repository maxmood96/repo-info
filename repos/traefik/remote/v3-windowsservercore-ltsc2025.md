## `traefik:v3-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:aa4b67f6d64bb081603c35458d906aa5f0c99fb9920982ef57efeb719bb521c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `traefik:v3-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull traefik@sha256:842d96703855b9f9655d20b6696bb2782f7efee1d20cf6a0a310f1234adf22c3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2130745604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d148f9daae0acfa8b4651e81a24e4d76462e3bf42212c688cdc77b5563e02d`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Thu, 26 Mar 2026 17:20:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 26 Mar 2026 17:21:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.12/traefik_v3.6.12_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 26 Mar 2026 17:21:52 GMT
EXPOSE 80
# Thu, 26 Mar 2026 17:21:53 GMT
ENTRYPOINT ["/traefik"]
# Thu, 26 Mar 2026 17:21:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.12 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:9bc5895798c7141b34a9c0b9d736f9ae3dea4b1bc8cfb7e79e2a0a82044f1ad6`  
		Last Modified: Thu, 26 Mar 2026 17:22:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08c01f33ce4d7600459689cea9d0b587cd8674077aa0e4983cb7c817ce7dff2`  
		Last Modified: Thu, 26 Mar 2026 17:22:22 GMT  
		Size: 49.5 MB (49544362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d249676c5ad269da00be2e1af14595ac633521b3af87942c0b40553939fa7f`  
		Last Modified: Thu, 26 Mar 2026 17:22:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e42d802e752769f94890622f01ff182148f6324ce3b473fc39e9121e856069`  
		Last Modified: Thu, 26 Mar 2026 17:22:06 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e4d8f4d06bf242ccc464b85ff4750287da6e75e3de7d7e6ffad1e3246e52ba`  
		Last Modified: Thu, 26 Mar 2026 17:22:06 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
