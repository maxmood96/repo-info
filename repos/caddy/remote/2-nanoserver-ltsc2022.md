## `caddy:2-nanoserver-ltsc2022`

```console
$ docker pull caddy@sha256:57cd9a13c630b519ce90398981f4c554b60bb1fecb4946437fa9b6fde326cddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `caddy:2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull caddy@sha256:05efcf3615cc2bd643c367a30dfcd58d9511c41c06076876464615545a7b60a7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143389539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7870f4e001e2e8328366efd9964f76e384ad6fd7ad5db41f225c1f7a91bba0f0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 00:15:26 GMT
RUN cmd /S /C mkdir c:\config && mkdir c:\data && mkdir c:\etc\caddy && mkdir c:\usr\share\caddy
# Wed, 11 Feb 2026 00:15:33 GMT
RUN cmd /S /C #(nop) COPY file:32cf40eadbbb089db5d2a89aab3783b917db3d218ef99bdd6915c6b4af650c32 in c:\caddy.exe 
# Wed, 11 Feb 2026 00:15:39 GMT
RUN cmd /S /C curl -fsSL -o c:\etc\caddy\Caddyfile https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/config/Caddyfile
# Wed, 11 Feb 2026 00:15:41 GMT
RUN cmd /S /C curl -fsSL -o c:\usr\share\caddy\index.html https://github.com/caddyserver/dist/raw/33ae08ff08d168572df2956ed14fbc4949880d94/welcome/index.html
# Wed, 11 Feb 2026 00:15:42 GMT
RUN cmd /S /C #(nop)  ENV XDG_CONFIG_HOME=c:/config
# Wed, 11 Feb 2026 00:15:42 GMT
RUN cmd /S /C #(nop)  ENV XDG_DATA_HOME=c:/data
# Wed, 11 Feb 2026 00:15:43 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.version=v2.10.2
# Wed, 11 Feb 2026 00:15:43 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.title=Caddy
# Wed, 11 Feb 2026 00:15:44 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 11 Feb 2026 00:15:44 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 11 Feb 2026 00:15:45 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 11 Feb 2026 00:15:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 11 Feb 2026 00:15:46 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 11 Feb 2026 00:15:47 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 11 Feb 2026 00:15:47 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 00:15:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 443
# Wed, 11 Feb 2026 00:15:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 443/udp
# Wed, 11 Feb 2026 00:15:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 2019
# Wed, 11 Feb 2026 00:15:55 GMT
RUN caddy version
# Wed, 11 Feb 2026 00:15:56 GMT
RUN cmd /S /C #(nop)  CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9867e9a6a7cde8a67a2dbc8d1a05778b398251f6c3b7db1a0f94ad597f149a0`  
		Last Modified: Wed, 11 Feb 2026 00:16:05 GMT  
		Size: 73.6 KB (73566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e2d918996b28fe98425d978b062d534feff2a932826c5bffb53d7a3dc7914`  
		Last Modified: Wed, 11 Feb 2026 00:16:07 GMT  
		Size: 16.2 MB (16217754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacb92486f804119eb898ee5569b08e3db4f46466a0b200b0884d2882a9f162a`  
		Last Modified: Wed, 11 Feb 2026 00:16:04 GMT  
		Size: 172.2 KB (172171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83161973e2c321f4a624f8feaec75d8bfb759fefffc25785c3a2c11d60fc58c`  
		Last Modified: Wed, 11 Feb 2026 00:16:04 GMT  
		Size: 132.4 KB (132386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45d1e6362f1beffc05c88e68a3fa8062d1d85890cc131fe7bdf5deffb2df0f`  
		Last Modified: Wed, 11 Feb 2026 00:16:04 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b0140498e4aed5dcc9b621543ae328d4907680dd4fd68bf1c15c3530989ea5`  
		Last Modified: Wed, 11 Feb 2026 00:16:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9bcc8cd428d97bbafa969bb9ef08ca9a6da00080e294884ab0b037b0743c19`  
		Last Modified: Wed, 11 Feb 2026 00:16:03 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf99d127c34576a63c8fad6177eda3f9abbb348dd905a25cd559538face5af7`  
		Last Modified: Wed, 11 Feb 2026 00:16:03 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6893070eb54cf6bda1c75aaf60d8298e23a1f34e8ecd0add28496a6a19a1ae71`  
		Last Modified: Wed, 11 Feb 2026 00:16:03 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e681da8bcbe3bdcb49f9ce3ac56013a64eae4f0787aed744c83af3e0af1ac5`  
		Last Modified: Wed, 11 Feb 2026 00:16:03 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53aca82439fe5245986e2567dd76df610e348319b303e9096d68447b6b736270`  
		Last Modified: Wed, 11 Feb 2026 00:16:01 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2886ea13948800f2e309ed0ed69c28c2dc0a5c6b3144b6846a51a02b2fe2cf`  
		Last Modified: Wed, 11 Feb 2026 00:16:01 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb561160889ea9faac89e2ccca2db745cbc029661be4cd611614efa7380ee6`  
		Last Modified: Wed, 11 Feb 2026 00:16:01 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e3e3c01df60bb5d54fe085fc5c9f0fc52c58fa54ff8d2e95b4f0b762b8f05a`  
		Last Modified: Wed, 11 Feb 2026 00:16:01 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d897c9277333406fd9f9a986a2023896423a561004c8f921ff84e1f4c5d678`  
		Last Modified: Wed, 11 Feb 2026 00:16:01 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9772feb3f384baf0ef3c29aa6518f101a0fc274c3fdf0fc75716d49404ac301e`  
		Last Modified: Wed, 11 Feb 2026 00:16:00 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f5d3dee9484ef151f11c38a34df4df80774685695f562eed4603a0d61f4ee4`  
		Last Modified: Wed, 11 Feb 2026 00:16:00 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c542d8946373aab1c1e37170fdb8ceceedaf0a6a80404d6d820b7708dc63d1f5`  
		Last Modified: Wed, 11 Feb 2026 00:16:00 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3fd0d343aa88b0f2427f64ff839cba2b395ddbd64b79d84540cbce528e7848`  
		Last Modified: Wed, 11 Feb 2026 00:16:00 GMT  
		Size: 132.0 KB (131952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e99140adab9208b7b1d963fe9222bd18ec8f95bf2cb6d6b74f2a726f56dcca`  
		Last Modified: Wed, 11 Feb 2026 00:16:00 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
