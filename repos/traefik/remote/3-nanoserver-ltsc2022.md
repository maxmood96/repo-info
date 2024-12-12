## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:86610fc15b71ab271212d4ed1e3ccd3746b5c96d0265d720c81a23e9fc6d2793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull traefik@sha256:18fb3d0af76e890469f317a3d2ec17b1fc33aa7c91539b96d6ad908444d434d0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169513861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b997e1967e51d4406b300e11da353c7755fe3f3ada7d90e47cea15dcac8f38f`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:48:42 GMT
RUN cmd /S /C #(nop) COPY file:a4119dd5079022aea22363901b7dd6f116b350cca29b6618e55d06fc15514ce9 in \ 
# Wed, 11 Dec 2024 21:48:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Dec 2024 21:48:46 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Dec 2024 21:48:47 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.2.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Tue, 10 Dec 2024 18:34:17 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f902949776fc2e46eb58acbcfbea9b747e1b63ba0e81f760f94ad347a0d824b`  
		Last Modified: Wed, 11 Dec 2024 21:48:56 GMT  
		Size: 48.9 MB (48909445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed68acd1455bd7eed66668d1febef22ee35e1ef5675abbc4ff1e9541a81e5ff3`  
		Last Modified: Wed, 11 Dec 2024 21:48:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c37b3a751d2e71cfe3eeeb8d9fc6370ec3ee9d3cf3afa759a019d1f338b461`  
		Last Modified: Wed, 11 Dec 2024 21:48:50 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35412dee8ef6957e0dfc571bbfcdf6fb13ab15df8448316ff20ed821f747938b`  
		Last Modified: Wed, 11 Dec 2024 21:48:50 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
