## `traefik:saintnectaire-windowsservercore-1809`

```console
$ docker pull traefik@sha256:42313fbf9cc8a670aca52c252c44b61716269eb38116150f09ccc83b71bc82d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `traefik:saintnectaire-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull traefik@sha256:b921846c041f227dd38cbe23ced9d5d522656836f2b41b28ba11b851df1f7266
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2063897684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9588175a437b443639bfe7a2da7d68aadacb9f45585b2b8181f113cad8961c2`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Fri, 20 Dec 2024 21:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 20 Dec 2024 21:30:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.3.0-rc2/traefik_v3.3.0-rc2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 20 Dec 2024 21:30:10 GMT
EXPOSE 80
# Fri, 20 Dec 2024 21:30:11 GMT
ENTRYPOINT ["/traefik"]
# Fri, 20 Dec 2024 21:30:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:fa949ae480e0bc597dee7fb358f886d86ca2ecafc9f57a2703bf5b2b3d08073f`  
		Last Modified: Fri, 20 Dec 2024 21:30:15 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cf0f5594dfb5ca7211d03c741c6b1f7d92a82edb032344cd1f756ecdb4d42e`  
		Last Modified: Fri, 20 Dec 2024 21:30:21 GMT  
		Size: 49.7 MB (49722224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d428f7394bfe2858fd4b3129ae4ff7922ef42f5df5636818d9e50b042203deb2`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b084d3416956c96e21bd182338d3b1181f18e6c858d1e66b025c161a094c34df`  
		Last Modified: Fri, 20 Dec 2024 21:30:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ec4ef26c2d7302817bad4e7b3f81a5d69365088a284c9afa50aaaf08c884ff`  
		Last Modified: Fri, 20 Dec 2024 21:30:15 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
