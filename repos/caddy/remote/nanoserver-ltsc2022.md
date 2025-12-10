## `caddy:nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:7931925260e18bb7c0e7b4e16c71351bdb73b055d479ce9df38ae288c7d8f5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `caddy:nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull caddy@sha256:b546b4ef8f9a17a8f20c4b44e3b2f5e49cb02d6a58435b74636570096a8ea81d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143049932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3711cc2168cd77171733041a120e28fced851fc5a63c9a9caa531a87efa43e`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 09 Dec 2025 21:17:46 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 09 Dec 2025 21:17:48 GMT
RUN cmd /S /C #(nop) COPY file:32cf40eadbbb089db5d2a89aab3783b917db3d218ef99bdd6915c6b4af650c32 in c:\caddy.exe 
# Tue, 09 Dec 2025 21:17:51 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 09 Dec 2025 21:17:54 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 09 Dec 2025 21:17:54 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Dec 2025 21:17:55 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 09 Dec 2025 21:17:55 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.10.2
# Tue, 09 Dec 2025 21:17:56 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Dec 2025 21:17:56 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Dec 2025 21:17:57 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Dec 2025 21:17:57 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Dec 2025 21:17:58 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Dec 2025 21:17:58 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Dec 2025 21:17:59 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Dec 2025 21:17:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Dec 2025 21:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 09 Dec 2025 21:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 09 Dec 2025 21:18:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 09 Dec 2025 21:18:04 GMT
RUN caddy version
# Tue, 09 Dec 2025 21:18:04 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005a5aa4fb9366e8b0170598708ea5150e6a89ae21a5b9a4bbc93054fe26832c`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 75.6 KB (75630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d6ec222ded998ea91166d74db4a2b6d0a03c861cfd0dd3258a0d76cb576770`  
		Last Modified: Tue, 09 Dec 2025 21:18:26 GMT  
		Size: 16.2 MB (16217718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f80950bf20039dc1b793c238b901931f1d84c8126c69493405126da400590`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 146.5 KB (146478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4ddd4a91c2585482a06c6c3c6754d5eae9a2fd491ab2181f2b38eec68ecd17`  
		Last Modified: Tue, 09 Dec 2025 21:18:25 GMT  
		Size: 115.7 KB (115697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9319fa3806af315cb19d89c9abc65fbab154ecc433fa2865ea3f48a6bd945f`  
		Last Modified: Tue, 09 Dec 2025 21:18:25 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8eb27f6db591ea6958f6d58e4041c26c2f2390d6d28716c8234eb0830786be3`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda95f63a3e40012d89f27f60c10138f9504d7e13f6ffc3c88c04b4ebfb8faa4`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3a4408c3af7f62df302e1ee143e15d769b05b07cde5023fe4f8129679ca8ef`  
		Last Modified: Tue, 09 Dec 2025 21:18:25 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf0f3e7c70f1672b6a4c5d809e43df6a89bf8f785f3b2bcb93adbf04fc60418`  
		Last Modified: Tue, 09 Dec 2025 21:18:25 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c704e812a1343d2ff2d8dff724520dc6cd5284afa7f51e2dea1d46c2fd04cc69`  
		Last Modified: Tue, 09 Dec 2025 21:18:25 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abcb7b6b8ba38f409c73618ed6d7c62dbd907807f46239718ec02e55685019c`  
		Last Modified: Tue, 09 Dec 2025 21:18:23 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45665b5d744bb7a3a671b72a3815121e6d4383f0d67592acc25f560bf65017a`  
		Last Modified: Tue, 09 Dec 2025 21:18:23 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7e7ebf06e84ebecb5295bcaad779a319b317f651cab725dcf3e32ce4a3f77c`  
		Last Modified: Tue, 09 Dec 2025 21:18:23 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a2ebea169b0add696a6817cf0b857cc3a13a4ee1fb5ecfa252987ac9a3a7de`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e203465a2d575be38767d662b10d895075978b8667f888ba6248ea65488f20e`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e22bd1ed4b5866634973d0dcc07a8e8b33a77d3e622837ea9e788ccf86f484`  
		Last Modified: Tue, 09 Dec 2025 21:18:23 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e870fd4f16d0f351839402693530e5fa3bbec80b46a0b760bf92ce7708aef5`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291866bdf2c5df029db2ceeecca50847c3dccabadc0dcd4577652a029b7ea787`  
		Last Modified: Tue, 09 Dec 2025 21:18:24 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b050df4678bd293ac6d0ae47c7abf9f02134ddec4e1b2053f7fe0404d669b3`  
		Last Modified: Tue, 09 Dec 2025 21:18:23 GMT  
		Size: 120.1 KB (120088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbbcdcee0aadf6cca8ade33faa0161eddcbe394f5eefdaeb231b57f8724d3a1`  
		Last Modified: Tue, 09 Dec 2025 21:18:23 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
