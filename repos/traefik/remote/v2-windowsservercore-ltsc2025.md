## `traefik:v2-windowsservercore-ltsc2025`

```console
$ docker pull traefik@sha256:108025d28b268caf996a2e47cc24133e1a24634e95f810fa45a707bc1e33007c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `traefik:v2-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull traefik@sha256:c4e1bb47260189e875d1d4a1a478fd48456cb97ff83bc4f679048557650b2503
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2129363367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727719fdc89135a09eb2cc41d127e8d9bf47fac9f3c9d91ecb3f6361a17138f8`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Thu, 19 Mar 2026 19:17:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Mar 2026 19:18:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.41/traefik_v2.11.41_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 19 Mar 2026 19:18:54 GMT
EXPOSE 80
# Thu, 19 Mar 2026 19:18:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 19 Mar 2026 19:18:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.41 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:04c9159a47f7380385d8f1149c28f6609251f90bbb3e653d1fb21935853a2590`  
		Last Modified: Thu, 19 Mar 2026 19:18:59 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b5c518eae3c232f9537a1fa38f2b76baca03c8324b5010dd7357d69e8e0a2e`  
		Last Modified: Thu, 19 Mar 2026 19:19:07 GMT  
		Size: 48.2 MB (48162060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da834f354ee0990f6d8409a23b1764901a60b47bcab40895349b80cf87b674d7`  
		Last Modified: Thu, 19 Mar 2026 19:18:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4130cbcbd1b74db24d3a7ba816d7237063c7e0c0d9e38c14678156cdac2a300d`  
		Last Modified: Thu, 19 Mar 2026 19:19:00 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0814eb12d5f6516ad49b64b4e966965e3213664d8f4e24eab0877d16c5df9d`  
		Last Modified: Thu, 19 Mar 2026 19:18:59 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
