## `caddy:windowsservercore-1809`

```console
$ docker pull caddy@sha256:9641c4ad8df632e8cf0b50ffdb2c040654007e05aacc3d6dd0074f2566c34522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `caddy:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull caddy@sha256:7bc4e34094da43c1e1b976aae13a2712d2b868423a9c0ec3b9a83a784319f501
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2030278913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc39690363d078b21bcfff6aa72c7b005b56e216c07b5970948e8d529f541d88`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:46:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:47:15 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/509c30cecd3cbc4012f6b1cc88d8f3f000fb06e4/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 11 Dec 2024 20:47:15 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 11 Dec 2024 20:47:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.8.4/caddy_2.8.4_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('89f8fc9ece9941a15a0981b3c69543d3b9b5fe095e747875a05fc1775d4d78d4505a7fe54a58d496dade601e85f6053a00a1b0382a781d3e8b6eec044384f6e6')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 11 Dec 2024 20:47:27 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 11 Dec 2024 20:47:28 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 11 Dec 2024 20:47:29 GMT
LABEL org.opencontainers.image.version=v2.8.4
# Wed, 11 Dec 2024 20:47:29 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Dec 2024 20:47:30 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Dec 2024 20:47:30 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Dec 2024 20:47:31 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Dec 2024 20:47:32 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Dec 2024 20:47:32 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Dec 2024 20:47:33 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Dec 2024 20:47:33 GMT
EXPOSE 80
# Wed, 11 Dec 2024 20:47:34 GMT
EXPOSE 443
# Wed, 11 Dec 2024 20:47:34 GMT
EXPOSE 443/udp
# Wed, 11 Dec 2024 20:47:35 GMT
EXPOSE 2019
# Wed, 11 Dec 2024 20:47:39 GMT
RUN caddy version
# Wed, 11 Dec 2024 20:47:40 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97246c5680611ca54c82b46a1b99c0fa8736360ba746944746eed74dcb909fd4`  
		Last Modified: Wed, 11 Dec 2024 20:47:50 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeced505dc30a6c09c2fbb3f49ab5f6c4ec7ed59ace87530a1330ba2b19113e8`  
		Size: 491.5 KB (491482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55c8ee4ffaf1ade428db3a519673893399f432c8491011f4fd396cf48d797ae`  
		Last Modified: Wed, 11 Dec 2024 20:47:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95e8bcd3770f76847fd62a51328e60ad9c60b3e15b34278d754b92788dc3981`  
		Last Modified: Wed, 11 Dec 2024 20:47:51 GMT  
		Size: 15.3 MB (15253682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf628b95e2a67f64242d79788eb69764ed136b7f983d6be69b4743bbd242930`  
		Last Modified: Wed, 11 Dec 2024 20:47:49 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa647b807d2607932ce4452b99cee480c80854e70d5d5d313310696241db9df`  
		Last Modified: Wed, 11 Dec 2024 20:47:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cc039e7fdf9da697ba72d0e51a701219e4304fa67a61f768ce08eb97a0083c`  
		Last Modified: Wed, 11 Dec 2024 20:47:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19306413c3479c482f4fd7d12f3f51fb038d8d925bf4f70c9a7a9fed885e045`  
		Last Modified: Wed, 11 Dec 2024 20:47:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538d98ba9a237c94414d055eedc9e5fb402186785d8d942196f4679de2106202`  
		Last Modified: Wed, 11 Dec 2024 20:47:47 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a6f3f7a33174be222c1f1fb6c83fb4348c32330100023a16941bd1de0ee1ac`  
		Last Modified: Wed, 11 Dec 2024 20:47:47 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4efe395ec6b3c203f94631a5e0753c7e3a1eda8d311ca646b1b3fbee3d4cfe7`  
		Last Modified: Wed, 11 Dec 2024 20:47:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c93ff0eaf4790a05bb623381571262b4f65c8d0eec354c59722d10d9e0245`  
		Last Modified: Wed, 11 Dec 2024 20:47:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1715dc9082095c2f00d6a96f47950ba97a4ff541fdab5f5b42e694925e76b80c`  
		Last Modified: Wed, 11 Dec 2024 20:47:46 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d96e08d7375e0732280791115bd877bc5bc121daac99c7d05f40f71b7a4ea77`  
		Last Modified: Wed, 11 Dec 2024 20:47:46 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11de2194170177fb68a1f08af2c5adff3c2e259bd937c1a86e7fd66e27bff89`  
		Last Modified: Wed, 11 Dec 2024 20:47:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b4c40e2c317372663cfbcf86ca814a9f047653e1365d23c933c2cdfdb2f688`  
		Last Modified: Wed, 11 Dec 2024 20:47:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52138eca4780e8bf876d80cca0ce16e2ab8b5c9ecf263bf7aaa2b29f6295585`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba08de7038b029a915d17270a87b50728fe2e8d351fb4569fc8e220ce703013`  
		Last Modified: Wed, 11 Dec 2024 20:47:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42af5ed85985c8b21ad32455c64c01c13c059a5014da6e2e113cbcb5f5197341`  
		Last Modified: Wed, 11 Dec 2024 20:47:44 GMT  
		Size: 341.6 KB (341604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d5643e79c16d911c06c0279af12f12afc4a90034ba5fca8e41d09146d75718`  
		Last Modified: Wed, 11 Dec 2024 20:47:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
