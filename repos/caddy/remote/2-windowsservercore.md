## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:378b443107c1e6d8d57d7ba4bd96ac7eb9280f2e13984bcf7a478c7e54afb3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull caddy@sha256:0cfc2817cd8612ae9a6740b3278832ff16864f6e5ec34c9e73009c155de01f57
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2286722812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d91c450d10d40b10ff05bd9b82bca084eb58a68424f9822d229057ab1a20b1c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:52:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:52:50 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Apr 2025 00:52:51 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 09 Apr 2025 00:53:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Apr 2025 00:53:01 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Apr 2025 00:53:01 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Apr 2025 00:53:02 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 09 Apr 2025 00:53:03 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Apr 2025 00:53:03 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Apr 2025 00:53:04 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Apr 2025 00:53:05 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Apr 2025 00:53:06 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Apr 2025 00:53:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Apr 2025 00:53:07 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Apr 2025 00:53:08 GMT
EXPOSE 80
# Wed, 09 Apr 2025 00:53:08 GMT
EXPOSE 443
# Wed, 09 Apr 2025 00:53:09 GMT
EXPOSE 443/udp
# Wed, 09 Apr 2025 00:53:10 GMT
EXPOSE 2019
# Wed, 09 Apr 2025 00:53:15 GMT
RUN caddy version
# Wed, 09 Apr 2025 00:53:16 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766cfcc1f117561cff5f7e27486f135d5441d9d3f9c2ab8ae50d97926ed2cb6c`  
		Last Modified: Wed, 09 Apr 2025 00:53:22 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a7cd8bd32ba36ffcc78bdc0570810437c537938592ecbdf0257bbcaa098c47`  
		Last Modified: Wed, 09 Apr 2025 00:53:22 GMT  
		Size: 357.5 KB (357542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2772f09d163a3194d66e8ce9f01c6c50404867c408bb66c416d19e22c22dc8aa`  
		Last Modified: Wed, 09 Apr 2025 00:53:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da74b381ac5aa8b705aec03b6c6bd5edbe7a97d880baa43e17ad9143390c71f8`  
		Last Modified: Wed, 09 Apr 2025 00:53:24 GMT  
		Size: 15.0 MB (15008481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfd0a1e30ca9c4d401d93281e641f176987f219d12cbe38d3b62ec14d837867`  
		Last Modified: Wed, 09 Apr 2025 00:53:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fbb2a000a415d26ea3dc68305499771798972f25eb26132449542cebcadc9f`  
		Last Modified: Wed, 09 Apr 2025 00:53:20 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b726cb47db346c1305ba332591603135b627c6478564ec080c88b6bd2ef7463`  
		Last Modified: Wed, 09 Apr 2025 00:53:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e5170da5880fbabb3c14d3e64d8d742e799285ebd8180b58c78ca6f6c2163`  
		Last Modified: Wed, 09 Apr 2025 00:53:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d366f298af0b289ab940ebc0cfe4fab14f72ddaf97085c377f8673c662ec75`  
		Last Modified: Wed, 09 Apr 2025 00:53:20 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc91eabc8cb599338ed3dada4b531ebd00a9569608e0cd69435b012cc27da389`  
		Last Modified: Wed, 09 Apr 2025 00:53:20 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9f02da5aaefc3cb11c907f2ce2e5f2ddd133a3c542c3bf18040e01cca50623`  
		Last Modified: Wed, 09 Apr 2025 00:53:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d767d4dcb892c50c75b91f535ce0457db48e9aa0e2d5bf4c7f64fd5800de7ea`  
		Last Modified: Wed, 09 Apr 2025 00:53:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863f9b72687764ac36ce3fd994cab344b5d70c8f4dfc334ad5ca2110db342554`  
		Last Modified: Wed, 09 Apr 2025 00:53:19 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a21636bb838d0cfcb5438bfefdc86b4596cea5ec1e0ff3bbfbed8e3ca1a24d3`  
		Last Modified: Wed, 09 Apr 2025 00:53:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149a8525d8a8a32ed1c3acc5d5667ed9fbb2f735d9f0025cc1cbf328c2645f4e`  
		Last Modified: Wed, 09 Apr 2025 00:53:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8b60b9bb646e3d1c0b3f338be6b13c231e6aee1234cd8135a47005b8d6a9a6`  
		Last Modified: Wed, 09 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5fd2157114f360ee604c87b5069ada8ba042563f248059ce9e5340d10707e0`  
		Last Modified: Wed, 09 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae94408966245ab9da7e8f517cf09aea94e8f979952d5a3c1828c09ca2539b64`  
		Last Modified: Wed, 09 Apr 2025 00:53:18 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b3b51dcd1f123363b2cc05586cad9867ed664716b87733bad26fd6dfdd79bf`  
		Last Modified: Wed, 09 Apr 2025 00:53:18 GMT  
		Size: 339.1 KB (339131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d41dc532a4d26d16a7294594540c031cb26ce97a68af6074c5ad66d539bfa2`  
		Last Modified: Wed, 09 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull caddy@sha256:fcd7b0c701fd0b2e28ad58ddb03c7b05dd089f697e5cfba9147891689cd30e7e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167335537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49538e47b959210c49da9cebcb6f0213eb7dcf03dc9fe3183b676ec2fa8713aa`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:46:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:12 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 12 Mar 2025 18:47:13 GMT
ENV CADDY_VERSION=v2.9.1
# Wed, 12 Mar 2025 18:47:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.9.1/caddy_2.9.1_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4f0f85b42015ff2276d08705751472e6a98bdc7fda5ec76dd41b7a0c16fee90af012f1a7beb226164408cfbe656bd3453ed5ccbb596f80c45d0fa1c749fc8da2')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 12 Mar 2025 18:47:24 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 12 Mar 2025 18:47:25 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 12 Mar 2025 18:47:26 GMT
LABEL org.opencontainers.image.version=v2.9.1
# Wed, 12 Mar 2025 18:47:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 12 Mar 2025 18:47:27 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 12 Mar 2025 18:47:28 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 12 Mar 2025 18:47:29 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 12 Mar 2025 18:47:29 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 12 Mar 2025 18:47:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 12 Mar 2025 18:47:31 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 12 Mar 2025 18:47:32 GMT
EXPOSE 80
# Wed, 12 Mar 2025 18:47:33 GMT
EXPOSE 443
# Wed, 12 Mar 2025 18:47:34 GMT
EXPOSE 443/udp
# Wed, 12 Mar 2025 18:47:35 GMT
EXPOSE 2019
# Wed, 12 Mar 2025 18:47:40 GMT
RUN caddy version
# Wed, 12 Mar 2025 18:47:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0c4bb2d0220227f457267c48b8b05622b5a83afbc3026d4b39dd575c05de3a`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089c0ab037c6a430ef561f326e9937208d21a1074d3e628a6c8f06298d985daf`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 342.1 KB (342148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b776cff3f47b06da06c9770771101745b5b95634f98465357d523645be9e6`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0498cc3702dd49a2a399de9f37b93a5ce1645ff82dee9e973209f6d2e0609af3`  
		Last Modified: Wed, 12 Mar 2025 18:47:53 GMT  
		Size: 15.0 MB (15002278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c319e3076b2ee7245a9de9840d6c0b1c5d15c04a170af4eddafeafa3514e467`  
		Last Modified: Wed, 12 Mar 2025 18:47:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dad9eeb2454b823530c41c97f66efe6d456893b36304625af00c1c2631ec17`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80203d078e3ae007fb0bd7311b5369c46f3daf4b2218d1ea3bb14a8b8ec9a94`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d495466f2e8de169be7302068793587f6dd07bd6a16d1e84bf2af6d3c6495f`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25eaff429bee4ca466fb094a20a25119b336e3434bf79e2526b09b1bbe2d53e`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8cdf5b58fc5cc5a75bc299356534b7d54519857873ce9e3db3514839fbda01`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de0967722fde7ba30e01ed1474b95646eddd8ff9483ecb4026ecf70d42974f1`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dda06e0ea33b9df4124562577790d63bf894f2a705651c30073df07c3a2266e`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88daaa748bd3065007b925a424ed0167ce9aa4bd6250d279ebe7299ec31d7ee2`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e26ec9c4f5d853ac0439cc64c551e76a153acc77c93bb0af15d975a29553c41`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89a90cf3438bdbc9499ffb916150bc715a519e58ed3c3fe99b675160b47a870`  
		Last Modified: Wed, 12 Mar 2025 18:47:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010c889dd5cbd5383e5ea985eafc6234d507416b5dd2637112947b6e422c863e`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd5e3905b9a5601b8d3b5c72f4db0bad5c4ba8a68bbd0f16579267460e35ce0`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eaf3c65c2679d95ef34b87941c305ec878285bc389ba79c379e9abb07b04d26`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3028a1484fe765d3859dc9f4bbb6a329b15671a5fa24253fcd35e9d3afb2905d`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 334.5 KB (334485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267f277f7ead5674a53c2926751dc033541be2211b3d97184034a08f84305629`  
		Last Modified: Wed, 12 Mar 2025 18:47:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
