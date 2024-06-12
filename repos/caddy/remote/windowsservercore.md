## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:293f27633b2835bd4c5ac0194808147482ed154a9102cdb8a0329fb32b29f8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2527; amd64

```console
$ docker pull caddy@sha256:51147c928efe77a4b4099cc27d06e7db18a5721176cec3e20105fa142c09b25f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2134147349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560d413e8be5e8e31f17540371afc251b4e57a43c55063617d40892e4473e898`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:05:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:05:56 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Jun 2024 18:05:57 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 18:06:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Jun 2024 18:06:08 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Jun 2024 18:06:09 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Jun 2024 18:06:10 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 12 Jun 2024 18:06:11 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Jun 2024 18:06:12 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Jun 2024 18:06:13 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Jun 2024 18:06:14 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Jun 2024 18:06:15 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Jun 2024 18:06:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Jun 2024 18:06:17 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Jun 2024 18:06:17 GMT
EXPOSE 80
# Wed, 12 Jun 2024 18:06:18 GMT
EXPOSE 443
# Wed, 12 Jun 2024 18:06:19 GMT
EXPOSE 443/udp
# Wed, 12 Jun 2024 18:06:20 GMT
EXPOSE 2019
# Wed, 12 Jun 2024 18:06:25 GMT
RUN caddy version
# Wed, 12 Jun 2024 18:06:26 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e545a2fc5d3075adc1d6a745e6b2672175e0edb524c41741a015287407c7cf`  
		Last Modified: Wed, 12 Jun 2024 18:06:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5722a8f2906463d5d6778f51a612a3ffbf427a41451e46844f664f0c9b994f4`  
		Last Modified: Wed, 12 Jun 2024 18:06:38 GMT  
		Size: 357.8 KB (357844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f62cb99602a812ea5ca60f8dd34b8a72c163c7f5943990bf844c94439b09fe8`  
		Last Modified: Wed, 12 Jun 2024 18:06:37 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86705d66327fb336a3dc0795058217a72a83959f56078c243bfc567de39ec9c6`  
		Last Modified: Wed, 12 Jun 2024 18:06:39 GMT  
		Size: 15.3 MB (15251871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee45ca65f4b3ff2e1f52cd7fde719a06fbfff1d0836be6ebe0bdaa6d0e745aa`  
		Last Modified: Wed, 12 Jun 2024 18:06:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a739cfe2c04e879f40533d04fba63f9fd68ace6361ba73ba2effcac3bafa690`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a29797e301bc36a0546ef4e042054bf93256cb3888578aca83e018bc77368b`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988d07a5554acc0d603c5e058d487da8edc7ebfe95eb1232f07ab7ea0366280`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ef2c93189ec1bc02ecce2f44a4bf9a255a7f320782e6340eea391895f3f303`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb0ade3e94278b0df4f52923ad65406d5fc4a000aa97049fe7db8387c6e6076`  
		Last Modified: Wed, 12 Jun 2024 18:06:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aa98437e0f860e5163d5a8368019dc14dd3fb53a791c27738dc4b7a16a0b13`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eaecae7891029f0ee7757e03a7b4b74cabb083fdb028d17cc43ee464829794`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf00901eaa304c584a21dbe8a70c3b80a6b0c6fde285f57db9c47d1f4d66f30`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09121d08b868a076afba48cc26857cdc4410e5fbab4452d138a5ba00e10c8a61`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095968204cbc805ee64ab0fac270bd2ed576ea57cbd7a82b338ebbe689d31538`  
		Last Modified: Wed, 12 Jun 2024 18:06:33 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672972d9699e689d8896c7a21c5dfaa9ee3a2b58b871a9df0c18e56b7f4ff08`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f435a4624de5ceec43b71f0c3e6372a1ab64e41e906b8fa18483115027e98d3`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf1139230913bc0093c2a4c3328ca2de4798f7246b53faab1f5f52dfea039c3`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad623230e152a65511f5223dbfc568f8236a7857f4b4d15edf79c0a7181a780`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 337.1 KB (337086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91574d61749f6b283be1b9468a9fb0b557b1872546a8b307275bcc8dca2c912e`  
		Last Modified: Wed, 12 Jun 2024 18:06:31 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull caddy@sha256:a5c00013b5cfa9cd49996e182bd9f5a85abed2a8d0d74f1dc61bde309ee3cfcd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2236778768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e90a84406eff7717cfb437b2d988f4c7f58f428f885806782315bcf6942141`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:14:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:15:50 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Jun 2024 18:15:50 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 18:16:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Jun 2024 18:16:13 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Jun 2024 18:16:14 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Jun 2024 18:16:15 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 12 Jun 2024 18:16:15 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Jun 2024 18:16:16 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Jun 2024 18:16:17 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Jun 2024 18:16:18 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Jun 2024 18:16:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Jun 2024 18:16:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Jun 2024 18:16:20 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Jun 2024 18:16:20 GMT
EXPOSE 80
# Wed, 12 Jun 2024 18:16:21 GMT
EXPOSE 443
# Wed, 12 Jun 2024 18:16:21 GMT
EXPOSE 443/udp
# Wed, 12 Jun 2024 18:16:22 GMT
EXPOSE 2019
# Wed, 12 Jun 2024 18:16:39 GMT
RUN caddy version
# Wed, 12 Jun 2024 18:16:39 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e451e2214cb46d91701a5efdeec888aa7d4bb1abd886b3ea1ab94b6f5c77434`  
		Last Modified: Wed, 12 Jun 2024 18:16:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385a5d9b53c9cd647493df39a9e4f81260cf4cfd352c829b59120980dbda419`  
		Last Modified: Wed, 12 Jun 2024 18:16:45 GMT  
		Size: 486.0 KB (486040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fee2e008257210ce03b0310c3fd46ad00de102869b57f0c49d72b851b5e1cff`  
		Last Modified: Wed, 12 Jun 2024 18:16:45 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a1730fab799de2f3376ad39d417775e7d729f9eab97fb0ee5807e57f82b57f`  
		Last Modified: Wed, 12 Jun 2024 18:16:46 GMT  
		Size: 15.3 MB (15253086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c97e474161736db0a5fa6376934e5f1a87063b5a6b5c29a1538e57d31f2d5d`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351ff70de2baa55d09f0fd436e5796ce05ac94304b5a49adaf5356738bcdb3eb`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505357b6cd3601e73aa7b4bea94c23fae309eca2582315471ec7a37f40ccd097`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d13d827172c8dd1a368ba470e93fcac50603791ad749be0b000394b2a6cc9d`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815a80b170874260ad13f80b080aea2b92f8b70e0d700f7df5c6152d6e5073d3`  
		Last Modified: Wed, 12 Jun 2024 18:16:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e67694cd431f519e9a418acf8118968562ce07d38bd1cc6a8c23c0e6b3855c`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c65a7507f079159e33c8113457614026bef357e6c79e264edf07ac5ec619212`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231d80673520560b892fd3c9af92d9762023cf7ba67240380ca0ad8480e4761e`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96693e4ec5c88c00f528b2e4cc30a6d25825d886b4f6cc8533ca34d772028262`  
		Last Modified: Wed, 12 Jun 2024 18:16:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60bb90d75c3d81b23efab09d3ff3a10b79c44ce139cad2e8c16b3981c37df3f`  
		Last Modified: Wed, 12 Jun 2024 18:16:42 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37f4729482dc6a862c6da3ad00f05b6ee5819cb96c72fe579a3f347231c68cd`  
		Last Modified: Wed, 12 Jun 2024 18:16:43 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab02387e2baa16a12f15698e549a0767d32017af6314c0f6971ca06845a744f`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb07b0c0cca090fa9ab548d7b5bf0809605f6d7938939e2e50757041425e94`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289563f0fb9ba9caf2a30b6a7fd4221f28071a6ad712056531bb8e32b8cd1695`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcda06e9916af1f402738739c5ae633f9b3adc283ca2dd8772744d857b0867f`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 336.4 KB (336380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ec8747b8e7791d503f3e814ec490ec965b506aa5d9b24f319e43bd0f16a0b9`  
		Last Modified: Wed, 12 Jun 2024 18:16:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
