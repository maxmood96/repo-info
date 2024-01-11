## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:f7e06b6f876505ed8ae83c339c860ab40d8287d52669bddf6dad0302470155d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull caddy@sha256:45db61c754ddd6e5ec06fd28a8099b51b78e0848a64f1b55a89da26731ef2579
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2085736435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d84e958273e9ab44607135820d1cb0a85c662765ec566b7fdfc82c7f819995`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 22:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:24:51 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 11 Jan 2024 00:24:52 GMT
ENV CADDY_VERSION=v2.7.6
# Thu, 11 Jan 2024 00:26:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 11 Jan 2024 00:26:10 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 11 Jan 2024 00:26:11 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 11 Jan 2024 00:26:12 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Thu, 11 Jan 2024 00:26:13 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 11 Jan 2024 00:26:13 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 11 Jan 2024 00:26:14 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 11 Jan 2024 00:26:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 11 Jan 2024 00:26:16 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 11 Jan 2024 00:26:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 11 Jan 2024 00:26:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 11 Jan 2024 00:26:18 GMT
EXPOSE 80
# Thu, 11 Jan 2024 00:26:19 GMT
EXPOSE 443
# Thu, 11 Jan 2024 00:26:20 GMT
EXPOSE 443/udp
# Thu, 11 Jan 2024 00:26:21 GMT
EXPOSE 2019
# Thu, 11 Jan 2024 00:27:18 GMT
RUN caddy version
# Thu, 11 Jan 2024 00:27:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8ac948dab7d4d3a44ab44e27a80115467b2f5fba68a58b377fef3e920bc5eb`  
		Last Modified: Thu, 11 Jan 2024 00:03:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628b34eba07214b21750eb21215539642fc79460ac44602f68367c8ef8f1876`  
		Last Modified: Thu, 11 Jan 2024 00:31:48 GMT  
		Size: 460.6 KB (460623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bba07c52b418ca922065149b75e4f078732301d850f6c6a857a0396fa758183`  
		Last Modified: Thu, 11 Jan 2024 00:31:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d43dbc97e7f70164392cf4e8ba36666c051180f2d9a5fa749c2ebd8f8902da`  
		Last Modified: Thu, 11 Jan 2024 00:31:50 GMT  
		Size: 15.3 MB (15274872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf65f149b526a7db12aa1cc0a82fee2c91e70e14004538422b70bf463f1e6a`  
		Last Modified: Thu, 11 Jan 2024 00:31:47 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0e80605ac50e370132adb19e7fbd35df1083f20a16f102ba838dcd1fbe6ddb`  
		Last Modified: Thu, 11 Jan 2024 00:31:46 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbf4dbf98c5ef756b92eec802352998cae9a7a53998309f4d23f3a25fe998ab`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5289b1119e5b6b3d21ecba38a21af08402723786c6a0d255d9656bab6fb0e45b`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4279deef6070878783847e2a97632c9e6c1c1f4ee240c4582cf8ff0f507a1f`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baca7c3ac198520fe83b18575029c9d68d6458b37234869602bf5a246f1cae49`  
		Last Modified: Thu, 11 Jan 2024 00:31:45 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc6cdf36ba1ce7eb637a46f998fd84b12e02b76b737244ac8f6a5a61a2f6d65`  
		Last Modified: Thu, 11 Jan 2024 00:31:44 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0870a17942cc9d0cbbffa15ab03f6401c95d37ab9fd965e63cb8267dfb6a4d5`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97548b26d83c7392114297bcfdbf85c8fdf5f812fea56a4c355e28a0f063454e`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824baecd8144b0da5828335f980e72f9721a3ac35dbda7f8927ef4e1dc4fdf0f`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe4e2c9f762e3bacef96b2394563066a0e8f4b62d3dea44e8a8d6c1a661ac86`  
		Last Modified: Thu, 11 Jan 2024 00:31:43 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f434e7a3223202b5c62896b0b513f7ac33068974c4a3a87c2c13dd95dda313`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41470b117bd27755279ab256ba0156bf64796a6fcd06cc26ac6d1e617387d4a0`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e389ce50002f8ac47cbbe67517402ca31e7fc2e99945faf3cf392848560faaa8`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0990eeef88a51462c1b1e6a7044d57c8b6976e099844570344699067f387a3`  
		Last Modified: Thu, 11 Jan 2024 00:31:42 GMT  
		Size: 254.6 KB (254599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b1fd2b9188ec5f76a81bfc4d7aa53b000672e101a91e51a5df9ab4cfcc2a8c`  
		Last Modified: Thu, 11 Jan 2024 00:31:41 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
