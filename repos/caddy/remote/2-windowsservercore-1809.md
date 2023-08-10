## `caddy:2-windowsservercore-1809`

```console
$ docker pull caddy@sha256:40d5f0aa53bb62f81ccb8625ca40ae2b0057b977b8432daa5d3a76079b9737e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `caddy:2-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull caddy@sha256:1b4a86d284b971594d7e30ef09451be59ba84514b612c87b6406e2dfb8e9e23f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2011958834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5f48eae2f949ec09ad9f70ff2c2626318e07111bea5b6622116482ac991b0`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 02:59:41 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 10 Aug 2023 02:59:41 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 10 Aug 2023 03:00:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('69d2d73c2514ab5ce4f6a60489c79ce4da0e1d4302c85ab584d0a7a7fd0d034bfe5a5caab78c96ac3383ddd7d2e12c3c41fb47c4716909d2a78d448b0289ccec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 10 Aug 2023 03:00:58 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 10 Aug 2023 03:00:59 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 10 Aug 2023 03:01:00 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 10 Aug 2023 03:01:00 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 10 Aug 2023 03:01:01 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 10 Aug 2023 03:01:02 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 10 Aug 2023 03:01:03 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 10 Aug 2023 03:01:03 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 10 Aug 2023 03:01:04 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 10 Aug 2023 03:01:05 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 10 Aug 2023 03:01:06 GMT
EXPOSE 80
# Thu, 10 Aug 2023 03:01:06 GMT
EXPOSE 443
# Thu, 10 Aug 2023 03:01:07 GMT
EXPOSE 443/udp
# Thu, 10 Aug 2023 03:01:08 GMT
EXPOSE 2019
# Thu, 10 Aug 2023 03:03:10 GMT
RUN caddy version
# Thu, 10 Aug 2023 03:03:11 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907ddb8e2b3b8f440ec855971bf77d521900d3faecd1816d7146d89f1c78f408`  
		Last Modified: Thu, 10 Aug 2023 03:07:15 GMT  
		Size: 469.4 KB (469388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d430330f12b22fcc17a5d114d51ba3bb8e62a55f87b67f939d18651c226f927`  
		Last Modified: Thu, 10 Aug 2023 03:07:15 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd493f43c2fb25a7c8540ea353a098f784a6e8d5fe4e9d070e4a1de796cde96c`  
		Last Modified: Thu, 10 Aug 2023 03:07:18 GMT  
		Size: 15.2 MB (15241515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95b32f0fb8252db266318cca24c13f5eea8b8b3c19405b92f1a8b9199e39c5d`  
		Last Modified: Thu, 10 Aug 2023 03:07:14 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7dbc1767506f0f3f5b4d3a9671f97a723014ae1e38cf8056f6257db7917a88`  
		Last Modified: Thu, 10 Aug 2023 03:07:13 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7905b1f85b201367c5a62618ddc55da9a60cbb3da1da40ab60a88c125a5956`  
		Last Modified: Thu, 10 Aug 2023 03:07:13 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce34081b153cf49ce89b2ff4fc81f54a648cefc5d2dbb0f60048b94ba10f43b`  
		Last Modified: Thu, 10 Aug 2023 03:07:12 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9622cc1048f5f7259d3263b67dd386c5d70ae4cf0a358c33deb3df8cdb316efd`  
		Last Modified: Thu, 10 Aug 2023 03:07:12 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b1ca0970bf360a0627a1deae2985b658f54b41758f12f4e5448ed1aee3bc82`  
		Last Modified: Thu, 10 Aug 2023 03:07:12 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503770a8fe554599aa8e6413082b7cb24d7f1faa328deaf28b34ddb2a294972b`  
		Last Modified: Thu, 10 Aug 2023 03:07:11 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea5eee99969c433a1c2f4d0f7fdc838185350144b9d3f20888c2a53cc6f3563`  
		Last Modified: Thu, 10 Aug 2023 03:07:11 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675093fb34c31fff953a92ee1831f09679783e7d3e1d9ff40a962f346d1dc581`  
		Last Modified: Thu, 10 Aug 2023 03:07:10 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fd64685610dd5572f21efe3fae8cb13537c9deb6693caf4097bf9ec3b4dabe`  
		Last Modified: Thu, 10 Aug 2023 03:07:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e52aaf0b1acca0c4a9fbb2a60e5ce4bca2c119fbb3bbd86658186b23e3202`  
		Last Modified: Thu, 10 Aug 2023 03:07:10 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29819bc504b56dacdb0df898ee58e26d8097802c0a5578cd14d4e3ed0655bde7`  
		Last Modified: Thu, 10 Aug 2023 03:07:09 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2157a412d53cd6d3174744de6c1cf5cb0dd03274fe9b36f749525867e4b9bd2`  
		Last Modified: Thu, 10 Aug 2023 03:07:08 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cfbf0b65ccf78eb536c8a23f0b92fa148268c1fa4a39c1b19c7d9310e53b8d`  
		Last Modified: Thu, 10 Aug 2023 03:07:08 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faedca764204aa914e83a3721476c9a6a7f8177d057021e5a1debb81a436808`  
		Last Modified: Thu, 10 Aug 2023 03:07:09 GMT  
		Size: 268.6 KB (268640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86622825a44d72176deccdf0a5e4c9127ebf8f2591211cbdae585e9977363e8`  
		Last Modified: Thu, 10 Aug 2023 03:07:08 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
