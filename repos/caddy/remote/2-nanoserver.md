## `caddy:2-nanoserver`

```console
$ docker pull caddy@sha256:041e2132c0a60a20f8023de716197c7b3edcb0633edb4f7f4c226f86759dd157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `caddy:2-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull caddy@sha256:eb2051374d6156f727ea1c3c6918ca85da7984ca78c3e4868c467a7f8f82b0c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217632617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb9a9e38bbbb703c8bc82d711a3ad793e1b308636cdc5da5a75609a079bacde`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:14:59 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 14 Apr 2026 22:15:01 GMT
RUN cmd /S /C #(nop) COPY file:11e7667c1584a79af7b586b90aae7543497c229bc94afaf5bb80d10c2bc7791e in c:\caddy.exe 
# Tue, 14 Apr 2026 22:15:04 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 14 Apr 2026 22:15:06 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 14 Apr 2026 22:15:07 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Apr 2026 22:15:07 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 14 Apr 2026 22:15:08 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.2
# Tue, 14 Apr 2026 22:15:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Apr 2026 22:15:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Apr 2026 22:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Apr 2026 22:15:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Apr 2026 22:15:12 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Apr 2026 22:15:12 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Apr 2026 22:15:13 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Apr 2026 22:15:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 14 Apr 2026 22:15:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 14 Apr 2026 22:15:15 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 14 Apr 2026 22:15:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 14 Apr 2026 22:15:18 GMT
RUN caddy version
# Tue, 14 Apr 2026 22:15:19 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd326daa70cd33735b880a50283e5eac7bf4e34b02ffb1bba11439318b8bd5`  
		Last Modified: Tue, 14 Apr 2026 22:15:28 GMT  
		Size: 72.7 KB (72697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a101f4532bfd0f3d8985c78e0742658b522ee4728df2bec3ac9fdf707723ced`  
		Last Modified: Tue, 14 Apr 2026 22:15:30 GMT  
		Size: 17.3 MB (17318465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a99cd48adcd23aeef127ba8f4714ff502ad2fb1fefd420a61b7cdbe90d09ef3`  
		Last Modified: Tue, 14 Apr 2026 22:15:28 GMT  
		Size: 278.8 KB (278832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6623fdf1b302d0316fef3a27c2eec763173e794b1b96badee6cd489d7692bc38`  
		Last Modified: Tue, 14 Apr 2026 22:15:28 GMT  
		Size: 119.0 KB (119049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183824a5743104b9dd6a31210856bde3c14df147db1201e2d458189f9230cb93`  
		Last Modified: Tue, 14 Apr 2026 22:15:27 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95831947a5d7ce62e980788205c11be40cefc57739816fd9ff43d2c7f24aeff`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffafae5706f2630eec81a56cd11bf53b24e2fd4f84d5d2f99ccb0fac0cc250d4`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8c172f03e9c978e18fa8ff99c91c144a81a60330344f498f02e662fccceaf8`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4e01d1c3eff648d14f92844c33b38d08ebf2ebb64b8b9d74f71220b951f35d`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b66670f7dac567b964b486894c486e6966abdb2f6002e61fb69a0a512c89c`  
		Last Modified: Tue, 14 Apr 2026 22:15:26 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec70237cc536487548ddd571e6c18fb62fb762589ce173eae84cacbd4b159f97`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716e525f7426f125fccb8c78ca2aa312ec2aa117916c4a6229847eb948cbfc6`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6faa875bce1e7fc5ba66d10b75fbf40d11b603b71c726dc5b87555f20108689`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cd8376522700f1719bf48615c42aaf4d1ff7a144fdf92ad838de48a4b44a17`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39187d9bee4c424a98a9ae7426618a1e81e649fcb0adf1a2ee8faa591e891794`  
		Last Modified: Tue, 14 Apr 2026 22:15:24 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7acd2e5b4272caff171acb4ebe080d3ff0f67e11b6f453d5863637f35f8e4f`  
		Last Modified: Tue, 14 Apr 2026 22:15:23 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dcde7cc1f3bb0ecdf15e9775d7dbc7f96e5cfd17f82a27b104461fb20106a7`  
		Last Modified: Tue, 14 Apr 2026 22:15:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cee510540343385465784c69dccaf55a8358f4f4110aeba449feac46a95568`  
		Last Modified: Tue, 14 Apr 2026 22:15:23 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb50fbc8a14868f9c976ad42c2e1c8be13c02398d4221277d7f7cb3e11dc552`  
		Last Modified: Tue, 14 Apr 2026 22:15:23 GMT  
		Size: 110.5 KB (110459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4ce2dfb2f8882e0d3ff565580ca9fc45189846a667340eededc0234ad01766`  
		Last Modified: Tue, 14 Apr 2026 22:15:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull caddy@sha256:9ceedb5d0893913cd34557d8f58c3ffd00e08cb7ed95f5303f7d7f6060f35650
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144861583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884459cd618d2ae6e5dc8df2e88b3db07fe0cca33a731cc6a9f9ea859516ac9a`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:16:48 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Tue, 14 Apr 2026 22:16:54 GMT
RUN cmd /S /C #(nop) COPY file:11e7667c1584a79af7b586b90aae7543497c229bc94afaf5bb80d10c2bc7791e in c:\caddy.exe 
# Tue, 14 Apr 2026 22:16:57 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Tue, 14 Apr 2026 22:17:01 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Tue, 14 Apr 2026 22:17:01 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Tue, 14 Apr 2026 22:17:03 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Tue, 14 Apr 2026 22:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.11.2
# Tue, 14 Apr 2026 22:17:04 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Tue, 14 Apr 2026 22:17:06 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Tue, 14 Apr 2026 22:17:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Tue, 14 Apr 2026 22:17:08 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Tue, 14 Apr 2026 22:17:09 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Tue, 14 Apr 2026 22:17:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 14 Apr 2026 22:17:11 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Tue, 14 Apr 2026 22:17:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 14 Apr 2026 22:17:12 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Tue, 14 Apr 2026 22:17:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Tue, 14 Apr 2026 22:17:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Tue, 14 Apr 2026 22:17:18 GMT
RUN caddy version
# Tue, 14 Apr 2026 22:17:19 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813e27713394538a8bb5e49849ec84b30e4672dc4f080d1c666498888a3636a`  
		Last Modified: Tue, 14 Apr 2026 22:17:28 GMT  
		Size: 76.8 KB (76831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bfcc633b2cf187caeb6f081a73f58b359a19119f55a8958d337ca97d637b0d`  
		Last Modified: Tue, 14 Apr 2026 22:17:30 GMT  
		Size: 17.3 MB (17318452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8058c8717e22906cff4a8886bae913224c5a34998f28cb26957db69244e0dc7f`  
		Last Modified: Tue, 14 Apr 2026 22:17:28 GMT  
		Size: 272.8 KB (272767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a57e82fe893ddfecf888a7b08a7aa518313336a4607a9ea8fb38ef2a5082162`  
		Last Modified: Tue, 14 Apr 2026 22:17:28 GMT  
		Size: 111.3 KB (111289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf7ea858ea4ae18374d3d70c6708f64bba073aab51052e24f7f337aacfb131f`  
		Last Modified: Tue, 14 Apr 2026 22:17:28 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c752f3d47604d74fd9cec3f7c914b68b1a540e3659ed14b7fe256ef55495fc`  
		Last Modified: Tue, 14 Apr 2026 22:17:27 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a3c06cd6472b58f2a98b183aba2158e7248c05c3815ed679fb8b1a4098e4d2`  
		Last Modified: Tue, 14 Apr 2026 22:17:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38ca3c34a735bf5eb93634071b4d5a18a16a6484fe6460a4eec841c04de17e1`  
		Last Modified: Tue, 14 Apr 2026 22:17:26 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76996314fdef12a975d00245f4a2b6e245757a92383a1e49607de810ea78cd87`  
		Last Modified: Tue, 14 Apr 2026 22:17:26 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe4f8f117a5c1e040bc5ab34b7a32daa716a1e3e3a36626826a03b6b8dbf52d`  
		Last Modified: Tue, 14 Apr 2026 22:17:26 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab5f7910cd7d80627c16957c625dadbd39d56c2a307541a14a7ea883d75d8a`  
		Last Modified: Tue, 14 Apr 2026 22:17:25 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e94ff430493c5994a046cd5e07b051aaf2d4be3c1c66b78e9875330e919f3`  
		Last Modified: Tue, 14 Apr 2026 22:17:25 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa60c40bacbe2afacdbc2d95f950627f6961b6881ac7d997b2f2c5c98d7635`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb713341370f94c1154cf747719340ca5b152c7f8aafbec10206ee2f127fb65e`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f443e1efde695acdee9c523eeb059ae61aac60fccaaac4b958a422f1ef0c445f`  
		Last Modified: Tue, 14 Apr 2026 22:17:24 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c6ad341bf6a2ca0fe31df35e85fda7199c1a03afc20bd6745d7ab60e08b15d`  
		Last Modified: Tue, 14 Apr 2026 22:17:23 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e8e8ac9cc2cc5bab43d876a4c1a3b6140fb16d02374d62810fbb6676ff6be1`  
		Last Modified: Tue, 14 Apr 2026 22:17:23 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc6dcbf314e1bc32d3e5460316da4502e512d3f54aa1fe4f62ae1e8b3add4fc`  
		Last Modified: Tue, 14 Apr 2026 22:17:23 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e9c515b93c975130c57b3c7f017533ece7015344c9ebd439a12735e62057a0`  
		Last Modified: Tue, 14 Apr 2026 22:17:23 GMT  
		Size: 110.4 KB (110414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e40625240f4f5ada3b5b5282bf14bd0a1d5a741e5756ebbbd9f24be6b0bc8f`  
		Last Modified: Tue, 14 Apr 2026 22:17:23 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
