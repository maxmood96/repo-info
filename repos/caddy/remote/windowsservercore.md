## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:0cc9e18409440159fbf2ac241bce180b0214fc5d2358aa87fedf1189394d7469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64
	-	windows version 10.0.14393.3986; amd64

### `caddy:windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull caddy@sha256:5b0edc0113282eff2b0b97cb2768aef9406975982b52b5801fe66a3b7e0f1f6b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2399991421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a3be7f6340286c7cad100a7baf86ff095c7d81ce5c10b5c314e8d7e73a9ade`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:03:47 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:03:48 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:04:19 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:04:20 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:04:21 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:04:22 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:04:23 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:04:24 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:04:25 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:04:26 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:04:27 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:04:28 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:04:29 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:04:30 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:04:46 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:04:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590b685e6f8e8fa4cbca8ce94e257baf1c179f183afabfc59bdff4420027e080`  
		Last Modified: Wed, 14 Oct 2020 21:13:24 GMT  
		Size: 9.2 MB (9237870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8a16e6bfc40544aeeaa55e8406570aec66018352db80098da3663138201f74`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468f02630a43054839d6262fe9f0d41cdd551ab83bbbb35c26cd9ead72ce6985`  
		Last Modified: Wed, 14 Oct 2020 21:13:25 GMT  
		Size: 16.3 MB (16343904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dcdb09f7b5a57cb7fce28be7e54975dfc770735e4570b259b9104ddc8421bbd`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4b2b1c53bbf344fa90b58a9d5ee4b990881289dde49074cecd1f0da649c20a`  
		Last Modified: Wed, 14 Oct 2020 21:13:20 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bade2ee2333f9cd004bd1812f0c1fc7f55b2297cf57b8343e17b48c9d3535`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b312fdc7f27df222f05918031d72e4457582b08c8fdeff7cde88a6a402b6f0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053d376e7f1eb8e50a394d7247f16006d36ae65144e75d37fe8bb0740d91695f`  
		Last Modified: Wed, 14 Oct 2020 21:13:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88dd9c5821fcba44cce1002ed12b8702e0cbec6ee8d137cbec8e5bd145acd5`  
		Last Modified: Wed, 14 Oct 2020 21:13:17 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca72f02c89a70e463873f7095a54263f02a7dc1fc35b8b3d92d0d6ed1114e1c3`  
		Last Modified: Wed, 14 Oct 2020 21:13:16 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744bfb9438a82d19472dbb92037ab018420b16a677b9451e9b92d13d9d4cc309`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab7908db3cd309e1cf3200fc5b51374d626702ea4ff411559cfa15da77b097d`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691b1b3fc24e5b473537703fcabf8cdc0acd56705ab671452b135de184ffbe0c`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba327018ef360de6c48ecbdb06f66a73defdb3996be6c2f17f0731514dbece5`  
		Last Modified: Wed, 14 Oct 2020 21:13:14 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c122dffbcf7af8877cc67b8f468cd74a76d63a739b85f3ac429fb27794f724`  
		Last Modified: Wed, 14 Oct 2020 21:13:13 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbf77f12be69367c8fcf09b53209ec5b25083762192120e9ed3f8e429569a4f`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c631d9175a05b1f8c784df5ccc0daeda8990f4cfa0faebc76e525dc737e034`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b5835866e9c4e5a927e7b41da88a4c61a54547cc83fc91db1c1a43494bbac2`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13669d36e52f3d6963333d5102e23ad22fd5892d4fd1a9468f12194c39c2753`  
		Last Modified: Wed, 14 Oct 2020 21:13:11 GMT  
		Size: 299.0 KB (299047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f0e09c2bd5ebc6729c8f1d852f4adefae35e2335cd7dbbcc09c95205e95ab0`  
		Last Modified: Wed, 14 Oct 2020 21:13:10 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull caddy@sha256:4c7f9ebc39d2e00064b805df702d5364f55de8cb8cf5ae58d8e4f438988069e8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5773083905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ce891f0605eaed2c51c683e9fe3d70f29bf6588b85b1f2be21dfcba2c4fb3`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 21:06:24 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 14 Oct 2020 21:06:25 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 14 Oct 2020 21:07:55 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 14 Oct 2020 21:07:57 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 14 Oct 2020 21:07:58 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 14 Oct 2020 21:07:59 GMT
VOLUME [c:/config]
# Wed, 14 Oct 2020 21:08:00 GMT
VOLUME [c:/data]
# Wed, 14 Oct 2020 21:08:01 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 14 Oct 2020 21:08:02 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 14 Oct 2020 21:08:03 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 14 Oct 2020 21:08:04 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 14 Oct 2020 21:08:05 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 14 Oct 2020 21:08:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 14 Oct 2020 21:08:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 80
# Wed, 14 Oct 2020 21:08:08 GMT
EXPOSE 443
# Wed, 14 Oct 2020 21:08:09 GMT
EXPOSE 2019
# Wed, 14 Oct 2020 21:08:53 GMT
RUN caddy version
# Wed, 14 Oct 2020 21:08:54 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b4a4f0660702b9f47920e1e7ea79666ac43584dadc8412d8a7b7eb0490a2c`  
		Last Modified: Wed, 14 Oct 2020 21:13:59 GMT  
		Size: 9.9 MB (9925104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3c401ae3441b3e5b7543d5482214980c1c14958e2713fee5966c2622a53963`  
		Last Modified: Wed, 14 Oct 2020 21:13:55 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffab013bf500710ef95125418f98138723e756c560a1de0145379662b77335db`  
		Last Modified: Wed, 14 Oct 2020 21:14:00 GMT  
		Size: 21.5 MB (21518510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf1f0773bd9f450a654eb5dcecd55e2e3fe3ba01eb0dae7dbf27e84402a6be`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077da12d3b43ef9b9dad1d8c770898c3a0224a8a0a3b99dc4656cc594d09b62`  
		Last Modified: Wed, 14 Oct 2020 21:13:53 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3976aabb2b169dd3bb85d39e2473fe70f7f15de0124b56095dd3c25fbbc27c`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5576c4d0eac332d8332455193ed1057c55aa90bd5e9a6bca884a25623c3c8`  
		Last Modified: Wed, 14 Oct 2020 21:13:52 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dc7c5fabd3bf6636614bc150a0965808e559f2b293340b4d8e049a185684`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7af1dab2b20db7484c30ac3175b1dc3b89884f843ece3209fdab4882f5e018`  
		Last Modified: Wed, 14 Oct 2020 21:13:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe18c02535b810df5a6916e6ffe0a4532c5a70dae17b5ce28956695be585480`  
		Last Modified: Wed, 14 Oct 2020 21:13:50 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1797af36c3af3ecc1e7db5ddfdba44c6bfff97b0515b3463d0948fed92ac4`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98a2d0f6d0934d8a3b866e68ca5e7775b2af52b170aa71f2113de2d32d532a3`  
		Last Modified: Wed, 14 Oct 2020 21:13:48 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f14b6955af73ac11170ddb2c596a1dd963ceafda86300b2de8466357d56aa4`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce0d3817eff364f0101431f28cb70cde3766120bbe5fb10b53ebf59363136f`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dd973289c284ff507f57773413c00c41a54ad2015bafb509c68a044b609cda`  
		Last Modified: Wed, 14 Oct 2020 21:13:47 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6c2b7b482e55dcb167623e29563231f659e1a523cb8f6e83423bb1d69a2014`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7811e07229200779f1a17a1899bf48c49f0250685f18fdffb38ee7c30ab779`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d7cb4258c8b7eab1c92df575a363d8685d8d783672e5256208f715c662b27b`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ab63ba04ec1b983074014465794ebf2e437ec4c03997ac40e1be3a4abcce61`  
		Last Modified: Wed, 14 Oct 2020 21:13:44 GMT  
		Size: 268.2 KB (268209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac54f9c3e58e5d406091c73dec798c29e2ee3134663b63d3ddb4959f10f4f32`  
		Last Modified: Wed, 14 Oct 2020 21:13:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
