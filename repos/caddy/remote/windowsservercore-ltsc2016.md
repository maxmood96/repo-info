## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:b399e4134eac2ed1e68a9f6d12fa6c2f89351edd4b13f45e687d84ee2c8c7891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull caddy@sha256:2c091f3638b3d3948ffa8c2d95a9be662e858768ffc52e366872371a68d003a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6285957464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb2d13bfaf3ee5703b28aa6d939cbfac5b14658e1e3e91bbae594e1c4b22a2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:15:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Nov 2021 20:15:35 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 10 Nov 2021 20:16:38 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Nov 2021 20:16:39 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Nov 2021 20:16:40 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Nov 2021 20:16:41 GMT
VOLUME [c:/config]
# Wed, 10 Nov 2021 20:16:42 GMT
VOLUME [c:/data]
# Wed, 10 Nov 2021 20:16:43 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 10 Nov 2021 20:16:44 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Nov 2021 20:16:45 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Nov 2021 20:16:46 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Nov 2021 20:16:47 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Nov 2021 20:16:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Nov 2021 20:16:49 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Nov 2021 20:16:50 GMT
EXPOSE 80
# Wed, 10 Nov 2021 20:16:51 GMT
EXPOSE 443
# Wed, 10 Nov 2021 20:16:52 GMT
EXPOSE 2019
# Wed, 10 Nov 2021 20:17:30 GMT
RUN caddy version
# Wed, 10 Nov 2021 20:17:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224cfcc2d1317d73465188f71867febbba9a64bbfcdf83b35bccd662bdb25748`  
		Last Modified: Wed, 10 Nov 2021 20:21:11 GMT  
		Size: 366.8 KB (366836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98f673e7fe75a29f4060341dab79e20ad059162395f10fb1fc2504379d12f22`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dc3d9f8e8e85985894d372a912cae2cbc64cc10540262498597bbe8cad8c31`  
		Last Modified: Wed, 10 Nov 2021 20:21:24 GMT  
		Size: 12.2 MB (12158174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197a3f340985e5e76e3ae77fcbb9e208f521abbad0cfb8921d27d4afe569f280`  
		Last Modified: Wed, 10 Nov 2021 20:21:13 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1443a981044b58af1bae85624fffe4dde7c1759e6a5f930ddaf2eb70bc3185dd`  
		Last Modified: Wed, 10 Nov 2021 20:21:10 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1b023614dd84860e7a4fdd1855131b5478b9b747a40fc9383467934e48e310`  
		Last Modified: Wed, 10 Nov 2021 20:21:09 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca4ab6367b318ae3a2df27bbe0c53c12ee1a0196fc4f43a43ec47acd74c7c`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a288866cea4075f0f825973ce9d3369dd9411f73c325ed870a5233b383476dbc`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea1c63b1b4cb8f39b59025d926f384679d17bb660eceafe7f7c9418dcdfad61`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25f60f98964a2d03947e1dac0b01388ad6c9c65497e546f8efe7f2fdcd35e`  
		Last Modified: Wed, 10 Nov 2021 20:21:08 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10f21fe32d5dd37a74db003c1119b2aaba639690b10ad4c46d22e2699140fc`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4bd5845100c889806835753480fb0016610fbfab35d197c6aa641d73c114ed`  
		Last Modified: Wed, 10 Nov 2021 20:21:06 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190767770423c20b77f963553559cfa26d18b490228ad11c4f9fcf62e6dcefd7`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab0412df33f87a4e77ce1ef8afc68a04cd9a9a56ce9a21e3494f4e4f7c1083a`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80edcc113a751c789aee343b18fdb12c9099cd642cf099ab6a962c7cb0bce8b`  
		Last Modified: Wed, 10 Nov 2021 20:21:05 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d513b74afabeb0e8050ca955cdf8b72040cabc21350ab394862808bd4382649`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc99c5e78f676bc2fed853c2d43f71dedcbf29fe3a6f69f5d0bc1eabca7f8e98`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1532dfe2f3d7f9a4d2eed5ac842a7b54e160fb4d856388e1153d0c6488bab749`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c6594f3623b09c0359fe4347b1981678cebb55cebad4bd683d4bc059e0a201`  
		Last Modified: Wed, 10 Nov 2021 20:21:04 GMT  
		Size: 316.3 KB (316295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c07c5e836014edc4e052889ecbe945aa470b434f2563726bd4f9684da37bfc1`  
		Last Modified: Wed, 10 Nov 2021 20:21:03 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
