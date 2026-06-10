## `caddy:nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:fa26f0805d3e9aec35489bfbb22357418e3d0ecbc8890ccd7c98473d699e6fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `caddy:nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull caddy@sha256:a3cf17182f95814b45d2486488ee36c95dcaf2559d54b5f0a94dc265104139ed
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142225891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b2003aab5da8cffc2c741461b164cfb9eedcaa39a9b1ef0ec6d33ccb38613a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:25:52 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 09 Jun 2026 23:25:58 GMT
RUN cmd /S /C #(nop) COPY file:7d2f419889d1c745e8d01a18ec688d43a6c8f6363f61c1964c7e88fd70b1b987 in c:\caddy.exe 
# Tue, 09 Jun 2026 23:26:02 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 09 Jun 2026 23:26:05 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 09 Jun 2026 23:26:06 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 09 Jun 2026 23:26:06 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 09 Jun 2026 23:26:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.4
# Tue, 09 Jun 2026 23:26:08 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 09 Jun 2026 23:26:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 09 Jun 2026 23:26:10 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 09 Jun 2026 23:26:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 09 Jun 2026 23:26:12 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 09 Jun 2026 23:26:12 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 09 Jun 2026 23:26:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 09 Jun 2026 23:26:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Jun 2026 23:26:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 09 Jun 2026 23:26:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 09 Jun 2026 23:26:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 09 Jun 2026 23:26:20 GMT
RUN caddy version
# Tue, 09 Jun 2026 23:26:21 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb81032a8c2dd6e7132cd0caa49b86381f824e398dd9dbf9df22fb6696f6568`  
		Last Modified: Tue, 09 Jun 2026 23:26:31 GMT  
		Size: 77.0 KB (76953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8d93ab59f4a96312287fff400bb3d06588cf45b4ddb48156c50b4c763e554`  
		Last Modified: Tue, 09 Jun 2026 23:26:34 GMT  
		Size: 17.6 MB (17619906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d293f74cec76d9714f70a4eeba73a954b5a5677550339eb861af7dddf47c78d`  
		Last Modified: Tue, 09 Jun 2026 23:26:31 GMT  
		Size: 275.9 KB (275880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714b55c1fa5aa7d80fe11a9c964819cc36701407a486e65ded5fd977afd8f4bd`  
		Last Modified: Tue, 09 Jun 2026 23:26:30 GMT  
		Size: 119.3 KB (119328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6030619cc7f7522a9304f3d3eced7baec793e54c2b049815bbaf2cf2822670`  
		Last Modified: Tue, 09 Jun 2026 23:26:30 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f04af4465c58a47ffe902ff6dc877a35c07eab121e26fb495aca1edc23fde9`  
		Last Modified: Tue, 09 Jun 2026 23:26:29 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c8e8252361cacb7aea26e4693ebae35a8a406c3bc4f9cf21f6035e3e6f3d75`  
		Last Modified: Tue, 09 Jun 2026 23:26:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb5434470ee6962c8d0c34d25dceb0ddf7165f1dc90f96cfb20e6493701013d`  
		Last Modified: Tue, 09 Jun 2026 23:26:29 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3115d8a867422f6987ab031a093390db57a6baaa58c5a10f6fb60c4364a6200`  
		Last Modified: Tue, 09 Jun 2026 23:26:29 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3754515431f058fb733e3a74ee5a7941a9c62d1e38a8e9e8faa43f03e05c30`  
		Last Modified: Tue, 09 Jun 2026 23:26:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d37350bedb49c33d28f38057269dac2cd906a48ee6dc1dbfe611ac85d345b79`  
		Last Modified: Tue, 09 Jun 2026 23:26:27 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a01d0f276f0e679f0b050ef295fd248add76639c672cb7e97aa4e99560e627`  
		Last Modified: Tue, 09 Jun 2026 23:26:27 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f568675273efe7432aa2f2f1eb70fbdac99da33be286f0f2e8612af840d43f09`  
		Last Modified: Tue, 09 Jun 2026 23:26:27 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dd2919fbb725563519ce12d0f7e593ac2611f8a352df83888f4f0b2ea1c548`  
		Last Modified: Tue, 09 Jun 2026 23:26:27 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4923f2056b48ccb08cfa3da8684cc9e2bbe6fc3cedcd6a4470a091ff743b1a`  
		Last Modified: Tue, 09 Jun 2026 23:26:27 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f326973820f912ecf9bbb366022af941c3ff5b987d408ad715fd0fc9e6321f37`  
		Last Modified: Tue, 09 Jun 2026 23:26:25 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7228ec3caf2de9d14fadaf6da9bd9f17c10efbf3abed3c72a61238f7c69005bf`  
		Last Modified: Tue, 09 Jun 2026 23:26:25 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb758d20ec3a623e9e6835d55eeb414bf1e479a49b1506b60917060a6b693d2`  
		Last Modified: Tue, 09 Jun 2026 23:26:25 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263642fae6d80b345d3b6029600a6ebbd8f6d2f7caaefb9ddb77f0ce1b0a30aa`  
		Last Modified: Tue, 09 Jun 2026 23:26:25 GMT  
		Size: 120.4 KB (120374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c3352846764f5f10c2d54d448bde96e945e2eb4abde7f5d055ae0aef21c157`  
		Last Modified: Tue, 09 Jun 2026 23:26:25 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
