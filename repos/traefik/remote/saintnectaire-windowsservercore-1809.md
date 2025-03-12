## `traefik:saintnectaire-windowsservercore-1809`

```console
$ docker pull traefik@sha256:f019f1e6974b1161a6fd71c19d7a29fe3d5b7e7eaa7d887c6b394183384ebc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `traefik:saintnectaire-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull traefik@sha256:59d3c46f4a2554db69d45cb24ac248ec47ee9fef3371ec7a0e3add9e20816276
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201416223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b22915ac9466465a21a904c3a35a0e32f19aecfd15e956b2ff3e34ae6e428df`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:56:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:57:56 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.4/traefik_v3.3.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 12 Mar 2025 18:57:57 GMT
EXPOSE 80
# Wed, 12 Mar 2025 18:57:58 GMT
ENTRYPOINT ["/traefik"]
# Wed, 12 Mar 2025 18:57:59 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2d044e9fb53a1e6c12486b185f2f42e12b192e1f6743c8832346b30e4c7cab`  
		Last Modified: Wed, 12 Mar 2025 18:58:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb32afca199f28ebbbc07d990b1fe92971f6f5bd277d2706cf523a76d83565e`  
		Last Modified: Wed, 12 Mar 2025 18:58:07 GMT  
		Size: 49.8 MB (49776416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa643b8b76808e58daa798de46c5a193437e051ef510285180461589592197`  
		Last Modified: Wed, 12 Mar 2025 18:58:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4befbf36415926a108f088b392d4232720202918d3354a9af1d272caead33`  
		Last Modified: Wed, 12 Mar 2025 18:58:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c814e2206f49cbebf79163d44534b1f276e47532c872d1ad35f6cf288c2f61cb`  
		Last Modified: Wed, 12 Mar 2025 18:58:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
