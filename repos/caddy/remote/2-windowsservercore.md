## `caddy:2-windowsservercore`

```console
$ docker pull caddy@sha256:02e4ec422a43bbe257c0b6f52bc54f9e391ac2ed078f86fc4d80269ca8ef3533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `caddy:2-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull caddy@sha256:e92a98f9befbcc685cba6014745c4c4e5573d524f98646666afae41fe635a647
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1973514153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c02263e4345786d822a7cbe2109be66b8bbc405dad0088432e203c583cdb8c4`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:37:25 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:37:26 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:37:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:37:53 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:37:54 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:37:54 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:37:55 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:37:56 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:37:57 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:37:58 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:37:59 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:38:00 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:38:01 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:38:02 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:38:03 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:38:21 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:38:21 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3433f0cddf0bf50f831ae26d44034fb9ccdaea63173630b59cbe9dc33860a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:45 GMT  
		Size: 471.5 KB (471467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39aa89107a4c1ac15acc37ba98faa00f98774062e839984cd569c84acccbefa`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903c57abacc03a4132d1914d83b140d91cad6d3f72113588dbb0449668e5459e`  
		Last Modified: Wed, 13 Mar 2024 02:41:47 GMT  
		Size: 15.3 MB (15272331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c505d8db5c54f9f5b13a230f310c78e1daa9f0fa5baa7db6bb4b6f9b2824c64`  
		Last Modified: Wed, 13 Mar 2024 02:41:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02c7783ff4e4ea0351aa496f9316d007b5d39dd7ac091772a53c788cc850835`  
		Last Modified: Wed, 13 Mar 2024 02:41:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2f6f475cd8b631685eb3441f13c0418b595dc3f64fc43f4de103cd270bd07a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c099338186092d8e8a9ee4e1aef2ac6bac6e0e37d05b00acc2519d4828eebc1a`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66be30fd26f10adf7753fc7287726b290417f432503173cc8cfcc37c5970eed5`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdecded462eba57ac719ddeaf73027953397d9470c8d9ce91486b650688448d1`  
		Last Modified: Wed, 13 Mar 2024 02:41:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b196924a8268e867bced4e92552ad7a24d5079dd5d3a5f2d32e98acf5b94ec`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b83e0533daa0143428320795f95f747a318ce9dfaec9c1918dc09ddabff7ce6`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d6f7d580438b0f330c60e990071ee0a7fd2cb8e861b5b3673229aae5f40a97`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3043316cf0d3543d7ad8c2cf29b9f42217a7ff7ee358b9ccf49ec1c2742b40dc`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d07b35dd72d9c89f56d604b5b5ff1096607de0b699a7845b4d4eef4542999`  
		Last Modified: Wed, 13 Mar 2024 02:41:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7138f2320f3eb26befb56422d151646fa73d61b45b1fd7ba1a97e97b12b1794`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dd6eb25db87e92a30fe3a646b0ca820c3a8a855af39f49e9c1239e9e7e8fa8`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff49c00e60e2791dac19058d6bba6e562c80b90859f8e91ae70b474a582042`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28453d92f8177a5ca4103ba031b5f02ceb70269930e8642e8bda358f1eef11`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 289.3 KB (289264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5958cc3ab872a13ea8011a1ae0a2290cefbfb5721bf58c5c16e2a1dfa216aa`  
		Last Modified: Wed, 13 Mar 2024 02:41:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:2a10673838e2beefb539398925457319c1e7800b242f5c261bc40ddd7f16aa33
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2141123401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b000d65334996d09969a3e79ce6304b5ea6811c67eb7add59f0c78b73ba5c`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:34:07 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 13 Mar 2024 02:34:08 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:35:29 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 13 Mar 2024 02:35:30 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 13 Mar 2024 02:35:31 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 13 Mar 2024 02:35:31 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 13 Mar 2024 02:35:32 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 13 Mar 2024 02:35:33 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 13 Mar 2024 02:35:34 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 13 Mar 2024 02:35:35 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 13 Mar 2024 02:35:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 13 Mar 2024 02:35:37 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 80
# Wed, 13 Mar 2024 02:35:38 GMT
EXPOSE 443
# Wed, 13 Mar 2024 02:35:39 GMT
EXPOSE 443/udp
# Wed, 13 Mar 2024 02:35:40 GMT
EXPOSE 2019
# Wed, 13 Mar 2024 02:36:47 GMT
RUN caddy version
# Wed, 13 Mar 2024 02:36:47 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bb323765ff7b405cedec6f88daa8a1c8470f45c358d637c0062cf4c63d7e07`  
		Last Modified: Wed, 13 Mar 2024 02:41:21 GMT  
		Size: 465.6 KB (465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b3f11ec4ee425a6a0b9f5ad200c9193592181f59520c9a80372e647787163a`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ffe491a522455b1d95c1d0d3384188ea361064259fffcadd657bebae4fa934`  
		Last Modified: Wed, 13 Mar 2024 02:41:24 GMT  
		Size: 15.3 MB (15277213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62af40926c0d1a37e6126f41f63533166809b5b54434cf3b53ab5734357e59`  
		Last Modified: Wed, 13 Mar 2024 02:41:20 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a9b1639ec2e8588ca4fd94f87b31b4e30adef3c0ac45ea4ac0e4cdce643d6`  
		Last Modified: Wed, 13 Mar 2024 02:41:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7a48958fcb11d52bb7a65f60d6f322d3326d4f2916e0547b764cbe4fe0eae8`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb36d28260e8ba5549b16a87d121a4d7b0d38f46e1127ee1fd95f2e31e6f2c`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d221a46e4e966da289289be19ac425d0199540bef1d6d7c890ba45ec255e79`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeda3213337ce81d383bcb08c0b241e763185b91a2e180f35c59395e3c0290f`  
		Last Modified: Wed, 13 Mar 2024 02:41:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d7bf5ae3a283a09c7a385afa5160b2d0f1d275fc23e0a1711bf734511fe0b1`  
		Last Modified: Wed, 13 Mar 2024 02:41:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f309d19b55289fe422d64dd24736be59a52f6eba872d8fb1054416f8b5d9c553`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ac1a4021eeee54512dde50b437001408fd1dda9d896f68d38728f7dba8c6c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e117655b528b6e8f7ce8d4d2cb69d41a1735fec0e31e10dc40cddcf0d012be`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5524c6d618843e710fa22d77e57a844c7cdfd68676c809d2d1ecde656c16a81c`  
		Last Modified: Wed, 13 Mar 2024 02:41:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879784be55be2c5d212302ae42232de9bfeaccea0b1398ec0101ef36d542930c`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8aadcc42505eea344cf0504c7312d01033f159e88d6eadab5abb9eefc98a1`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41580c6cc25a82ee1a4de9315ec98ce6e89bd73461a941248648d04292e9ff52`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1261dc2b6b686493c5c3989f8efdd404b912398f6a38933aba80fe65d5d6240c`  
		Last Modified: Wed, 13 Mar 2024 02:41:15 GMT  
		Size: 258.2 KB (258159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856855cc09ca543e8712766ea12d12556af369305babcaf786f620c89c3450d`  
		Last Modified: Wed, 13 Mar 2024 02:41:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
