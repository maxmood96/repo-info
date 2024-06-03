## `caddy:2-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:298ce474adcb68acbbf7d561e3182062bc7c263ef39cfac2632da7d9841bf435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `caddy:2-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull caddy@sha256:e6db27474d89a30e19a4fe90189b84ce3c43e933075fc380730c8b35adbfa971
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2128593264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4881c93dfe5ec6835959c290ee1e8f939e061da284db35eea81a684147727ed2`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:01:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:02:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Mon, 03 Jun 2024 19:02:10 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 19:02:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Mon, 03 Jun 2024 19:02:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Mon, 03 Jun 2024 19:02:26 GMT
ENV XDG_DATA_HOME=c:/data
# Mon, 03 Jun 2024 19:02:27 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.title=Caddy
# Mon, 03 Jun 2024 19:02:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 03 Jun 2024 19:02:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 03 Jun 2024 19:02:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 03 Jun 2024 19:02:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 03 Jun 2024 19:02:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 80
# Mon, 03 Jun 2024 19:02:33 GMT
EXPOSE 443
# Mon, 03 Jun 2024 19:02:34 GMT
EXPOSE 443/udp
# Mon, 03 Jun 2024 19:02:35 GMT
EXPOSE 2019
# Mon, 03 Jun 2024 19:02:41 GMT
RUN caddy version
# Mon, 03 Jun 2024 19:02:41 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc9e3f16619094921579c508caeafe5fbd4be335b90d2bdc8456fe7b1c8cf53`  
		Last Modified: Mon, 03 Jun 2024 19:02:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1bfc62b6094a1fbe3556a4e6dd6a3eab62019905a0a86931ef6d3de28e89d`  
		Last Modified: Mon, 03 Jun 2024 19:02:53 GMT  
		Size: 361.9 KB (361943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb2770de7d8b0a637920699459f41fa4308dea87e21da043c717b91bfb4fa94`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f45d642d99e99c508d6774f2f5b925804eafb397ef9744de9e1408978eb1e8`  
		Last Modified: Mon, 03 Jun 2024 19:02:55 GMT  
		Size: 15.2 MB (15220732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2445fae5d00d0d1231acaafd6a1fb8e571705ada84e75d3a7b97962da9b76`  
		Last Modified: Mon, 03 Jun 2024 19:02:52 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0279c7bf7ce2cde3d6c8061f80e8e4b8bb88b798007595863f0e5f87829a53`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fca3202cd979191633b784a0509517231ef5bec3ca748d9ef291ad62cd894c`  
		Last Modified: Mon, 03 Jun 2024 19:02:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2928df5b32dd3d1d421fd79744ef02b9f8b278dec3ac73b4abb915c7c63fe06d`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec1421b0ff702830c81b770e54392d3c6522f8eab9a7edc441fe13b012fae67`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b025bf27a9422170bef762810a54a92ea412c15290ed5e7420026cb00b1da6`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0481f87c40c5fb8cc6501cc91b495649d7b974ad36b924a093207f179106a0`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db8b38928ab0e66573f72481501e98f46d466d3f9b688c7d5324d37e8b12ef`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48eb824e4a53f76a56831b2f01b41a2d7c79b492c0ca24611c7bb9ecbca23b9b`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae56a925ebfbb56ca8a71b6f5d6d7aae10bf486814927b6a98454549ca16519`  
		Last Modified: Mon, 03 Jun 2024 19:02:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339be01ef890092f003845864424305cfef014669d417613292c1a048d61b1f9`  
		Last Modified: Mon, 03 Jun 2024 19:02:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75631559fc83f3c1f1f89b9637ab844389108228e3570acc285210fef68debb`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22323439f064623fae35007af39f199a0873fb676ff0cc6b59513ebc620b7001`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c1c8741c3a63a92dc88ec8e45773f43f6f9b30ee5ab01feda3e72d68ad0b1e`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a73612ad1af7062adc7d2f8481c460bf468814ddda476b34d668062f45f4bf`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 317.2 KB (317196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f978a46a3769b43eaa18729d4137498e769df0ca7c322a56e6867e831fed8`  
		Last Modified: Mon, 03 Jun 2024 19:02:46 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
