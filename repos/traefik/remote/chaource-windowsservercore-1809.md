## `traefik:chaource-windowsservercore-1809`

```console
$ docker pull traefik@sha256:0bca713adbee5868c61c5d316087c87e4f3535d6fb1adf13a1d81340e76e2ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `traefik:chaource-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull traefik@sha256:4bc8550d109a3e11e77bb22eb5fbd5c5500d14bc049b62b24f1706754974ad5b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2217855741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13821c7eb81674e476e879da4b1568aab947f8d700dcad6c5e83912ea4e8f565`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:58:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.4.0-rc1/traefik_v3.4.0-rc1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Apr 2025 00:58:53 GMT
EXPOSE 80
# Wed, 09 Apr 2025 00:58:54 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Apr 2025 00:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d66b46695b5a5dbf209eee8c7be900af876bcfb6ffb65a9dab953dda62d945`  
		Last Modified: Wed, 09 Apr 2025 00:58:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bc1cd2f3d18079db9140a227a64af40fef5f62fa641dc63da69439bf65a47b`  
		Last Modified: Wed, 09 Apr 2025 00:59:05 GMT  
		Size: 55.1 MB (55124697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9919bc205889d08a413d57ffd2c296ae700ce8650e95199ad7be8a868471dd2c`  
		Last Modified: Wed, 09 Apr 2025 00:58:58 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac302cbe1b418652ff789798eebbf7c430995b085514e5f5ab0fea0808dce897`  
		Last Modified: Wed, 09 Apr 2025 00:58:58 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e716a2de9ee20119ee77fe9b2b017d4f93c79fe22bf755e256c0a833af4cfea9`  
		Last Modified: Wed, 09 Apr 2025 00:58:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
