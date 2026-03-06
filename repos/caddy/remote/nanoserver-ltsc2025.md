## `caddy:nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:580b97c3b3d9597e83fdf488acc336c9c68ae509aa4a7e0fce92b3224f054e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `caddy:nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull caddy@sha256:6732f828931b8a1c1a8bd352e2b936bc0b5a4ad38cfb858203731863e36f47a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217169982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fba8538d67a17edb2b5259df2257889e8d44c23923b2afc107d314755846b68`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Fri, 06 Mar 2026 19:12:46 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Fri, 06 Mar 2026 19:12:54 GMT
RUN cmd /S /C #(nop) COPY file:11e7667c1584a79af7b586b90aae7543497c229bc94afaf5bb80d10c2bc7791e in c:\caddy.exe 
# Fri, 06 Mar 2026 19:13:00 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Fri, 06 Mar 2026 19:13:02 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Fri, 06 Mar 2026 19:13:03 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Fri, 06 Mar 2026 19:13:04 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Fri, 06 Mar 2026 19:13:04 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.2
# Fri, 06 Mar 2026 19:13:05 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Fri, 06 Mar 2026 19:13:05 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 06 Mar 2026 19:13:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 06 Mar 2026 19:13:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 06 Mar 2026 19:13:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 06 Mar 2026 19:13:08 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 06 Mar 2026 19:13:08 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 06 Mar 2026 19:13:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:13:09 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Fri, 06 Mar 2026 19:13:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Fri, 06 Mar 2026 19:13:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Fri, 06 Mar 2026 19:13:13 GMT
RUN caddy version
# Fri, 06 Mar 2026 19:13:14 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f36e3fb3ee3952aeab7b05a707d99a9b09935679ce41270aebf06770482a7cf`  
		Last Modified: Fri, 06 Mar 2026 19:13:24 GMT  
		Size: 69.8 KB (69835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7547b9a9e56f8502c607e191b9a727a8b2b26d0b63041026a026dcea6c122ede`  
		Last Modified: Fri, 06 Mar 2026 19:13:26 GMT  
		Size: 17.3 MB (17318431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb39b8f32dc4a47f3f19f02ab962923f97650677fb949cc2b1b4bc9550717ea`  
		Last Modified: Fri, 06 Mar 2026 19:13:24 GMT  
		Size: 285.1 KB (285098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bdca12ca6bdb70a76d57817957221b476812527f8f539658db54bda9e1766b`  
		Last Modified: Fri, 06 Mar 2026 19:13:23 GMT  
		Size: 109.7 KB (109673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b8fdbe7d49f70c45aae9142e083f18702ec7bd3a660679696ab6de09d7af87`  
		Last Modified: Fri, 06 Mar 2026 19:13:23 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afff647fa0521e47c479265d654b7674511f33b03dd59fb67914f978ce438630`  
		Last Modified: Fri, 06 Mar 2026 19:13:22 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9187712b8ac37b45eda79478dc64a0b08a37c2e1aed3ca91c47c9319f0f5bf`  
		Last Modified: Fri, 06 Mar 2026 19:13:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae95a1721b3ee6464510ceaa1ec691eff9d1d9d94f61f692ec6f8592a5d2615`  
		Last Modified: Fri, 06 Mar 2026 19:13:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a1ee745e9ba4c9e26f5e0135301edb7205b9074630a41afb841074a6dd89f`  
		Last Modified: Fri, 06 Mar 2026 19:13:22 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0794ecffbc5cda8588d68acc3089fa8c34a66455e2f94ffe580c401782a9b964`  
		Last Modified: Fri, 06 Mar 2026 19:13:22 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a679c0c2ae2f03bb631591afbd8e18f2012154206b23b8d4dedb2a67a95f38`  
		Last Modified: Fri, 06 Mar 2026 19:13:20 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfcb8174fa34e904591e95b614451723c9e886a561bd7f515f9e69ebb5ab087`  
		Last Modified: Fri, 06 Mar 2026 19:13:20 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935c37529cb9bc2096077862993f9c1738f88afba78e1c6aff2a34a2e7820cd4`  
		Last Modified: Fri, 06 Mar 2026 19:13:20 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9ec778a578265fd0abe45f336e22e6008151d7db85e08c13f90fb574eed194`  
		Last Modified: Fri, 06 Mar 2026 19:13:20 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b720f9fc4bccde5bee4334dccf08fc4621b9d266b70d0866d9dadd4b9ec0f2`  
		Last Modified: Fri, 06 Mar 2026 19:13:20 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fa829f09e03176f4509aa0a1812c4c92ebd68bc09e1a9badb20b00556976bc`  
		Last Modified: Fri, 06 Mar 2026 19:13:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10da28be1e3eddf92e5e8c37006ca7ed02e591f4e7cf04dd24ae6d0e04b66b2b`  
		Last Modified: Fri, 06 Mar 2026 19:13:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6c4847064a35a68654a7450219f5b5c25fe671d25c1afb897a14d8628afa5e`  
		Last Modified: Fri, 06 Mar 2026 19:13:19 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cceac83e142e49109e45cbbb34d9670d5db90087a0f8ccd11c032bcef497c5a`  
		Last Modified: Fri, 06 Mar 2026 19:13:19 GMT  
		Size: 119.5 KB (119475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900dce485b8b2598f9cbb123f5d78b1a392e34a629392041ac3c58c32aace771`  
		Last Modified: Fri, 06 Mar 2026 19:13:18 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
