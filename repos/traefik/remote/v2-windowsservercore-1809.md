## `traefik:v2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:e3b34785d194df551c5e1ba1593fd27f86f9e63d8d40bf857426dbbd22aaa407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `traefik:v2-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull traefik@sha256:b5832df9db3c0959859efd1782c845d6ae3e5d868012cbc3feab080984ad7014
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056711332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b776f2324d5f152ea25865fcb167f4f4d73481456b5640fbc328e3d20ec335f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:07:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:08:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.13/traefik_v2.11.13_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 14 Nov 2024 20:08:10 GMT
EXPOSE 80
# Thu, 14 Nov 2024 20:08:11 GMT
ENTRYPOINT ["/traefik"]
# Thu, 14 Nov 2024 20:08:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.13 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:236973c667e69c43db6b3386fbf123511b4e6bee9b5d5b799ffe0ff290e71957`  
		Last Modified: Thu, 14 Nov 2024 20:08:16 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae721cef1d420edc4b105d986ba15c37712c6f5f17210490c4010bc1e019889f`  
		Last Modified: Thu, 14 Nov 2024 20:08:22 GMT  
		Size: 46.1 MB (46052202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9989992dec1bc5705da68322602332edb200d5325f7ca5908b31774d2f0291`  
		Last Modified: Thu, 14 Nov 2024 20:08:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62987199bb4f0c8d5b66de07ae3b8524d6eaeb9a60a8db8c1035072f1aaf79ed`  
		Last Modified: Thu, 14 Nov 2024 20:08:16 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e412eb9a3b11cf62aa30bb314204549a1a7bbecdfa1d977020e1ae95e9b504b`  
		Last Modified: Thu, 14 Nov 2024 20:08:16 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
