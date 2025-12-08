## `caddy:nanoserver-ltsc2025`

```console
$ docker pull caddy@sha256:6c865ae608cf146d8f96f7b00205aedb1a8faf65e98b654c74d6e1c4cc62f0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `caddy:nanoserver-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull caddy@sha256:c928d59154347f49b9837949bea16d53179443b7bdc8773215a9f05d44031019
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214598513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78b0eb39e1f7d439d755405b2d3673c587029d85de64cb8bed0ec861ae2b842`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Sun, 09 Nov 2025 10:04:50 GMT
RUN Apply image 10.0.26100.7171
# Mon, 08 Dec 2025 18:36:22 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Mon, 08 Dec 2025 18:36:33 GMT
RUN cmd /S /C #(nop) COPY file:32cf40eadbbb089db5d2a89aab3783b917db3d218ef99bdd6915c6b4af650c32 in c:\caddy.exe 
# Mon, 08 Dec 2025 18:36:38 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Mon, 08 Dec 2025 18:36:40 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Mon, 08 Dec 2025 18:36:41 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Mon, 08 Dec 2025 18:36:41 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Mon, 08 Dec 2025 18:36:42 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.10.2
# Mon, 08 Dec 2025 18:36:43 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Mon, 08 Dec 2025 18:36:43 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Mon, 08 Dec 2025 18:36:44 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Mon, 08 Dec 2025 18:36:45 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Mon, 08 Dec 2025 18:36:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Mon, 08 Dec 2025 18:36:47 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 08 Dec 2025 18:36:47 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Mon, 08 Dec 2025 18:36:47 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Mon, 08 Dec 2025 18:36:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Mon, 08 Dec 2025 18:36:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Mon, 08 Dec 2025 18:36:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Mon, 08 Dec 2025 18:36:58 GMT
RUN caddy version
# Mon, 08 Dec 2025 18:36:58 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:87c91227213eb6e7c8cfe33b6bd0429350e524756878f37f3860b013f804bf59`  
		Last Modified: Tue, 11 Nov 2025 20:41:49 GMT  
		Size: 197.9 MB (197936447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6644422d3626612abc76d303bdc40525e90932e77977f25a98a4b080e22bd8`  
		Last Modified: Mon, 08 Dec 2025 18:37:51 GMT  
		Size: 70.4 KB (70374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb9794b93e7552ea134515127e9afbca5bf3b61e8de37a804865674e26a575f`  
		Last Modified: Mon, 08 Dec 2025 18:37:53 GMT  
		Size: 16.2 MB (16217740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdc16d1ee69c3c51c7f1affcf680a4b99dfedaa3b3f7322105417ff66416d8b`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 138.3 KB (138261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfcc18648e0e3fd846bd6b43e591531cdc2b34500d672248d97e52f503db54b`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 107.7 KB (107746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c3a1ca8b47726afc9bbbcd585bcceaacc0738d5f3f31d184b377e5d0cfc9aa`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffc97f9af23523c9b663030e8f8fc274e1f99e787ce46bf13b7bac57f106342`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589ef439420226630743c99d90aa47502f597e2cdac40c5fd0d88c9761404523`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bd67f50927eb38b2372007bad99658b06efeadb1638e93cb053f4b59fbea37`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e297b10075d16c799ce9a13205675c73c4ba3a16ce06bf726064edb3e961e71`  
		Last Modified: Mon, 08 Dec 2025 18:38:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c2b1d0def125c8569070d5a5a1aa5719faaca6909fd087a97a2f4e2ee71be`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741882ec523df2fbef5a9a9efdf3dcbadbee6a643a03fa0853538c6f218015af`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6a870473ab90e8d8f8411b0e45a9fe73e48535684febfdf6d7e3c50dd1b88d`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3e1fcd90b3681fb04b428e4eadd5939043f34b7eede148a0f36abb20491c5d`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf6c0f59e9db7cb19e874a2e220e43490823061536641599a2bbf425209209`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c86f1aae1ab65e986675485091c5e47c85443a1df8f8a99e9f6078d49ee280`  
		Last Modified: Mon, 08 Dec 2025 18:37:52 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7910063bb8951f765091aad3162091404ae9db1399a23c3e38eccc79a054563`  
		Last Modified: Mon, 08 Dec 2025 18:37:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60ca7234deaa6ce5d1d94d8f80500f10a1c7fe463ac65c90c31cdf840dba78d`  
		Last Modified: Mon, 08 Dec 2025 18:37:53 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9b19a4e86bd2812a9954d58fb2f3163704c8b6dc74bb3fc4ff53de37ef46a`  
		Last Modified: Mon, 08 Dec 2025 18:37:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cf3cd5a4c36fa037e4da6f790bde636a5ed565658f4b146d81acd1b2b8e88b`  
		Last Modified: Mon, 08 Dec 2025 18:37:53 GMT  
		Size: 112.0 KB (112013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434898d5f59db7dcfab7b399468ef9b1362f49b2581588ef4914cba668c45e89`  
		Last Modified: Mon, 08 Dec 2025 18:37:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
