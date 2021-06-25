## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:e1c2343f4871a27fd0813dc571b2532a0b598e983d818dd30a7ba8d7eb6dff66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull caddy@sha256:fecf68d5734e6ad573d3e14fb998b94d3cdc851aa9acdf7cfff05dcc4bf75f35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2654297410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc381081eb2bc174e6f28a149fe58f65a2f53aada33d380ac42d6f4b367917c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 20:08:05 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 24 Jun 2021 19:15:09 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:15:51 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 24 Jun 2021 19:15:54 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 24 Jun 2021 19:15:56 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 24 Jun 2021 19:15:59 GMT
VOLUME [c:/config]
# Thu, 24 Jun 2021 19:16:01 GMT
VOLUME [c:/data]
# Thu, 24 Jun 2021 19:16:04 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:16:06 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:16:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:16:12 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:16:15 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:16:19 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:16:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:16:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:16:27 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:16:29 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:16:32 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:16:50 GMT
RUN caddy version
# Thu, 24 Jun 2021 19:16:53 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dc18d712eacfb666370e311daaf51e09fc2f76ca762e4592e149fbe6aba561`  
		Last Modified: Wed, 09 Jun 2021 20:19:34 GMT  
		Size: 361.4 KB (361380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e527cc0fb36e8f714f031d5eff029a55226e17552f7b813f4796ca242f1f8d9e`  
		Last Modified: Thu, 24 Jun 2021 19:23:22 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2fc4c750e6b97556947872ba4fe4fccac36ff1afb3073cde64759dfa4b1d8b`  
		Last Modified: Thu, 24 Jun 2021 19:23:36 GMT  
		Size: 12.0 MB (12025081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2369a8bbd41fbf46414df953a4fad059a4abbeb103f8c1939c203f2524575`  
		Last Modified: Thu, 24 Jun 2021 19:23:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cc23dc985d29fb96faf1e17031a84e8493e3e9a1eccadff1b3620bc2faa9f5`  
		Last Modified: Thu, 24 Jun 2021 19:23:22 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4db5b593c181acd67fc7b9afbd2d2d044153ebca82d90fc4e32b1f2e64737b`  
		Last Modified: Thu, 24 Jun 2021 19:23:20 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a75107b0764df2164c5d9dde0d895467a87df21692a6b6a19fb28768d4d764b`  
		Last Modified: Thu, 24 Jun 2021 19:23:20 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a082f4ce7cb474ade55964de90c6f7865a82bd1bb40479c9cfe627dd8aa7372e`  
		Last Modified: Thu, 24 Jun 2021 19:23:19 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd9a94966603c59995cac8e0587949c2e0bf885e0731842d9b800a89fc34484`  
		Last Modified: Thu, 24 Jun 2021 19:23:19 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a3b017e753cd0d0dfb38d9905b76636405e6dc7399acc5054f536a19503477`  
		Last Modified: Thu, 24 Jun 2021 19:23:19 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a92126da0acc1b8651b87a0832b3c45f1ee5e845903e9b43090e7fd4a61f625`  
		Last Modified: Thu, 24 Jun 2021 19:23:17 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7883e71cdd44a6deae7c8c0d556c480008e7daf17689f18440e6c253d79e45`  
		Last Modified: Thu, 24 Jun 2021 19:23:17 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab4cc839f18f02ae818ac338a8401f91f991ea293bd214e472b4b8d19b5bbaf`  
		Last Modified: Thu, 24 Jun 2021 19:23:17 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5eacf33ecf3614f9c66cac3346b235351ec870bc3cd415b14a06141ae15def`  
		Last Modified: Thu, 24 Jun 2021 19:23:17 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b866478e8e53c0ac5f3302e5ce54d04bdcbeab445f8721ade54dac1bc31ee305`  
		Last Modified: Thu, 24 Jun 2021 19:23:17 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0124d4afc4bfbd9d1a08aa00e98a0c15f5dc09ef661e1bdf73926abb0005e9e`  
		Last Modified: Thu, 24 Jun 2021 19:23:14 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ea4b04297845308fd5914e374d36f5d97c6f34b218ac03004a869bb5a939b8`  
		Last Modified: Thu, 24 Jun 2021 19:23:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7abc4a3c4cc44b8c42becc8df13e5b52c85e4f8707b1241597dc84fd7d9985f`  
		Last Modified: Thu, 24 Jun 2021 19:23:14 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dc50a050c92c09afac4ce4bc1c3f5d03119afbad8b5d6630b1c816400caf1b`  
		Last Modified: Thu, 24 Jun 2021 19:23:14 GMT  
		Size: 300.3 KB (300264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b238bdf7f4fcbe8caefbbf7fbe5e1ef1c7f736e36ce5c0221354d3c3ed6f5e`  
		Last Modified: Thu, 24 Jun 2021 19:23:14 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
