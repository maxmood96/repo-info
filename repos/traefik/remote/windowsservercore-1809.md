## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:ede6573eee00a50e9cb1430721efee0f61861dc33aa904d6620760578058f78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull traefik@sha256:1ddabb841c2cf1d602e213785d5e0b871979056be6f7bf5dc49dba3855c6a2e3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2064078802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca5f0ffc2582545756c666540e4466876c80a0258f4b1c8df46a31929ec8775`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Mon, 06 Jan 2025 15:26:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 15:27:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Mon, 06 Jan 2025 15:27:23 GMT
EXPOSE 80
# Mon, 06 Jan 2025 15:27:23 GMT
ENTRYPOINT ["/traefik"]
# Mon, 06 Jan 2025 15:27:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbae836f2c6ffe1bd28b7f89d5dbbcf137a5e394bc25b9b5f6499c10bf7e15a3`  
		Last Modified: Mon, 06 Jan 2025 15:27:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e214e7c536633844c0132523d06ce3ac67855c066b5467c9eeabcc98345d6db5`  
		Last Modified: Mon, 06 Jan 2025 15:27:34 GMT  
		Size: 49.9 MB (49903416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca4c28dfc2fc9a5e170e9aca2d5c416f5d32cf3ac3b16991e46b3e1167d809`  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56cb9d595324b157479ceffc37dd663142036b917844526bddbecc3f125616b`  
		Last Modified: Mon, 06 Jan 2025 15:27:28 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc8a283e8c6c31b38b7dac77b78212a46885ff78adac3b4d3a21fcf94a9f0fa`  
		Last Modified: Mon, 06 Jan 2025 15:27:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
