## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:6cf1a482d3ff8be6017a33c4569b8a772810800c2adbef410fbe02a74e179f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull traefik@sha256:6ce6329f37820faecde7ecd6045d49bc9b5ae35ee0066f3caa861bf256f2c3d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766257436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66520ca57e7c42e43a64fc75edc5db026a6f791d62c0af5dd65b18656b99d60e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 02 Oct 2024 23:56:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 02 Oct 2024 23:56:46 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.1.5/traefik_v3.1.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 02 Oct 2024 23:56:48 GMT
EXPOSE 80
# Wed, 02 Oct 2024 23:56:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 02 Oct 2024 23:56:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b9ed23ba3da1981421086477709c42e33bb7c7a5f8e82f6087856d36c3b0c2`  
		Last Modified: Wed, 02 Oct 2024 23:56:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f30b67c628e6e4b524837c05a107f94f1642a2fd1a8a0cb6f7e3014bffbd548`  
		Last Modified: Wed, 02 Oct 2024 23:56:59 GMT  
		Size: 46.0 MB (45983900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5970d5d83babd50191240522c40fd4415943588aa886a7cf9929d0fbfd49a0ae`  
		Last Modified: Wed, 02 Oct 2024 23:56:54 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251a34ff5c94cd380f6388f3e7381e3d7245f1a1ec520385345b46706764330c`  
		Last Modified: Wed, 02 Oct 2024 23:56:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7280a5f680011b35ff1e4b342327b4f773e22cfaf97380d3ca6dc50f9af1444f`  
		Last Modified: Wed, 02 Oct 2024 23:56:54 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
