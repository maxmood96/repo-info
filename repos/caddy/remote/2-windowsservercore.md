## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:acf5e23cec50493c87055dc956c95daad8a5c724686b1d96fe7b188ca4e62e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:db2ca936588a88f8cb1f1ac281665623ae6cff49aa03938f153f61368a5cc56b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015565479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df45dc5c85ef1b67aa9ac39373f5d31666a1fc45364c803bbcedc13b41167ece`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Wed, 01 May 2024 21:52:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 01 May 2024 21:53:35 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 01 May 2024 21:53:36 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 21:53:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 01 May 2024 21:53:51 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 01 May 2024 21:53:52 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 01 May 2024 21:53:53 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 21:53:53 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 21:53:54 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 21:53:55 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 21:53:56 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 21:53:57 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 21:53:58 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 21:53:58 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 21:53:59 GMT
EXPOSE 80
# Wed, 01 May 2024 21:54:00 GMT
EXPOSE 443
# Wed, 01 May 2024 21:54:00 GMT
EXPOSE 443/udp
# Wed, 01 May 2024 21:54:01 GMT
EXPOSE 2019
# Wed, 01 May 2024 21:54:11 GMT
RUN caddy version
# Wed, 01 May 2024 21:54:12 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0010899e99c47859b14feb3007a937573303de68076ec99117119ab57fdd57c1`  
		Last Modified: Wed, 01 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c890145d7d363f973edd90b4ffdcc5d20b5b1260bb3bbeb325dbcf0e9009a3`  
		Last Modified: Wed, 01 May 2024 21:54:18 GMT  
		Size: 512.1 KB (512100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8422e5e19e084131580873257c6f2625df71a8745e2c1595ded7c16ba475a0`  
		Last Modified: Wed, 01 May 2024 21:54:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ef736991f48e994e25aeb590132bea5f19d8b42fa8d1180d315f2f73495fa0`  
		Last Modified: Wed, 01 May 2024 21:54:20 GMT  
		Size: 15.3 MB (15323389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef601d3fe6409725e550af59a5ba123c5702c2fbd40b326cc940c084d5f0785`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3df3db726e1e0a5a13fec3c8248a22c2d9e07471c0b95a3ba2f0e4cc95b304`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3cdb261531e719d2bc6b975c0f53b29040dbe568c1303af740b2ae6ea41b85`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff5c5e04007ac6458d1ea04660e383c43b99803f43e2a668701b18941736838`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84de06b1d99a5017a815393d6265dc38221ccec44af3c08e6c2ff648892b34b2`  
		Last Modified: Wed, 01 May 2024 21:54:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6def0c5665fae6a5f2f264ed2da99bab0ecd84fef2046f839b3b401056847`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4fe393b3e7b4c6b6456a1973667f020b2302bb22dfe798cdc05b944a97769e`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71ec2469f82bfb83af1bfb0fded85a95bfd2712cb32d862af3b7129c6211fec`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd104668c0fec173f2d4d176447ae55e00a317704f13f2f0e6b88c962dfef1c8`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5409a5e8b2cdefd2116ef7002f18fa0f8dc654c94ce9d998e8b249893c495bc2`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f0af2fa993eebe78fa6f22654d8c4b0a0ac855f974f10f4f541eee1477bd8`  
		Last Modified: Wed, 01 May 2024 21:54:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a8d145e66895c555fa5ee89b4deeb8f1e72d45cdbaa91f0b2ddd9337a404df`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1491cf2c5b446d7e52a6a7a07c7929a86546c4d6e88c807abf9117cde973bdfb`  
		Last Modified: Wed, 01 May 2024 21:54:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdc06d71f3b6a91dfd3cc874ed8e93b0c646b7e6e1efdd7825dc8a7e3d45db0`  
		Last Modified: Wed, 01 May 2024 21:54:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91eb21f53b513606014145f4ab50fc401c21276b52680592c2dce492250d5cc`  
		Last Modified: Wed, 01 May 2024 21:54:15 GMT  
		Size: 334.3 KB (334339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2799cd914dadb04d5be8ac47754e967df5574ac518aecabdf69ee7e83575ef3c`  
		Last Modified: Wed, 01 May 2024 21:54:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:58b302755f654da481f0b65cb8a754c0682320d6d1d67983df3fe8dfd2519292
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180627792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8709e36c6a33d54655556e49964ded05c8cf7bac9dfccf3155b88388bc5b9c6`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 01 May 2024 21:52:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 01 May 2024 21:52:49 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 01 May 2024 21:52:49 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 01 May 2024 21:53:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 01 May 2024 21:53:19 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 01 May 2024 21:53:19 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 01 May 2024 21:53:20 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 01 May 2024 21:53:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 01 May 2024 21:53:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 01 May 2024 21:53:22 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 01 May 2024 21:53:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 01 May 2024 21:53:23 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 01 May 2024 21:53:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 01 May 2024 21:53:24 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 01 May 2024 21:53:24 GMT
EXPOSE 80
# Wed, 01 May 2024 21:53:25 GMT
EXPOSE 443
# Wed, 01 May 2024 21:53:25 GMT
EXPOSE 443/udp
# Wed, 01 May 2024 21:53:26 GMT
EXPOSE 2019
# Wed, 01 May 2024 21:53:48 GMT
RUN caddy version
# Wed, 01 May 2024 21:53:49 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11f8f0ed706dd088e2964a1db4c196eab427d3ebcd72a94bc601bc71f0edd66`  
		Last Modified: Wed, 01 May 2024 21:53:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7867e31171e68f8934ada5c219f4c6f382d53aef22408ff4303e828a83ad0246`  
		Last Modified: Wed, 01 May 2024 21:54:00 GMT  
		Size: 497.1 KB (497053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953f416cfa31c18fc5a61bc98c96d8637a1cde627f2f5394d0a515489411040f`  
		Last Modified: Wed, 01 May 2024 21:53:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a76666bffc803defd63fa816e852588ae58756e61b07006c09b7722e9648474`  
		Last Modified: Wed, 01 May 2024 21:54:01 GMT  
		Size: 15.3 MB (15344008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1605fdc91841c5519f821acf15e6b1c23522f51bf72c2136541550a7c5a1aff3`  
		Last Modified: Wed, 01 May 2024 21:53:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24774db8845fdc637df149345943184e1f4c523ea2b4dd00407788369e0d7cc`  
		Last Modified: Wed, 01 May 2024 21:53:58 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6051ca70f9a3d922809a1676bc4a00f1c9cc43020c18a765905660bd4e36e087`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a03e682933b577dc860b4314b7947c0873cd968ec09c4c6d851878589ff446`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105b73d8a840e890b5605d1ece6adeb212e32e17f31f70c6f206778d2c07c866`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489b6f22087ae5eb9b3131ea68a1e13033cdb0dfca64abbc4d5761cc7eadda91`  
		Last Modified: Wed, 01 May 2024 21:53:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154e4875860ebfccacb938b6d0169c810e3398d544960b97b3df96872f5f14c3`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dd5e69cfe7d2e118eb318eb0701125025185cffa40dd2be33c622068d5ace3`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c8b0d6c3ac77c9af55159666d49dfbea38d01f17f4824fa8738a6f9bdaea4d`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847710ca1f0cdda84e9d48d0d0577c8924de4d1b4ee1dc5e72d62b99a57a9cbb`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802477541d228fe5a3dfd3d067b89afc39171fa056f56821b08ece8f94552108`  
		Last Modified: Wed, 01 May 2024 21:53:55 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a562cce4903e8ede1483531b0412cd0610454f6a21cc33b4bb228d5306013300`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4b04e85bdb051c214ae0c76191bc498513f5198158d22fb4f386fccb7b1f98`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce63a1f1784f21f621d3199572beda3b3d0cffd4c5cb9c858e6e3ef55014d1`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77523f1e3d4709dc2fed1ebfbd39c17444f56c74ef4a6a29bdfbd50c9ae38859`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 336.7 KB (336665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d02c65e08275d3374291aa34d44d250c91bb6254851098389c338efd91592`  
		Last Modified: Wed, 01 May 2024 21:53:53 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
