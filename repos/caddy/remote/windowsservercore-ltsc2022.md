## `caddy:windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:94da3959564e7d71fb52b680e736eccfd2ad5e768b881207bd9f741237852c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `caddy:windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull caddy@sha256:db5c274ccc45263de4a8ba8ebce390351ad2fa49898d9763146fc26b04d836ea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268484635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608c62c77f5ec94e951a8f7c088dc6ea47479e1c7ebd645f0eee080def067a34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:17:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:18:09 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 14 Nov 2024 20:18:09 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 14 Nov 2024 20:18:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 14 Nov 2024 20:18:18 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 14 Nov 2024 20:18:19 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 14 Nov 2024 20:18:19 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Thu, 14 Nov 2024 20:18:20 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 14 Nov 2024 20:18:21 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 14 Nov 2024 20:18:21 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 14 Nov 2024 20:18:22 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 14 Nov 2024 20:18:22 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 14 Nov 2024 20:18:23 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 14 Nov 2024 20:18:23 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 14 Nov 2024 20:18:24 GMT
EXPOSE 80
# Thu, 14 Nov 2024 20:18:24 GMT
EXPOSE 443
# Thu, 14 Nov 2024 20:18:25 GMT
EXPOSE 443/udp
# Thu, 14 Nov 2024 20:18:25 GMT
EXPOSE 2019
# Thu, 14 Nov 2024 20:18:30 GMT
RUN caddy version
# Thu, 14 Nov 2024 20:18:30 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e284acfb7386a88ebb9963105f88e23996eb803486e2776ddcf61d11a6bb3c16`  
		Last Modified: Thu, 14 Nov 2024 20:18:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d48f43aca92ee15eebb0a3bf0f79f17841c6584b6014ea254f94f230b78b1e7`  
		Last Modified: Thu, 14 Nov 2024 20:18:36 GMT  
		Size: 367.2 KB (367201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930efd46d7d009e4275cd3707295fcd7c415c62053321ed60b65f53b921e94ce`  
		Last Modified: Thu, 14 Nov 2024 20:18:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b683ae783bd6dae904834c8b306ca74b580a7e937b327aeb1bdf6c10f5a0113`  
		Last Modified: Thu, 14 Nov 2024 20:18:37 GMT  
		Size: 15.3 MB (15261578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd243dcf2a49fb7ab9557d9bb44845404c4856dd7028054cf5a07447242b4356`  
		Last Modified: Thu, 14 Nov 2024 20:18:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673783fc86401d17deca80f7bd85b8c7f83d5f88f3301ef350fea02b0d3fff04`  
		Last Modified: Thu, 14 Nov 2024 20:18:35 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525f3c5a827d19c0d0fdda9ace6b550755c1dabf3aea882785ba4a764e502fcd`  
		Last Modified: Thu, 14 Nov 2024 20:18:35 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edf4762197d101310974bf443de98cc1735b19595d82404ce745207413816b9`  
		Last Modified: Thu, 14 Nov 2024 20:18:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6123f493097367bf582e53d5ba0e313601d40475f53de3abbb37a142471ea44`  
		Last Modified: Thu, 14 Nov 2024 20:18:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281c90c264254a55047b43dfcbe0df934940f1e0cab738e0aba8268cc2180297`  
		Last Modified: Thu, 14 Nov 2024 20:18:34 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35d37e132471be99e9533df7c3c4b49b68c6f9db46e38df0ce53945fa34359a`  
		Last Modified: Thu, 14 Nov 2024 20:18:34 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f08abb3bfa6198d6566f98b76970bc1acf346a6d30af0e20aebebc71fd1857d`  
		Last Modified: Thu, 14 Nov 2024 20:18:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78358c919e9cb3328ccc78075aeec0e412a980d670c40b5644808ec6d6da7724`  
		Last Modified: Thu, 14 Nov 2024 20:18:34 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5247f6f0d0d4bdd88686d12b7ffacb6c263ecc7f0562b08a399a4d5c6bb78429`  
		Last Modified: Thu, 14 Nov 2024 20:18:34 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8230061a360ef870e1e1b8b622af4f779cd99a7191ae2d784d56a71f2fe8cc9c`  
		Last Modified: Thu, 14 Nov 2024 20:18:33 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c28d99b93c4a5918cd91b6ccbe2f9e8cf9a713647c28b4732b633562d06d368`  
		Last Modified: Thu, 14 Nov 2024 20:18:33 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229cd8f2d3d0a3670844c7ebc172ac6a5e0e29e9b834138f58bcba38bc60e03c`  
		Last Modified: Thu, 14 Nov 2024 20:18:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e969559f9da428edc52bcdb694a7fd0ac80d244469bc9fc8df69af51211ba955`  
		Last Modified: Thu, 14 Nov 2024 20:18:33 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666088934bb08596ebbe2becb45b50b1c17b789143f30744e3967ec600ea37b2`  
		Last Modified: Thu, 14 Nov 2024 20:18:33 GMT  
		Size: 349.7 KB (349714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28f288ef70a5eeef4628abbef900d8af84b824db7d69d3221588c19716fb5c8`  
		Last Modified: Thu, 14 Nov 2024 20:18:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
