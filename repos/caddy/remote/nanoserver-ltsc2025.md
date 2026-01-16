## `caddy:nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:45830b9cc0fa95838d3d59d5aa53f91fd9dcc028fc919381a4b5d2f482f4d8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `caddy:nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:8637bdb2921095ea8bcdc3493767f2457da527e0a7f0d8a1b8b86a881854f5f9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215756218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb332b2253cdd9bcb1ee0989236994d2a6a9078ab12520f2f8bcad8e62742b4a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:42:16 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 13 Jan 2026 23:42:17 GMT
RUN cmd /S /C #(nop) COPY file:32cf40eadbbb089db5d2a89aab3783b917db3d218ef99bdd6915c6b4af650c32 in c:\caddy.exe 
# Tue, 13 Jan 2026 23:42:20 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 13 Jan 2026 23:42:23 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 13 Jan 2026 23:42:23 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 13 Jan 2026 23:42:24 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 13 Jan 2026 23:42:24 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.10.2
# Tue, 13 Jan 2026 23:42:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 13 Jan 2026 23:42:25 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 13 Jan 2026 23:42:26 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 13 Jan 2026 23:42:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 13 Jan 2026 23:42:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 13 Jan 2026 23:42:28 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Jan 2026 23:42:29 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 13 Jan 2026 23:42:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 13 Jan 2026 23:42:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 13 Jan 2026 23:42:30 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 13 Jan 2026 23:42:31 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 13 Jan 2026 23:42:33 GMT
RUN caddy version
# Tue, 13 Jan 2026 23:42:34 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:56 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2294e46c0dd4505121fc25611f38448c825469c19784a983dc4ea77513d4f7`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 72.4 KB (72413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f6b2ff05d344bf11065e05e95208b66edf3bfc7d729b360b87b77af1f45380`  
		Last Modified: Tue, 13 Jan 2026 23:42:55 GMT  
		Size: 16.2 MB (16217745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd33bca186aee11284e4e56e08c3c38a02d47e4ea6af8adc2e54a03c38270191`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 145.9 KB (145874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa2896f517c73ac99e6ebd85b8fbcb85d18fca7b8b6d8d4613813802ff1f664`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 110.3 KB (110287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70172cb5a9d7f93e4853ca7b53a17b88e45ca2a361ad2a6edfcd4aa3f592dd31`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e6116ca26d9c600810adc218ff820a9af801ff68c8bd484d69dd579c866b53`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007d04cc09b48caac2f80bb01be8504e5928d67db72bf978089c6a530ea3bec1`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c6197f22c57ff7e5fe7dce27c179d99e548bbae1a762665be84e8bb36fd6a0`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5ad5770313e911b3fede8ec2db264cd7745b42ba554503b2fb8e13e300a7f9`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1cbfa7a3d19d614ff34a32b6d067938d9ab48d60c1b1ba1f042fb7847d5c75`  
		Last Modified: Tue, 13 Jan 2026 23:42:53 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af0c01bfa5a543e840b8fa44b6822ad1ababc73de3c6cc47d36ed4d6fed28c6`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495397a413d965f5e8bf672eb9325b6f081f7510a08c9177698a293e405409dc`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2309c1c728ba57135a8063c1283b05e0f3f9a26409bfb6a13422ca1fd96fc40`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd217e105387b66255d2f930f10f31d0786f53821f315e30c61272899f70d098`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afa1b33bc657def1b238f7de879bd53aa84f7197f3e1d44fc0122afd2fdc5b1`  
		Last Modified: Tue, 13 Jan 2026 23:42:40 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc491403ca975f74eb27c545d75aebf879da9937df180079c9e2ae8eeaa26dc`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091ee6a33106d66867882ab66f87422c69d2415ee33be0f26449b0e476d88f92`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58b63ab31c707c7bca9e7d813fae3c312a40c2dc2881530cf967b8a75f6f00b`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb369297e4c8b5b42f28cc92ebe0556d3f5c980e3a69ea87c1b5546122a2dc`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 117.4 KB (117382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a62a3360faaa914d5f8ec1caa267d62615e5ed7c920928146cacb082ef9468`  
		Last Modified: Tue, 13 Jan 2026 23:42:54 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
