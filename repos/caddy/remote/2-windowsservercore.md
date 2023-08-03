## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:f39f55e2163b6d39a839be8af2be7a2a2c75f08b8b23fdc85401789c77405e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.4645; amd64
	-	windows version 10.0.20348.1850; amd64

### `caddy:2-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull caddy@sha256:244e9ea648e66390681506ed4f38cc4443aa354d1610f9b378bcd02d1fd2cf3a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955706168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50540779ca9094da63ce195b82e5465f7d70989caa8f2eded984c185762b3663`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Aug 2023 21:16:24 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 03 Aug 2023 21:16:25 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:17:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('69d2d73c2514ab5ce4f6a60489c79ce4da0e1d4302c85ab584d0a7a7fd0d034bfe5a5caab78c96ac3383ddd7d2e12c3c41fb47c4716909d2a78d448b0289ccec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 03 Aug 2023 21:17:35 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 03 Aug 2023 21:17:35 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 03 Aug 2023 21:17:36 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:17:37 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:17:38 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:17:39 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:17:39 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:17:40 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:17:41 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:17:42 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:17:43 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:17:43 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:17:44 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:17:45 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:18:44 GMT
RUN caddy version
# Thu, 03 Aug 2023 21:18:44 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726f37fb0b4083f5193485e0d3eb3b3b22f42142f66c17aca0500f5d9bb746e6`  
		Last Modified: Thu, 03 Aug 2023 21:23:02 GMT  
		Size: 477.3 KB (477339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6eb2f82f2289bf967067e8f54468abfa74d0c560c7ff4ee0f24e17b5c61118`  
		Last Modified: Thu, 03 Aug 2023 21:23:02 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9910ce4e2dbdebf58561c3b79500d00fc0b10a1287e2d6c48a59fd53cd1dafb`  
		Last Modified: Thu, 03 Aug 2023 21:23:05 GMT  
		Size: 15.2 MB (15245835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bf5da4d48ea65ff2f357378115fba0f0820f95ad2e6f0ee28b4915d83a311a`  
		Last Modified: Thu, 03 Aug 2023 21:23:01 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed924e132f53161a3eee91723a9ad59a2131996c4a47ebaeffc7c6e10e5ccdf7`  
		Last Modified: Thu, 03 Aug 2023 21:23:00 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71109424ce24da154412db82bfb418de982d76dfd9f12848b5acfcff7e94c477`  
		Last Modified: Thu, 03 Aug 2023 21:23:00 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d33557b82e542b2f3a8ffae2b0f30e1e99e24d8bd68607565d9ffdde35fb578`  
		Last Modified: Thu, 03 Aug 2023 21:23:00 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d3774f6dbd2be4ba8ac48e3cb6190dcbd59b2a0851cd6f04ba52b006e6d07a`  
		Last Modified: Thu, 03 Aug 2023 21:22:59 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ffbcf8830dfcda713001c480020fef263d6ab48d71f78eff5f0f379bda6671`  
		Last Modified: Thu, 03 Aug 2023 21:22:59 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aca4d6a6c867fbdb7342667fffec74374f3713c0bd5953a435945184a732a96`  
		Last Modified: Thu, 03 Aug 2023 21:22:58 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d5a52d2c79318e51fa0e8b49d03066411ae79bd7b4c7183209f965ad2b7db`  
		Last Modified: Thu, 03 Aug 2023 21:22:58 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a5ea41d6995173c219170336c2f2508f3c513240c5c9beec697bac8750c4ee`  
		Last Modified: Thu, 03 Aug 2023 21:22:58 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c72b63c2f9d7d5012f78b6da71eed80f74bc25d14c1864697c63c375c76cc41`  
		Last Modified: Thu, 03 Aug 2023 21:22:58 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f98023d7c0698dd995c79b4ab8245804816d123d6bd4f296e0fcc775bd7497`  
		Last Modified: Thu, 03 Aug 2023 21:22:57 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e132135b4ecd518d7b016af2cd783c553c4805e458ca2ce5eff4a79d30ba20a0`  
		Last Modified: Thu, 03 Aug 2023 21:22:56 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd22701b68006012181ebe5b8b726bf4e18afae02e2811719add8702bae39d4`  
		Last Modified: Thu, 03 Aug 2023 21:22:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd852e11407bf1fef45700213ba9857caaef051c7d5e55a0c3632b0186a4b0`  
		Last Modified: Thu, 03 Aug 2023 21:22:56 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647b0fad50d9473598d50c3a2ac34267923778f155f20a4be40087605e8ee28d`  
		Last Modified: Thu, 03 Aug 2023 21:22:56 GMT  
		Size: 270.0 KB (269978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7826c418b559608173421f5ace0ca76d18eb4e81f42dd8ba13a0d38ee05211`  
		Last Modified: Thu, 03 Aug 2023 21:22:56 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.20348.1850; amd64

```console
$ docker pull caddy@sha256:61759f5a3d1ce10d853a4094cf6408335d1433fdc548bbb5df47112f7f42b37c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1753439348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fcc9fb8974b4428fbaf1925336b5f32b2042050f4668ab2477eeb473ce44ac`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 03 Aug 2023 21:19:26 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/5910351159c2995a9a1c911d7879de6ff598d905/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Thu, 03 Aug 2023 21:19:27 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 03 Aug 2023 21:19:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.2/caddy_2.7.2_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('69d2d73c2514ab5ce4f6a60489c79ce4da0e1d4302c85ab584d0a7a7fd0d034bfe5a5caab78c96ac3383ddd7d2e12c3c41fb47c4716909d2a78d448b0289ccec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Thu, 03 Aug 2023 21:19:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Thu, 03 Aug 2023 21:19:54 GMT
ENV XDG_DATA_HOME=c:/data
# Thu, 03 Aug 2023 21:19:54 GMT
LABEL org.opencontainers.image.version=v2.7.2
# Thu, 03 Aug 2023 21:19:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Thu, 03 Aug 2023 21:19:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Thu, 03 Aug 2023 21:19:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Thu, 03 Aug 2023 21:19:57 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Thu, 03 Aug 2023 21:19:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Thu, 03 Aug 2023 21:19:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 03 Aug 2023 21:20:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Thu, 03 Aug 2023 21:20:01 GMT
EXPOSE 80
# Thu, 03 Aug 2023 21:20:01 GMT
EXPOSE 443
# Thu, 03 Aug 2023 21:20:02 GMT
EXPOSE 443/udp
# Thu, 03 Aug 2023 21:20:03 GMT
EXPOSE 2019
# Thu, 03 Aug 2023 21:20:18 GMT
RUN caddy version
# Thu, 03 Aug 2023 21:20:18 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e9b6bcbb67de5b41933b793abd6c9589609ac3a81f57c9a9769774bc7d2f0b`  
		Last Modified: Thu, 03 Aug 2023 21:23:28 GMT  
		Size: 492.7 KB (492678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0360f78127e07566726f205a72b71f42ef1e3da4913f6a887e32f2e0ba4d366`  
		Last Modified: Thu, 03 Aug 2023 21:23:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af128dc74644b16188a4cb9b4fb19435d69d3d10b097722c5712897fa181dce7`  
		Last Modified: Thu, 03 Aug 2023 21:23:31 GMT  
		Size: 15.3 MB (15252961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89696f04e1e31855a60e95e326f06ed1916b2eb8b24016fb305d5b3cb24d9787`  
		Last Modified: Thu, 03 Aug 2023 21:23:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c23c5b8a90c440aae7423d54ec85e7e461c6877760b74873c27e9031c3f17`  
		Last Modified: Thu, 03 Aug 2023 21:23:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e57861cb9b72f7b636fb59a66e8da9be9aad09c3a064555f832560b91a908ef`  
		Last Modified: Thu, 03 Aug 2023 21:23:26 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a8802e26c708c1db71aee23e5ff8f662081a32c6ffb23887861289d3fa76c4`  
		Last Modified: Thu, 03 Aug 2023 21:23:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c621782c599e094a65087cbde3d0ccdaac54a9fdbca938411769a0dbfad9fd33`  
		Last Modified: Thu, 03 Aug 2023 21:23:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cc33619413c8259d35279c8f94f76b2f474920a1ece27c4941f511824d90fd`  
		Last Modified: Thu, 03 Aug 2023 21:23:26 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf2fce68a0a9aa50c6d7e2bb20cc8edda4d7138775c234c97773758330be771`  
		Last Modified: Thu, 03 Aug 2023 21:23:24 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d64f2b86ca83abd07dbf404641950ae47023547eb2be1738a4505fca9704a7`  
		Last Modified: Thu, 03 Aug 2023 21:23:24 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dbbc7aabf9f4e53a0434c7f7929e43b33d6e867cda77eeaa9a6a022bd5ba1c`  
		Last Modified: Thu, 03 Aug 2023 21:23:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7469da2db14b8c19ce07788ab3b97af9ddeb68a23da4d42798bffdc185cc7ebf`  
		Last Modified: Thu, 03 Aug 2023 21:23:24 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5e78924954f90ddeb5c34801adcf26789cd0522921ef88796a7c28dbf931c6`  
		Last Modified: Thu, 03 Aug 2023 21:23:24 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f245fed41d1a5742e9eae5db6128bdf5c83e6887f4ec020e452b5343b9a992`  
		Last Modified: Thu, 03 Aug 2023 21:23:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92f20efc54b02c58faef830e554c2bdab85b22b0176f17fdd2c39a5e9ae700d`  
		Last Modified: Thu, 03 Aug 2023 21:23:22 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d53fc9e8da0df2da9a6755505aaefa0d96f527339c282fc9efe0229912dc6`  
		Last Modified: Thu, 03 Aug 2023 21:23:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e397d6aa6ede289022b24d854c6b0598776f1e69bacdfc960065b4fe37ea39`  
		Last Modified: Thu, 03 Aug 2023 21:23:22 GMT  
		Size: 306.3 KB (306273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa04fefc0f732dd54239c7498fb47296762fe74c6ea8ada17d09683a9a59fb5f`  
		Last Modified: Thu, 03 Aug 2023 21:23:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
