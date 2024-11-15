## `traefik:comte-windowsservercore-1809`

```console
$ docker pull traefik@sha256:fd51c62222fc0cfb10485aec3227820a3b2805987a92be2bedacfadcb1464d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `traefik:comte-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull traefik@sha256:9a9009e6f9f55c4d0d5e4a7befc57bd1f993cc4f870d01431cbd289aa8df30c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2058231366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7923e73461cbde0c441420f918318d4d3ace541fc095cd1a5471f24050f902b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:12:14 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.7/traefik_v3.1.7_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 14 Nov 2024 20:12:15 GMT
EXPOSE 80
# Thu, 14 Nov 2024 20:12:16 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Nov 2024 20:12:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.7 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6c2ae4b9a24655753f8dbc001db10a6f08923ec0c48bd67273020487bf92dc`  
		Last Modified: Thu, 14 Nov 2024 20:12:20 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba18fc66b10659dee374d8641a3a5484683e67e8a0a9c56bdfb91649efac0b8`  
		Last Modified: Thu, 14 Nov 2024 20:12:26 GMT  
		Size: 47.6 MB (47572170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee97a359d00abc86fe9336ed8dd74567608b96c8efb81f94f1417005c82283`  
		Last Modified: Thu, 14 Nov 2024 20:12:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bb9fb045c3295c29cf6b236cbb9ad6ebf8d1aab56b10c21f85d5e1b7169944`  
		Last Modified: Thu, 14 Nov 2024 20:12:20 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ba39d5e703b96d06292beaefc34a6ee2f8e69bd7d2e0c49d3683756f8c0e76`  
		Last Modified: Thu, 14 Nov 2024 20:12:20 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
