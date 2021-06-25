## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:05ac90ff29822b86eb2c0c6c2e30358ec05c08d29379774f144246e7a6d891e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4467; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.4467; amd64

```console
$ docker pull caddy@sha256:8279cd4dcd079817fecabb5de589a5a5f18a769b13baebd169d088bfc9deb05b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6278388412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b125af4b52605c361c305f3a95784798803aebd988047e9bf1ca92baaf8633`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sun, 06 Jun 2021 15:37:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Jun 2021 12:41:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 20:11:27 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/a8ef04588bf34a9523b76794d601c6e9cb8e31d3/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 24 Jun 2021 19:17:06 GMT
ENV CADDY_VERSION=v2.4.3
# Thu, 24 Jun 2021 19:18:34 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.3/caddy_2.4.3_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e4b392d1384a02863f93c0e183c50a2b28a19ccf468c186fa1524b041895c237dbb88b0dd20c13d187779c0b5f5789458c84ffbc17cd628a9fd05779eb418563')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 24 Jun 2021 19:18:37 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 24 Jun 2021 19:18:40 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 24 Jun 2021 19:18:42 GMT
VOLUME [c:/config]
# Thu, 24 Jun 2021 19:18:44 GMT
VOLUME [c:/data]
# Thu, 24 Jun 2021 19:18:47 GMT
LABEL org.opencontainers.image.version=v2.4.3
# Thu, 24 Jun 2021 19:18:49 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 24 Jun 2021 19:18:52 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 24 Jun 2021 19:18:54 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 24 Jun 2021 19:18:57 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 24 Jun 2021 19:18:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 24 Jun 2021 19:19:00 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 24 Jun 2021 19:19:03 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 24 Jun 2021 19:19:05 GMT
EXPOSE 80
# Thu, 24 Jun 2021 19:19:08 GMT
EXPOSE 443
# Thu, 24 Jun 2021 19:19:11 GMT
EXPOSE 2019
# Thu, 24 Jun 2021 19:20:03 GMT
RUN caddy version
# Thu, 24 Jun 2021 19:20:05 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2f52abeee6d6f4a925ad418b5e6200d4fca9bf92834ffc918b8bbaccd34251db`  
		Size: 2.2 GB (2195741359 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c82e82e95dbad4ccc260b42e03767eb07222e2f00ec57a69b3c87b17da1d2fd3`  
		Last Modified: Wed, 09 Jun 2021 13:04:25 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a28e390d3b8e7b9369b102914eaee6e1fa0d14eb258b628be67f99f32f06f81`  
		Last Modified: Wed, 09 Jun 2021 20:20:01 GMT  
		Size: 357.4 KB (357370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec323c1b5d0b0ba3004a22eb86ff12adefd297b215652d320e4c5191429d44b0`  
		Last Modified: Thu, 24 Jun 2021 19:24:00 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e20ba3c9dfb401e9be6826d7971a90801ad534c25f3e7737800a61017b5b18a`  
		Last Modified: Thu, 24 Jun 2021 19:24:03 GMT  
		Size: 12.0 MB (12005053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768d2350e71354a251fdd9bf19f98f017f78e529d967eba82be6edfdfc7922a1`  
		Last Modified: Thu, 24 Jun 2021 19:24:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039e01598368df3c30c1e9dacb4afd475530550e09b63bb37be6f846831c5250`  
		Last Modified: Thu, 24 Jun 2021 19:24:00 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e12adfa3492bbc932b4993711e2c65f4caaf5bbb2d47b79979cde057ff6be6`  
		Last Modified: Thu, 24 Jun 2021 19:23:59 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0708179bfa829817469f835f868581e8626780fad67c949085d4c85c41e84265`  
		Last Modified: Thu, 24 Jun 2021 19:23:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aec8453dedcca8395b15ba368c79f3b434e928c68c7ebdd3322fed90be9b77e`  
		Last Modified: Thu, 24 Jun 2021 19:23:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23b0179fc7ec0af1fcc436313bc8fd3cb33600b8930c0cab88b07246a294be1`  
		Last Modified: Thu, 24 Jun 2021 19:23:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fc213275edc2074c6f079ecfeb86fe3f77e457859b06a5538d90474805d652`  
		Last Modified: Thu, 24 Jun 2021 19:23:58 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1053eb56c7e3c5610256b30d660a56bd93d275bab87e17a2d194e2883b3cf0e3`  
		Last Modified: Thu, 24 Jun 2021 19:23:56 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f686f33f63c97fd02546c6731b567b7181ee10e39daae5a692461346221d9c`  
		Last Modified: Thu, 24 Jun 2021 19:23:55 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4155172212b2a3a1b7fbe54cafa33eddec909e04e4675b7c38da637296cbc8cb`  
		Last Modified: Thu, 24 Jun 2021 19:23:55 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266dee6ad0435eeda42d56b6d18c56226a2c4f19e5e93e0f6f70a8029e5ffc85`  
		Last Modified: Thu, 24 Jun 2021 19:23:55 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ad107be83c2cbb5e9ad7642a0221d46c349c56c1f105480ebddfbeba7f55a6`  
		Last Modified: Thu, 24 Jun 2021 19:23:55 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825600d9693ca1e85a014169ad6c2f7065483f82fbf1eb61f6a225b254869393`  
		Last Modified: Thu, 24 Jun 2021 19:23:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1478c221a7ac6a17612e59ff5e085aeb72b7756ae0a6ec9ccbec4f47ad47c660`  
		Last Modified: Thu, 24 Jun 2021 19:23:52 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad9324d6459b5cb0ac5f620058c6bad613ef32d6895ae54fb26248a9cdb8964`  
		Last Modified: Thu, 24 Jun 2021 19:23:52 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9c49ee8ad149d6b7ed184eee36b8f2a2b8c65491fd509ec60dae53dc3289e7`  
		Last Modified: Thu, 24 Jun 2021 19:23:52 GMT  
		Size: 273.1 KB (273145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9d1ad81affeed6dc47e739c91716c91ba0b3bda44b11c6b77ba9f8619690`  
		Last Modified: Thu, 24 Jun 2021 19:23:53 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
