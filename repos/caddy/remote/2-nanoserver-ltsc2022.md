## `caddy:2-nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:748173f831f0de464f978cc6de2833a64be9463944f76e8075228d0d3d8fadfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `caddy:2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull caddy@sha256:587628cc099afb685ebf791072617dc04d148dcde599ca72f89a6e5c6cc419b0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144563191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4ea7d9ecc7c3b87d2ab1cc4a4b08182540d6a3b8c689dbe3c65c281a5736b7`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 06 Mar 2026 19:18:32 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Fri, 06 Mar 2026 19:18:37 GMT
RUN cmd /S /C #(nop) COPY file:11e7667c1584a79af7b586b90aae7543497c229bc94afaf5bb80d10c2bc7791e in c:\caddy.exe 
# Fri, 06 Mar 2026 19:18:44 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Fri, 06 Mar 2026 19:18:47 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Fri, 06 Mar 2026 19:18:48 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Fri, 06 Mar 2026 19:18:48 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Fri, 06 Mar 2026 19:18:49 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.2
# Fri, 06 Mar 2026 19:18:50 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Fri, 06 Mar 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Fri, 06 Mar 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Fri, 06 Mar 2026 19:18:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Fri, 06 Mar 2026 19:18:55 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Fri, 06 Mar 2026 19:18:57 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 06 Mar 2026 19:18:58 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Fri, 06 Mar 2026 19:18:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 06 Mar 2026 19:18:59 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Fri, 06 Mar 2026 19:19:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Fri, 06 Mar 2026 19:19:01 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Fri, 06 Mar 2026 19:19:08 GMT
RUN caddy version
# Fri, 06 Mar 2026 19:19:09 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb911cf5ad07d8b0aa47824e08f91fa9716d09feacd081a6d21c99b36fac7d`  
		Last Modified: Fri, 06 Mar 2026 19:19:18 GMT  
		Size: 74.6 KB (74561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b0d0774aa393fd60a7d8a9df53f2a75f2f647e1a75185f37552c6bb77ebe94`  
		Last Modified: Fri, 06 Mar 2026 19:19:20 GMT  
		Size: 17.3 MB (17318465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031bfa431937ecb10410bb2518ca161aa887d99da35598c924b4d916111e0545`  
		Last Modified: Fri, 06 Mar 2026 19:19:18 GMT  
		Size: 285.0 KB (285011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fde18ab5fdabcc9dc29016d95de19d67cbf509c9ee920fc401bcf48ec03e02`  
		Last Modified: Fri, 06 Mar 2026 19:19:18 GMT  
		Size: 112.3 KB (112254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a73d7aa8e3f0beb32a3f3dc8930d74ed30685aa97e7ca3c0df437fd9a439b2`  
		Last Modified: Fri, 06 Mar 2026 19:19:17 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cca0fb685d4052e1ea46cb1b7e635b0f895147fef77d086e707d411b0d4cad`  
		Last Modified: Fri, 06 Mar 2026 19:19:16 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38c332e202a47aaf0f8ea58f425603e9d599e1925e0c647b27cc0d9ece3a5cb`  
		Last Modified: Fri, 06 Mar 2026 19:19:16 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab34f5ddeb2acf419c0da33d61dcdec0dc8ee6f96bf531221113557950e65ee`  
		Last Modified: Fri, 06 Mar 2026 19:19:16 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7c4afbefbd52d21895b00da8bb82f1c66ac585077c4bd71616c8657ea41b05`  
		Last Modified: Fri, 06 Mar 2026 19:19:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a42af3e826497a2d61f18393f9aa5eae927a787f7664f10a95082efae6ecec5`  
		Last Modified: Fri, 06 Mar 2026 19:19:16 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db67458f8bad2917c6478e49da963cf2128862ada4ea30c3bcc5bba4071cdeb`  
		Last Modified: Fri, 06 Mar 2026 19:19:14 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef2062ac7fa7d38b5461cd1d7c7e16b6112bcecb593e11cadff893c070209c4`  
		Last Modified: Fri, 06 Mar 2026 19:19:14 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f081c0ec629326cf5f02dd0d5e9699c2607294d1efa2b6b8886bc6ffffe2d8f`  
		Last Modified: Fri, 06 Mar 2026 19:19:14 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a651e5bce416351865e086077a66632910b3fd6592584d1d9b82a74ced3f52d`  
		Last Modified: Fri, 06 Mar 2026 19:19:15 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a3a047c6533dd8efc1ff99ab4ffbaa1b6b8fd3182c0a060eea3c5e6a3bd73e`  
		Last Modified: Fri, 06 Mar 2026 19:19:14 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462efc33e141cd2fe16f1841a40ce7602813fc15bc952a753e6b3ab5ab6387f4`  
		Last Modified: Fri, 06 Mar 2026 19:19:12 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9b49117e662bde5f21d040f224b11924804aeb5021dde831c9fa16ee71a94f`  
		Last Modified: Fri, 06 Mar 2026 19:19:13 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa6520d8e9e5ac6881344089aa4b4b7745883e5f421176f8eb30f5aa9af99b8`  
		Last Modified: Fri, 06 Mar 2026 19:19:13 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69517b9f965a1818a8dfbffb25e560e0bf6a84d522b1dc35557aa9da0ad449f`  
		Last Modified: Fri, 06 Mar 2026 19:19:13 GMT  
		Size: 111.2 KB (111185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23a582f30de3cb0ec39dfb7f205df2531f95cb73311c701ded6a86aa0319d1c`  
		Last Modified: Fri, 06 Mar 2026 19:19:12 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
