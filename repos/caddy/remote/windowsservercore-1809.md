## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:89299b443724d4b0e89af13958b82e2d8fc4185f2a5a8dbfb83a284bab6f5b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull caddy@sha256:dad45b6df45cf6f4c45f010c391544a830a6372847bb2504a23a870eb9e96638
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2413941176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f3df5163746a4530d03a8bc80f3b1318d935f9f1b3e26f00a31af891a9ba86`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 20:53:30 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/56302336e0bb7c8c5dff34cbcb1d833791478226/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 11 Nov 2020 20:53:31 GMT
ENV CADDY_VERSION=v2.2.1
# Wed, 11 Nov 2020 20:54:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.2.1/caddy_2.2.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e5c5fba6af33a0e1b48cbabc106e907dc7171c2cc337ee5c7cbbad07587dc4970c3f49812b3938dee43209b7fe293c74b36274fd809730ecec0041dd6b1fa93d')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 11 Nov 2020 20:54:04 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 11 Nov 2020 20:54:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 11 Nov 2020 20:54:05 GMT
VOLUME [c:/config]
# Wed, 11 Nov 2020 20:54:06 GMT
VOLUME [c:/data]
# Wed, 11 Nov 2020 20:54:07 GMT
LABEL org.opencontainers.image.version=v2.2.1
# Wed, 11 Nov 2020 20:54:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Nov 2020 20:54:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Nov 2020 20:54:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Nov 2020 20:54:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Nov 2020 20:54:11 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Nov 2020 20:54:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Nov 2020 20:54:12 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Nov 2020 20:54:13 GMT
EXPOSE 80
# Wed, 11 Nov 2020 20:54:14 GMT
EXPOSE 443
# Wed, 11 Nov 2020 20:54:14 GMT
EXPOSE 2019
# Wed, 11 Nov 2020 20:54:30 GMT
RUN caddy version
# Wed, 11 Nov 2020 20:54:31 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dcdd0030882c54a82d0a279a4099081c604810ccccb17d3d7c04a2057bf657`  
		Last Modified: Wed, 11 Nov 2020 21:02:39 GMT  
		Size: 9.2 MB (9248045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3be730f5a5cc9d1dd7080908242b9ed33ba6541e7120addf14e416b944b577`  
		Last Modified: Wed, 11 Nov 2020 21:02:36 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d70ac9fb0285fe6670a558e9c1da67b5594dd483872376ac91425a3058f95b9`  
		Last Modified: Wed, 11 Nov 2020 21:02:54 GMT  
		Size: 16.3 MB (16343997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72340d1f03d76debdf2a014ab06bbd3bc5cb1e8358520912f0c9f71f2b4a6ea`  
		Last Modified: Wed, 11 Nov 2020 21:02:34 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ae7bc4f9eb3af2fa576dd096f9992ad2cfc8a2e9aad0af79e1ebf11c95065d`  
		Last Modified: Wed, 11 Nov 2020 21:02:33 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46832c7bcb0b053968836644798024f37cfede18aaac00abed0c1571fbeeca4c`  
		Last Modified: Wed, 11 Nov 2020 21:02:33 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdafb0d35a00870fdb93efde60b2d5c002b5ec117bb07526ec1d744787529f58`  
		Last Modified: Wed, 11 Nov 2020 21:02:31 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af235cb3a2a159b44c6b773e30cbd6f7931055fb7cfed2aee403c9197e0defc`  
		Last Modified: Wed, 11 Nov 2020 21:02:32 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493ee2907458eb7d47b217b59e2f23b4dd4a6974a36a70462fa54e5b9201f26b`  
		Last Modified: Wed, 11 Nov 2020 21:02:31 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2f8b9a7de64bd747e2afbc20e6ca964b00d3b48ccdb9245e162300a5ef9b44`  
		Last Modified: Wed, 11 Nov 2020 21:02:28 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc59b5cb8ee3554d8e4971222e0208e7b6dd831b33894abeba76400bbcb7d56`  
		Last Modified: Wed, 11 Nov 2020 21:02:28 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c88104f4e1fc6125880b248f3e1edcc5cbf3daf73aaf26bf3782972f11203c3`  
		Last Modified: Wed, 11 Nov 2020 21:02:30 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7cb21eb1cd8ca039940f462fdfe3348c877262adbbc5891cdbc3601ffa2649`  
		Last Modified: Wed, 11 Nov 2020 21:02:27 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef21802812d7f9ad5dcebb2efbf8d4831fcdf5b024bac00c22d04e7406a420b`  
		Last Modified: Wed, 11 Nov 2020 21:02:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed806482965bf605e395b83f00ba44639cc1c88b1b8ec7c75bb708d9c031610`  
		Last Modified: Wed, 11 Nov 2020 21:02:24 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee097b51db8b06f6e93d48da3e914d6a598b32681fdf27785279f3f5dbb5796`  
		Last Modified: Wed, 11 Nov 2020 21:02:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf5349d69a690d25aa14a10fab1fc6e7a82ec345bae9e1a01a4dfd95f09cd1b`  
		Last Modified: Wed, 11 Nov 2020 21:02:22 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0b5aa8db0e75c1ef349905a29ef299882814b7937d14753d2e6a972f7b13b1`  
		Last Modified: Wed, 11 Nov 2020 21:02:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cac55d84f022bb91b78bfb339492198e3fa96a7d1e25c1f8e09ad648376d45d`  
		Last Modified: Wed, 11 Nov 2020 21:02:21 GMT  
		Size: 299.3 KB (299301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7476d855c257a4a27ce525860567dd9bd67e74abb01c0fd1b334444ffaa8504c`  
		Last Modified: Wed, 11 Nov 2020 21:02:24 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
