## `caddy:windowsservercore`

```console
$ docker pull caddy@sha256:399999da333b248fef2da843177c302602a2e3f939228d52df499d197ea08cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `caddy:windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull caddy@sha256:b4de45abdf801e6fe4e627d4a9146c7f3822666f9795f1fe35921da33d3b5920
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2015415021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c537b274bb6928ea6772a745ddf910765f287696f3d596a64a2aef5bb3a49`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:59:40 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:59:41 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 02:00:11 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 02:00:12 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 02:00:13 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 02:00:13 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 02:00:14 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 02:00:15 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 02:00:16 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 02:00:17 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 02:00:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 02:00:19 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 02:00:20 GMT
EXPOSE 80
# Wed, 10 Apr 2024 02:00:21 GMT
EXPOSE 443
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 02:00:22 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 02:00:42 GMT
RUN caddy version
# Wed, 10 Apr 2024 02:00:43 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9cb628e4a7ceb9e124a728aba733c7b7837d0fe602c1af1c86af5ba7db1afe`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 462.4 KB (462386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe6244a1b7fd00d56255f78e7951d14811b06f10e069d90e75458e8f5198d6a`  
		Last Modified: Wed, 10 Apr 2024 04:39:53 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd5220e89ae5a44a14c920f948c28b3238c83307ad30f5955882930d72a23b`  
		Last Modified: Wed, 10 Apr 2024 04:39:56 GMT  
		Size: 15.3 MB (15272884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8711ac4c34fb1beb0cb9e799010a337864f252ea20a91c74e9ffb9dc4dd8f4`  
		Last Modified: Wed, 10 Apr 2024 04:39:52 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1bffa02c717094b56095d1f166aa11c19ba43f7481d7673313c862126f3434`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554dc514103b8d140d5ab4e9437abe3875ce416cd9a69161836f9676d14b650`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f583dd206e697664bb89b8647ac1fe5d98933b1d6540b249433dae65d02dd09`  
		Last Modified: Wed, 10 Apr 2024 04:39:51 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35fa3d4abc62509fa7c8c8b31d11482d23090a1f7e45393d43cbde05d0cd7e9`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f688302923c46000c0526a060b43160db4d9314cbd342a3fc31620052ceaa`  
		Last Modified: Wed, 10 Apr 2024 04:39:50 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e052187f5af8dbfaa36325485d886d7d47bbe36c18a5789d95efea81dfbf12`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea08dd4e4a398c33acb70cc8863ba300fad5cbf499840ed420b14ce06717f83`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc50e94c9c5e82f27b76ddd1796de52ee67ba64c275a531ee0d38c08757baf9e`  
		Last Modified: Wed, 10 Apr 2024 04:39:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af1603a6bd4dacbf08b4c974a5db996c73e892cbe440e2d5339aa355847e5a0`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaaeba50589b199d8e988596dada19daaec59e8b26f7835e17a29fff8ac88f7`  
		Last Modified: Wed, 10 Apr 2024 04:39:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b4695f6c339c5917ad1b57b3db1345b8cc1ac6b4e03d56d5f1de12f8e249a2`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d5e030bf8b034231beb875dd3a70af4fcf82b6350b60b23a72cef369792a29`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9280f84d3173ce915aa30f755697f993ca2d484caa9f8cd42334927563008d`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e2de6ed998eca032f334174172a69a2345072eda08fddd105b73a6e6238c81`  
		Last Modified: Wed, 10 Apr 2024 04:39:47 GMT  
		Size: 282.0 KB (282045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426ed15821e9616ced2fee524860d8e5554c359d0332601d4e035474c8a54964`  
		Last Modified: Wed, 10 Apr 2024 04:39:46 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:650f5144a6e8b1d947f54c017a1002956e096891718dc7edf9aa8661be3f82ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2180450650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e356a94cf89f9d5eb0399e9f2ae7bbba82bc08e09f5dbc1d964352dfa2497f34`
-	Default Command: `["caddy","run","--config","\/etc\/caddy\/Caddyfile","--adapter","caddyfile"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:55:53 GMT
RUN mkdir /config;     mkdir /data;     mkdir /etc/caddy;     mkdir /usr/share/caddy;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/config/Caddyfile"         -OutFile "/etc/caddy/Caddyfile";     Invoke-WebRequest         -Uri "https://github.com/caddyserver/dist/raw/cd39178d252a610fee6aa8465c787d9c780007a2/welcome/index.html"         -OutFile "/usr/share/caddy/index.html"
# Wed, 10 Apr 2024 01:55:54 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 10 Apr 2024 01:57:24 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/caddy/releases/download/v2.7.6/caddy_2.7.6_windows_amd64.zip"         -OutFile "/caddy.zip";     if (!(Get-FileHash -Path /caddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b2321473be1da500a8f6e4276aed03b11946e3758b792a3e9ba50c07246456d64d7da931d6d58be43e6d3cfd07c1ad68f6838df8e090bd5d212224a9bf94daec')) { exit 1; };     Expand-Archive -Path "/caddy.zip" -DestinationPath "/" -Force;     Remove-Item "/caddy.zip" -Force
# Wed, 10 Apr 2024 01:57:25 GMT
ENV XDG_CONFIG_HOME=c:/config
# Wed, 10 Apr 2024 01:57:26 GMT
ENV XDG_DATA_HOME=c:/data
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.version=v2.7.6
# Wed, 10 Apr 2024 01:57:27 GMT
LABEL org.opencontainers.image.title=Caddy
# Wed, 10 Apr 2024 01:57:28 GMT
LABEL org.opencontainers.image.description=a powerful, enterprise-ready, open source web server with automatic HTTPS written in Go
# Wed, 10 Apr 2024 01:57:29 GMT
LABEL org.opencontainers.image.url=https://caddyserver.com
# Wed, 10 Apr 2024 01:57:30 GMT
LABEL org.opencontainers.image.documentation=https://caddyserver.com/docs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.vendor=Light Code Labs
# Wed, 10 Apr 2024 01:57:31 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Wed, 10 Apr 2024 01:57:32 GMT
LABEL org.opencontainers.image.source=https://github.com/caddyserver/caddy-docker
# Wed, 10 Apr 2024 01:57:33 GMT
EXPOSE 80
# Wed, 10 Apr 2024 01:57:34 GMT
EXPOSE 443
# Wed, 10 Apr 2024 01:57:35 GMT
EXPOSE 443/udp
# Wed, 10 Apr 2024 01:57:36 GMT
EXPOSE 2019
# Wed, 10 Apr 2024 01:58:56 GMT
RUN caddy version
# Wed, 10 Apr 2024 01:58:57 GMT
CMD ["caddy" "run" "--config" "/etc/caddy/Caddyfile" "--adapter" "caddyfile"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ffc757feed37e26b36ff35084f4357219272c3ef8ce663a0db97763750bec`  
		Last Modified: Wed, 10 Apr 2024 04:39:29 GMT  
		Size: 465.0 KB (465007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f41e339dc34abe966a19ca999fece15bcf0a5e9eb2d36d4d42b84482e8e2ba`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac8e68361bdc1deb2d5d4e50f2da825b25f026f558a03aeeba18d6c7665e654`  
		Last Modified: Wed, 10 Apr 2024 04:39:32 GMT  
		Size: 15.3 MB (15281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05561518ae50169e6e15468669f8195d9b2ee80d945dd94c107d20afda067318`  
		Last Modified: Wed, 10 Apr 2024 04:39:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0720408b82b77dc7b0d925d39741de50fe2f9139768729af189a0f783b43519b`  
		Last Modified: Wed, 10 Apr 2024 04:39:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d8585bb3ff3b6a72b43181fc6df1c46ce88f6393295f32d2315e71c85e7295`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177da9a277ef013596e849aa2ea825a25dddcec2db12d81c6a4ab6fa02e77e57`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4686dffa2d26bcedea0a3b07e3d11640141e4a3888ddca8fc167fce49a67e102`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7411e6d276896da1fd4087fb7dbbe4e2169637862d1bee25144443263947ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966957575920790399f90fd33923b9cb27715dc7dd38e430480922326f86e953`  
		Last Modified: Wed, 10 Apr 2024 04:39:25 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa479db7e2e01c3cdda82927bbd2250f6933c5e4f6d67f09b4f090c26df209ce`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173767522133c716cc5b0c32c5c8778faa06e95a3933bab867e4569bb468420`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a488b5ddbaaac25b5ac6ce9375b9c9eb44e109874b5cd47d7f6591a446084bb`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27825614feb810c19f64b918a625f414d9f32098460aefcc9dad624bd2be669`  
		Last Modified: Wed, 10 Apr 2024 04:39:24 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcc1e73eb545e48d76e61fd1029ab3a682c27085f1b3d23b2e7be300cd8eca8`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef2713b7318664d7438093b75892a477ec691872f2c8fb13408d4d27d9bddd9`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce420a03b259096e6668f2765ce31ad5694523c86afe5c81bc0277d8b2bc861`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa1c6f084d5ad95cabb52b0d9aaed5e906928249958cb374cf25fe5e51e921`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 253.5 KB (253500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d599502ec7d608e46d6398aebafdee3aea525c5a3a58d826220dd06d128bb939`  
		Last Modified: Wed, 10 Apr 2024 04:39:22 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
