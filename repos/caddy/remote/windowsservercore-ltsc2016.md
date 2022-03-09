## `caddy:windowsservercore-ltsc2016`

```console
$ docker pull caddy@sha256:b546487b85047e9e3f4079762e61c94ed59d99fcb802345beec9026106536ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.5006; amd64

### `caddy:windowsservercore-ltsc2016` - windows version 10.0.14393.5006; amd64

```console
$ docker pull caddy@sha256:7f8374457a1c63677174631c3a8ea273702e069b924b615f44292250b7e2d8c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6289879706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40202b27c7479ec2d1d1618860745715dbfcabf489c651e5f04e826c286f72`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Sat, 05 Mar 2022 03:39:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Mar 2022 18:23:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Mar 2022 18:24:48 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/2f23e8a67eba98613ba87f2d04768f6b28875386/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 09 Mar 2022 18:24:49 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 09 Mar 2022 18:26:02 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.4.6/caddy_2.4.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('08fe8b50664644f5672a7357a7fe4c4835828c2464965ad78ec5f483dd2cd5643c64ea929d2f131601c48d71d2ddaebe251eb608d435ae1e31abe39d0687aebb')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 09 Mar 2022 18:26:03 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 09 Mar 2022 18:26:04 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 09 Mar 2022 18:26:05 GMT
VOLUME [c:/config]
# Wed, 09 Mar 2022 18:26:06 GMT
VOLUME [c:/data]
# Wed, 09 Mar 2022 18:26:07 GMT
LABEL org.opencontainers.image.version=v2.4.6
# Wed, 09 Mar 2022 18:26:08 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 09 Mar 2022 18:26:09 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 09 Mar 2022 18:26:10 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 09 Mar 2022 18:26:11 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 09 Mar 2022 18:26:12 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 09 Mar 2022 18:26:14 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 09 Mar 2022 18:26:14 GMT
EXPOSE 80
# Wed, 09 Mar 2022 18:26:15 GMT
EXPOSE 443
# Wed, 09 Mar 2022 18:26:16 GMT
EXPOSE 2019
# Wed, 09 Mar 2022 18:26:54 GMT
RUN caddy version
# Wed, 09 Mar 2022 18:26:55 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0fe465a8df276d07bd592c9424c00276a476fb7f74be6f867256b07fba31212d`  
		Size: 2.2 GB (2207094901 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c66997424475af0399fffec7897bad20e40b8309c56761077b30f5d9495f4db3`  
		Last Modified: Wed, 09 Mar 2022 18:29:32 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31f3b05b8f63dd42b4881a4c3d384691cc281678a86e0836d0c32819a344b5d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 345.5 KB (345470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9855b50f056bb89da3373dfb2c128c8cf2515840c723a9027f0c01bb0eb91d`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b715cda286f032f4b113aefacf8b42874e8bed4dbe0080772b9d6cc1e91fc4`  
		Last Modified: Wed, 09 Mar 2022 18:29:43 GMT  
		Size: 12.1 MB (12134708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e40c1797eb55c98999e616bff73129a77843c7cf7667787950662180cbd90b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d12359d4309d649fc7f0131974324ede0eb7aa11d1cd6f5d47000f9e14363b`  
		Last Modified: Wed, 09 Mar 2022 18:29:30 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1783134869b6be42026ea8457c2f07dcacd3e029eaa283e48e798ce94929111`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7104f8aa42fca009aaea2d885dfc7a0ea9acd8b7670cd9a90929f355d29cb5bf`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ee03e2f86a2587a31a03418808435e9804fd324f95c981776b71ac5541f122`  
		Last Modified: Wed, 09 Mar 2022 18:29:28 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617c8eb23f7d35a0012ac7a3ce817bb49edda99eb16da9e4a9e6897617ded26d`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85694b0569ffdf58e2f716205756d0a9eab45456d0ef23c2bbc8cb5816b99c1a`  
		Last Modified: Wed, 09 Mar 2022 18:29:27 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2abbbf56f3d370ddba372e974d4765e074ee94fa8b1e4037b1cbf9d4a1e04`  
		Last Modified: Wed, 09 Mar 2022 18:29:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4deaae43ac0785c4ccfb22ba187f33035f3041d44d770e8864cab157c1fe8`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7c04adc036f7a25c1c5a61895ba945aac263098d741203cb43e6b3b32174ef`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582d555a149be3d9ce42e33942b905cc2c8b9ebdc0dd1de51709fd7276c1e3ae`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b57929590127351973d44b26f950891ee7b918dc352a68098193a5d4fce629`  
		Last Modified: Wed, 09 Mar 2022 18:29:25 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71478b5420cbbbea1bb0a6e617445f903203fac8965dfc6e2c41932cbb7f2acb`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b709c8c0d2fb364fd66993072fd79d4d28cda233a5d991b74680a1f80b1563`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82093ad8180c0667cf71cdf92b8ead740771d5f2f5efda695fc67b815056d9`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34076b974bce5f92149f3e2eb58dc898a74d7ca4c563c20c4308f51a3f25212`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 293.4 KB (293417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e27086943ac64711a35c0e493db7b82a4faa0d65d5e80a91104238aba4845e2`  
		Last Modified: Wed, 09 Mar 2022 18:29:23 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
