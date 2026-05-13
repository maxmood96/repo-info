## `caddy:2-nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:b21843052fd26e5c943085b7c762650b07dc8c29a3b5fcf8fbd31e386da15100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `caddy:2-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull caddy@sha256:c1a3c04375a21f3358a7269b3c8db4c9aa20ef17b18b299628f245772d62b8ec
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145119076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585a0b8930c616b9ec159071d830e486719683a74b5b5cef16388fd8909f31f7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 12 May 2026 22:11:07 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 12 May 2026 22:11:08 GMT
RUN cmd /S /C #(nop) COPY file:854ad2ee1fa7676b2f51b4797565415276e59ae047f290bedfc6fff5d087ea72 in c:\caddy.exe 
# Tue, 12 May 2026 22:11:12 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 12 May 2026 22:11:14 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 12 May 2026 22:11:14 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 12 May 2026 22:11:15 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 12 May 2026 22:11:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.3
# Tue, 12 May 2026 22:11:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 12 May 2026 22:11:16 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 12 May 2026 22:11:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 12 May 2026 22:11:18 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 12 May 2026 22:11:19 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 12 May 2026 22:11:20 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 12 May 2026 22:11:21 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 12 May 2026 22:11:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 12 May 2026 22:11:23 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 12 May 2026 22:11:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 12 May 2026 22:11:24 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 12 May 2026 22:11:27 GMT
RUN caddy version
# Tue, 12 May 2026 22:11:28 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7062b7138a20868c09846f50247b3e2ff443c3ef1b8866f596eb8add5b7c9c0c`  
		Last Modified: Tue, 12 May 2026 22:11:37 GMT  
		Size: 75.0 KB (74993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275bbb8293a19aca0ec6bfe70dce9971367d582ff1e2dae43a120dcc6feb48bb`  
		Last Modified: Tue, 12 May 2026 22:11:39 GMT  
		Size: 17.5 MB (17549642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19bacdcaad8543374f21ab698f8b9b630cfd16096aa335296a5557f018947dd`  
		Last Modified: Tue, 12 May 2026 22:11:37 GMT  
		Size: 282.6 KB (282593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb76583a37e857cd9095ef25e843f4d10ee6e8eafd77f33ee032c9a61c87f9b`  
		Last Modified: Tue, 12 May 2026 22:11:37 GMT  
		Size: 119.6 KB (119554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3529b85ea58301e5cb550653ab48977a58867340b4c6418a1915f1234314a6`  
		Last Modified: Tue, 12 May 2026 22:11:37 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca3cce98047cb7dadb4936ba3f543e49c9bea14b7a3e79b926f0faff8e55060`  
		Last Modified: Tue, 12 May 2026 22:11:35 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1207ead8adcd8bb05df9d46da78b890e4a86facafdd0bf9e5f0a7a27780fd878`  
		Last Modified: Tue, 12 May 2026 22:11:35 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97079071bafd713f1b6d84c8b221cd8e84ae8a7a8564e0be39a26ed4635cb2d`  
		Last Modified: Tue, 12 May 2026 22:11:35 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac318d98086610d062d44938510553d3d87d726c5ebb5d5a42f2c0a961ed8e8`  
		Last Modified: Tue, 12 May 2026 22:11:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4223ffd68c15334b1bb311a7a91fee6beb32deb8d3b1a2b6bd0948032e6c97c0`  
		Last Modified: Tue, 12 May 2026 22:11:35 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a098887dd4c7eb74273785661306e3369d332ea049878f75e28f1870f1644`  
		Last Modified: Tue, 12 May 2026 22:11:34 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66501b51ee0367d2f19847b6cb7bd38c4add99193a960272d9a80aecd94f0a66`  
		Last Modified: Tue, 12 May 2026 22:11:33 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54f7535d55eea234ccb3f2d5b85176186ad3222b7334cc8a2279ab1c3e6970c`  
		Last Modified: Tue, 12 May 2026 22:11:33 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42884647b37678fe797ef7629684b977bdf0491a833005d2faa2656797c7fc42`  
		Last Modified: Tue, 12 May 2026 22:11:33 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76945a5aa73d2fb9ad35cfd68ab5429185acd920c14d7e2cbc42160b9df7a758`  
		Last Modified: Tue, 12 May 2026 22:11:33 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2c03d9d1755838028f5ea8b1a7420d0fa4d277864c46fd5e814a20677b504a`  
		Last Modified: Tue, 12 May 2026 22:11:32 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23edc09a1b0b1afdbf7913f570556f03e59d4078c8768514cb533e2e7f733f`  
		Last Modified: Tue, 12 May 2026 22:11:32 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c1fd15164a05313a54ad893ffb18ff18aef1c17cfc2fa89bc35527aebb90b6`  
		Last Modified: Tue, 12 May 2026 22:11:32 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe6ba2f887a10b8e1cee4021c273b3b1c350ba5dd0436ab960d535929547f45`  
		Last Modified: Tue, 12 May 2026 22:11:32 GMT  
		Size: 120.4 KB (120358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97b52d72fc5730011a24923f149032887854ccad161cf48b3404c4602109c35`  
		Last Modified: Tue, 12 May 2026 22:11:32 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
