<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.14`](#nats2-alpine314)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2-windowsservercore-ltsc2016`](#nats2-windowsservercore-ltsc2016)
-	[`nats:2.6`](#nats26)
-	[`nats:2.6-alpine`](#nats26-alpine)
-	[`nats:2.6-alpine3.14`](#nats26-alpine314)
-	[`nats:2.6-linux`](#nats26-linux)
-	[`nats:2.6-nanoserver`](#nats26-nanoserver)
-	[`nats:2.6-nanoserver-1809`](#nats26-nanoserver-1809)
-	[`nats:2.6-scratch`](#nats26-scratch)
-	[`nats:2.6-windowsservercore`](#nats26-windowsservercore)
-	[`nats:2.6-windowsservercore-1809`](#nats26-windowsservercore-1809)
-	[`nats:2.6-windowsservercore-ltsc2016`](#nats26-windowsservercore-ltsc2016)
-	[`nats:2.6.1`](#nats261)
-	[`nats:2.6.1-alpine`](#nats261-alpine)
-	[`nats:2.6.1-alpine3.14`](#nats261-alpine314)
-	[`nats:2.6.1-linux`](#nats261-linux)
-	[`nats:2.6.1-nanoserver`](#nats261-nanoserver)
-	[`nats:2.6.1-nanoserver-1809`](#nats261-nanoserver-1809)
-	[`nats:2.6.1-scratch`](#nats261-scratch)
-	[`nats:2.6.1-windowsservercore`](#nats261-windowsservercore)
-	[`nats:2.6.1-windowsservercore-1809`](#nats261-windowsservercore-1809)
-	[`nats:2.6.1-windowsservercore-ltsc2016`](#nats261-windowsservercore-ltsc2016)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.14`](#natsalpine314)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)
-	[`nats:windowsservercore-ltsc2016`](#natswindowsservercore-ltsc2016)

## `nats:2`

```console
$ docker pull nats@sha256:ac522b93125cafb92647e0c2154f3d84c626eae402ae181227f55073c8d02957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2183; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:f9fb49bcb658924ee2b299455aa09a1574b0edd78a04e157ce90b6c300c67fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:29e48bbbfabc68bd286161dd7b59b86ae9877601ba9a88578fcefa440f7f0434
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b274482e0b37c592f58b2c2b13db977af601c57886e25a1d2c502bd4d37e191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:20:16 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:20:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:20:19 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:20:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ed26ecc69fe2112cec367d3ba1751ac3f5ee981612711832d5e3c0efe0be9d`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 4.8 MB (4837177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4f7d9ca9e69cf94643d7c04aeeec199c0ac3e04d418a3e93cc08d47c74780`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76f2651885e7ca41e0f02191fa386cb990fb9e0d0d7c8ac3f88c1fef6d9fac`  
		Last Modified: Wed, 22 Sep 2021 18:21:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a34ac0e31ba3a92b96600275cecf905613b5787a2abdb52e17c0376a6ce05ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7129168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d219fd32cfde7b620cd71920812305af0ec015ab9d4abc91a3310197786348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:49:41 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:49:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:49:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:49:47 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d2a30e1afb94108b4740597e03e612718f5459f533e4d9c4317ebb677ea7f`  
		Last Modified: Wed, 22 Sep 2021 18:51:56 GMT  
		Size: 4.5 MB (4500751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77ac3089b37eeef71ddc37c1b1e00b7e9c5e78d3fa2e06fde1c6da51397af0`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77690a748c6dd95f7fb19c68f9ff0d403ab5b71b6c9644baffb81f40e95e661c`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:972ab950f2b66e74d87d22da4b1839d39668d5edd9101b890132a231497292eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e52058719acb3fa32fb129feb81f0056b2a7736696b0694669b38a2978d60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 21:32:10 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 21:32:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 21:32:17 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 21:32:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f3df2cbc3c87820b00184dca6f1f0fc56066b82a951efe785873912615010`  
		Last Modified: Wed, 22 Sep 2021 21:34:28 GMT  
		Size: 4.5 MB (4494903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac9dabd3dd6b459696ed61905b261fc5d2119025e1a4f11e4f28ac3148b5eb`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3893e6935065d5383621afd73fa5b94df41b088b8a86c1d0bc95fb287a88ed2c`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b3d4a84a592a481ce06edda2e809e1eb0d816832b4675bc3dbd4839829108c77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7160174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce75dadb60225019e9a3fdd6343ba2eaedfe3632f8c39a5fb677701ea67ce1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 19:05:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 19:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 19:06:02 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 19:06:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f7295ad0852b3a6a04040d1e7caff544aa6b162e8ebf10cd1275d1fc84d7a`  
		Last Modified: Wed, 22 Sep 2021 19:07:11 GMT  
		Size: 4.4 MB (4447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0ad901f967d763a163de035129a0507cebce7b1f2e72a73f56361210914ce`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c5bd7249eaa792fd6e725e8170fa00df0cd00b28ec5cfee698c8643177a52`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.14`

```console
$ docker pull nats@sha256:f9fb49bcb658924ee2b299455aa09a1574b0edd78a04e157ce90b6c300c67fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:29e48bbbfabc68bd286161dd7b59b86ae9877601ba9a88578fcefa440f7f0434
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b274482e0b37c592f58b2c2b13db977af601c57886e25a1d2c502bd4d37e191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:20:16 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:20:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:20:19 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:20:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ed26ecc69fe2112cec367d3ba1751ac3f5ee981612711832d5e3c0efe0be9d`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 4.8 MB (4837177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4f7d9ca9e69cf94643d7c04aeeec199c0ac3e04d418a3e93cc08d47c74780`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76f2651885e7ca41e0f02191fa386cb990fb9e0d0d7c8ac3f88c1fef6d9fac`  
		Last Modified: Wed, 22 Sep 2021 18:21:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:a34ac0e31ba3a92b96600275cecf905613b5787a2abdb52e17c0376a6ce05ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7129168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d219fd32cfde7b620cd71920812305af0ec015ab9d4abc91a3310197786348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:49:41 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:49:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:49:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:49:47 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d2a30e1afb94108b4740597e03e612718f5459f533e4d9c4317ebb677ea7f`  
		Last Modified: Wed, 22 Sep 2021 18:51:56 GMT  
		Size: 4.5 MB (4500751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77ac3089b37eeef71ddc37c1b1e00b7e9c5e78d3fa2e06fde1c6da51397af0`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77690a748c6dd95f7fb19c68f9ff0d403ab5b71b6c9644baffb81f40e95e661c`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:972ab950f2b66e74d87d22da4b1839d39668d5edd9101b890132a231497292eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e52058719acb3fa32fb129feb81f0056b2a7736696b0694669b38a2978d60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 21:32:10 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 21:32:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 21:32:17 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 21:32:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f3df2cbc3c87820b00184dca6f1f0fc56066b82a951efe785873912615010`  
		Last Modified: Wed, 22 Sep 2021 21:34:28 GMT  
		Size: 4.5 MB (4494903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac9dabd3dd6b459696ed61905b261fc5d2119025e1a4f11e4f28ac3148b5eb`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3893e6935065d5383621afd73fa5b94df41b088b8a86c1d0bc95fb287a88ed2c`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b3d4a84a592a481ce06edda2e809e1eb0d816832b4675bc3dbd4839829108c77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7160174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce75dadb60225019e9a3fdd6343ba2eaedfe3632f8c39a5fb677701ea67ce1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 19:05:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 19:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 19:06:02 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 19:06:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f7295ad0852b3a6a04040d1e7caff544aa6b162e8ebf10cd1275d1fc84d7a`  
		Last Modified: Wed, 22 Sep 2021 19:07:11 GMT  
		Size: 4.4 MB (4447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0ad901f967d763a163de035129a0507cebce7b1f2e72a73f56361210914ce`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c5bd7249eaa792fd6e725e8170fa00df0cd00b28ec5cfee698c8643177a52`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:3d957fe6ccb80c520c21ca16adfa1afeb0739e8f3dd29b57c84af876a2989310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:7220113a349a14783135a4042e0e44a361faccd9128716d206a3b676b00fd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:7220113a349a14783135a4042e0e44a361faccd9128716d206a3b676b00fd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:3d957fe6ccb80c520c21ca16adfa1afeb0739e8f3dd29b57c84af876a2989310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:fdeb661f9c106521de9c0e4ee3957743c6a01bc53dad9a910000b17181c280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:6ddc52d3e875f9554d59a33b5d1104fb42532c547d4d8f5206d8c781bbb5a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692032377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79640873e27f02ba95f3fe49da175373a8a9ad553ad317e65a82f3f013c619d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:14:08 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:14:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:14:10 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:15:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:16:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:16:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07141c7bd13ff557354ae70dc72a7227ab19912c70d3c3cc4bec996a7655fd56`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77418125b04da08a7f44f805ad699df7585eee0222040b996e32ec745a6fb697`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e4e9c985c834ccbfff1ff7ad155154a05369a7f919fab1c5bbfddcc785707`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620819d7f2e3d530e1ec4c86284a111b32e0762c5d2c6e4143432838d163d5d`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 365.8 KB (365754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12675a3560b6328442167831b90f74ab44ede0be36abda31297d4e58d10cc5`  
		Last Modified: Wed, 22 Sep 2021 18:20:24 GMT  
		Size: 5.0 MB (4955548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c4436ed073542d01e386f4bc5f03d020ecd52dad574b31970789141c1de78`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb89b26f377943b12e1fee4cdb39bb72bd8df511dfae8a449036522f487945`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b9e214271ecaa071b0a98ecf97a0b2f5855eb783d34be9bdd2531fd2129e`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ca19ac6ce761f376a3c541e1df6f545e7d529741b14181e8f220f419c88ec3`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-windowsservercore` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:314877eef7766a391b52ecf69b974a4748aa31d2fb95fbcb0e1a5d8e42c69377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6281135566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a54daf861376ae8610d058e173573fb604a26caaf14af1c5499bbf441eaf`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:17:01 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:17:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:19:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:19:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:19:45 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:19:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:19:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88fe5c5a961345978d08184ec37560319c1f229ebbb4d863376aefcbad7b4b7`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2304c6367aed5770ee0a8bd54e7dea8f2a203e192b70eeed63cd3408617f5b`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d959edd2154d9d22f4a4c4012edcd1822a540ffb5b202b6558510034cd763b13`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7fe2b4f2c28b84cfc71adcd6641ee59d1f42e7ed6931b962ec99f025abbee`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 342.7 KB (342699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a306cebcc4ab9ab2ac8339cd5d2b9f688dd69ec9868ff507dd8f90cb3fdccca`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 9.5 MB (9451560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b41fa3135fdcb6be75fbbd16394a5b9a17c1f92002f24c09376761f8147244`  
		Last Modified: Wed, 22 Sep 2021 18:21:02 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91141728f944a1bd37f7c330b23c424cb2c8bde47c1448773a1e6bd5632ad6`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e4512cffc332936bddbe616ef049e8f641e12912cb81575bacb8189e483c7`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a87f3457dcdf6c46117821892a75a957ac670a3efc04a713b772bc37c6d150`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:1e2f1cb87735039a34afb74ec52511a20dbed7d38f0cd8d92a8c7ad413bbd4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:6ddc52d3e875f9554d59a33b5d1104fb42532c547d4d8f5206d8c781bbb5a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692032377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79640873e27f02ba95f3fe49da175373a8a9ad553ad317e65a82f3f013c619d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:14:08 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:14:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:14:10 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:15:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:16:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:16:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07141c7bd13ff557354ae70dc72a7227ab19912c70d3c3cc4bec996a7655fd56`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77418125b04da08a7f44f805ad699df7585eee0222040b996e32ec745a6fb697`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e4e9c985c834ccbfff1ff7ad155154a05369a7f919fab1c5bbfddcc785707`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620819d7f2e3d530e1ec4c86284a111b32e0762c5d2c6e4143432838d163d5d`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 365.8 KB (365754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12675a3560b6328442167831b90f74ab44ede0be36abda31297d4e58d10cc5`  
		Last Modified: Wed, 22 Sep 2021 18:20:24 GMT  
		Size: 5.0 MB (4955548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c4436ed073542d01e386f4bc5f03d020ecd52dad574b31970789141c1de78`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb89b26f377943b12e1fee4cdb39bb72bd8df511dfae8a449036522f487945`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b9e214271ecaa071b0a98ecf97a0b2f5855eb783d34be9bdd2531fd2129e`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ca19ac6ce761f376a3c541e1df6f545e7d529741b14181e8f220f419c88ec3`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:596e47f6ddc0d8a87611a5de627d10bcba30f83b51e4c67582e928e4b414fcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `nats:2-windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:314877eef7766a391b52ecf69b974a4748aa31d2fb95fbcb0e1a5d8e42c69377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6281135566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a54daf861376ae8610d058e173573fb604a26caaf14af1c5499bbf441eaf`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:17:01 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:17:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:19:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:19:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:19:45 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:19:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:19:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88fe5c5a961345978d08184ec37560319c1f229ebbb4d863376aefcbad7b4b7`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2304c6367aed5770ee0a8bd54e7dea8f2a203e192b70eeed63cd3408617f5b`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d959edd2154d9d22f4a4c4012edcd1822a540ffb5b202b6558510034cd763b13`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7fe2b4f2c28b84cfc71adcd6641ee59d1f42e7ed6931b962ec99f025abbee`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 342.7 KB (342699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a306cebcc4ab9ab2ac8339cd5d2b9f688dd69ec9868ff507dd8f90cb3fdccca`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 9.5 MB (9451560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b41fa3135fdcb6be75fbbd16394a5b9a17c1f92002f24c09376761f8147244`  
		Last Modified: Wed, 22 Sep 2021 18:21:02 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91141728f944a1bd37f7c330b23c424cb2c8bde47c1448773a1e6bd5632ad6`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e4512cffc332936bddbe616ef049e8f641e12912cb81575bacb8189e483c7`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a87f3457dcdf6c46117821892a75a957ac670a3efc04a713b772bc37c6d150`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6`

```console
$ docker pull nats@sha256:ac522b93125cafb92647e0c2154f3d84c626eae402ae181227f55073c8d02957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2183; amd64

### `nats:2.6` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine`

```console
$ docker pull nats@sha256:f9fb49bcb658924ee2b299455aa09a1574b0edd78a04e157ce90b6c300c67fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine` - linux; amd64

```console
$ docker pull nats@sha256:29e48bbbfabc68bd286161dd7b59b86ae9877601ba9a88578fcefa440f7f0434
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b274482e0b37c592f58b2c2b13db977af601c57886e25a1d2c502bd4d37e191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:20:16 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:20:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:20:19 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:20:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ed26ecc69fe2112cec367d3ba1751ac3f5ee981612711832d5e3c0efe0be9d`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 4.8 MB (4837177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4f7d9ca9e69cf94643d7c04aeeec199c0ac3e04d418a3e93cc08d47c74780`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76f2651885e7ca41e0f02191fa386cb990fb9e0d0d7c8ac3f88c1fef6d9fac`  
		Last Modified: Wed, 22 Sep 2021 18:21:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a34ac0e31ba3a92b96600275cecf905613b5787a2abdb52e17c0376a6ce05ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7129168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d219fd32cfde7b620cd71920812305af0ec015ab9d4abc91a3310197786348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:49:41 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:49:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:49:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:49:47 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d2a30e1afb94108b4740597e03e612718f5459f533e4d9c4317ebb677ea7f`  
		Last Modified: Wed, 22 Sep 2021 18:51:56 GMT  
		Size: 4.5 MB (4500751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77ac3089b37eeef71ddc37c1b1e00b7e9c5e78d3fa2e06fde1c6da51397af0`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77690a748c6dd95f7fb19c68f9ff0d403ab5b71b6c9644baffb81f40e95e661c`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:972ab950f2b66e74d87d22da4b1839d39668d5edd9101b890132a231497292eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e52058719acb3fa32fb129feb81f0056b2a7736696b0694669b38a2978d60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 21:32:10 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 21:32:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 21:32:17 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 21:32:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f3df2cbc3c87820b00184dca6f1f0fc56066b82a951efe785873912615010`  
		Last Modified: Wed, 22 Sep 2021 21:34:28 GMT  
		Size: 4.5 MB (4494903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac9dabd3dd6b459696ed61905b261fc5d2119025e1a4f11e4f28ac3148b5eb`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3893e6935065d5383621afd73fa5b94df41b088b8a86c1d0bc95fb287a88ed2c`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b3d4a84a592a481ce06edda2e809e1eb0d816832b4675bc3dbd4839829108c77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7160174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce75dadb60225019e9a3fdd6343ba2eaedfe3632f8c39a5fb677701ea67ce1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 19:05:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 19:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 19:06:02 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 19:06:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f7295ad0852b3a6a04040d1e7caff544aa6b162e8ebf10cd1275d1fc84d7a`  
		Last Modified: Wed, 22 Sep 2021 19:07:11 GMT  
		Size: 4.4 MB (4447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0ad901f967d763a163de035129a0507cebce7b1f2e72a73f56361210914ce`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c5bd7249eaa792fd6e725e8170fa00df0cd00b28ec5cfee698c8643177a52`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-alpine3.14`

```console
$ docker pull nats@sha256:f9fb49bcb658924ee2b299455aa09a1574b0edd78a04e157ce90b6c300c67fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:29e48bbbfabc68bd286161dd7b59b86ae9877601ba9a88578fcefa440f7f0434
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b274482e0b37c592f58b2c2b13db977af601c57886e25a1d2c502bd4d37e191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:20:16 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:20:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:20:19 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:20:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ed26ecc69fe2112cec367d3ba1751ac3f5ee981612711832d5e3c0efe0be9d`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 4.8 MB (4837177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4f7d9ca9e69cf94643d7c04aeeec199c0ac3e04d418a3e93cc08d47c74780`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76f2651885e7ca41e0f02191fa386cb990fb9e0d0d7c8ac3f88c1fef6d9fac`  
		Last Modified: Wed, 22 Sep 2021 18:21:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:a34ac0e31ba3a92b96600275cecf905613b5787a2abdb52e17c0376a6ce05ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7129168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d219fd32cfde7b620cd71920812305af0ec015ab9d4abc91a3310197786348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:49:41 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:49:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:49:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:49:47 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d2a30e1afb94108b4740597e03e612718f5459f533e4d9c4317ebb677ea7f`  
		Last Modified: Wed, 22 Sep 2021 18:51:56 GMT  
		Size: 4.5 MB (4500751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77ac3089b37eeef71ddc37c1b1e00b7e9c5e78d3fa2e06fde1c6da51397af0`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77690a748c6dd95f7fb19c68f9ff0d403ab5b71b6c9644baffb81f40e95e661c`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:972ab950f2b66e74d87d22da4b1839d39668d5edd9101b890132a231497292eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e52058719acb3fa32fb129feb81f0056b2a7736696b0694669b38a2978d60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 21:32:10 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 21:32:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 21:32:17 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 21:32:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f3df2cbc3c87820b00184dca6f1f0fc56066b82a951efe785873912615010`  
		Last Modified: Wed, 22 Sep 2021 21:34:28 GMT  
		Size: 4.5 MB (4494903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac9dabd3dd6b459696ed61905b261fc5d2119025e1a4f11e4f28ac3148b5eb`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3893e6935065d5383621afd73fa5b94df41b088b8a86c1d0bc95fb287a88ed2c`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b3d4a84a592a481ce06edda2e809e1eb0d816832b4675bc3dbd4839829108c77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7160174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce75dadb60225019e9a3fdd6343ba2eaedfe3632f8c39a5fb677701ea67ce1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 19:05:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 19:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 19:06:02 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 19:06:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f7295ad0852b3a6a04040d1e7caff544aa6b162e8ebf10cd1275d1fc84d7a`  
		Last Modified: Wed, 22 Sep 2021 19:07:11 GMT  
		Size: 4.4 MB (4447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0ad901f967d763a163de035129a0507cebce7b1f2e72a73f56361210914ce`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c5bd7249eaa792fd6e725e8170fa00df0cd00b28ec5cfee698c8643177a52`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-linux`

```console
$ docker pull nats@sha256:3d957fe6ccb80c520c21ca16adfa1afeb0739e8f3dd29b57c84af876a2989310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-linux` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver`

```console
$ docker pull nats@sha256:7220113a349a14783135a4042e0e44a361faccd9128716d206a3b676b00fd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:2.6-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-nanoserver-1809`

```console
$ docker pull nats@sha256:7220113a349a14783135a4042e0e44a361faccd9128716d206a3b676b00fd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:2.6-nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-scratch`

```console
$ docker pull nats@sha256:3d957fe6ccb80c520c21ca16adfa1afeb0739e8f3dd29b57c84af876a2989310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.6-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore`

```console
$ docker pull nats@sha256:fdeb661f9c106521de9c0e4ee3957743c6a01bc53dad9a910000b17181c280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `nats:2.6-windowsservercore` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:6ddc52d3e875f9554d59a33b5d1104fb42532c547d4d8f5206d8c781bbb5a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692032377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79640873e27f02ba95f3fe49da175373a8a9ad553ad317e65a82f3f013c619d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:14:08 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:14:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:14:10 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:15:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:16:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:16:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07141c7bd13ff557354ae70dc72a7227ab19912c70d3c3cc4bec996a7655fd56`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77418125b04da08a7f44f805ad699df7585eee0222040b996e32ec745a6fb697`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e4e9c985c834ccbfff1ff7ad155154a05369a7f919fab1c5bbfddcc785707`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620819d7f2e3d530e1ec4c86284a111b32e0762c5d2c6e4143432838d163d5d`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 365.8 KB (365754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12675a3560b6328442167831b90f74ab44ede0be36abda31297d4e58d10cc5`  
		Last Modified: Wed, 22 Sep 2021 18:20:24 GMT  
		Size: 5.0 MB (4955548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c4436ed073542d01e386f4bc5f03d020ecd52dad574b31970789141c1de78`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb89b26f377943b12e1fee4cdb39bb72bd8df511dfae8a449036522f487945`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b9e214271ecaa071b0a98ecf97a0b2f5855eb783d34be9bdd2531fd2129e`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ca19ac6ce761f376a3c541e1df6f545e7d529741b14181e8f220f419c88ec3`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.6-windowsservercore` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:314877eef7766a391b52ecf69b974a4748aa31d2fb95fbcb0e1a5d8e42c69377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6281135566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a54daf861376ae8610d058e173573fb604a26caaf14af1c5499bbf441eaf`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:17:01 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:17:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:19:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:19:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:19:45 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:19:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:19:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88fe5c5a961345978d08184ec37560319c1f229ebbb4d863376aefcbad7b4b7`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2304c6367aed5770ee0a8bd54e7dea8f2a203e192b70eeed63cd3408617f5b`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d959edd2154d9d22f4a4c4012edcd1822a540ffb5b202b6558510034cd763b13`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7fe2b4f2c28b84cfc71adcd6641ee59d1f42e7ed6931b962ec99f025abbee`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 342.7 KB (342699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a306cebcc4ab9ab2ac8339cd5d2b9f688dd69ec9868ff507dd8f90cb3fdccca`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 9.5 MB (9451560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b41fa3135fdcb6be75fbbd16394a5b9a17c1f92002f24c09376761f8147244`  
		Last Modified: Wed, 22 Sep 2021 18:21:02 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91141728f944a1bd37f7c330b23c424cb2c8bde47c1448773a1e6bd5632ad6`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e4512cffc332936bddbe616ef049e8f641e12912cb81575bacb8189e483c7`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a87f3457dcdf6c46117821892a75a957ac670a3efc04a713b772bc37c6d150`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-1809`

```console
$ docker pull nats@sha256:1e2f1cb87735039a34afb74ec52511a20dbed7d38f0cd8d92a8c7ad413bbd4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:2.6-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:6ddc52d3e875f9554d59a33b5d1104fb42532c547d4d8f5206d8c781bbb5a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692032377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79640873e27f02ba95f3fe49da175373a8a9ad553ad317e65a82f3f013c619d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:14:08 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:14:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:14:10 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:15:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:16:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:16:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07141c7bd13ff557354ae70dc72a7227ab19912c70d3c3cc4bec996a7655fd56`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77418125b04da08a7f44f805ad699df7585eee0222040b996e32ec745a6fb697`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e4e9c985c834ccbfff1ff7ad155154a05369a7f919fab1c5bbfddcc785707`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620819d7f2e3d530e1ec4c86284a111b32e0762c5d2c6e4143432838d163d5d`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 365.8 KB (365754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12675a3560b6328442167831b90f74ab44ede0be36abda31297d4e58d10cc5`  
		Last Modified: Wed, 22 Sep 2021 18:20:24 GMT  
		Size: 5.0 MB (4955548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c4436ed073542d01e386f4bc5f03d020ecd52dad574b31970789141c1de78`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb89b26f377943b12e1fee4cdb39bb72bd8df511dfae8a449036522f487945`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b9e214271ecaa071b0a98ecf97a0b2f5855eb783d34be9bdd2531fd2129e`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ca19ac6ce761f376a3c541e1df6f545e7d529741b14181e8f220f419c88ec3`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6-windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:596e47f6ddc0d8a87611a5de627d10bcba30f83b51e4c67582e928e4b414fcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `nats:2.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:314877eef7766a391b52ecf69b974a4748aa31d2fb95fbcb0e1a5d8e42c69377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6281135566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a54daf861376ae8610d058e173573fb604a26caaf14af1c5499bbf441eaf`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:17:01 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:17:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:19:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:19:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:19:45 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:19:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:19:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88fe5c5a961345978d08184ec37560319c1f229ebbb4d863376aefcbad7b4b7`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2304c6367aed5770ee0a8bd54e7dea8f2a203e192b70eeed63cd3408617f5b`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d959edd2154d9d22f4a4c4012edcd1822a540ffb5b202b6558510034cd763b13`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7fe2b4f2c28b84cfc71adcd6641ee59d1f42e7ed6931b962ec99f025abbee`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 342.7 KB (342699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a306cebcc4ab9ab2ac8339cd5d2b9f688dd69ec9868ff507dd8f90cb3fdccca`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 9.5 MB (9451560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b41fa3135fdcb6be75fbbd16394a5b9a17c1f92002f24c09376761f8147244`  
		Last Modified: Wed, 22 Sep 2021 18:21:02 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91141728f944a1bd37f7c330b23c424cb2c8bde47c1448773a1e6bd5632ad6`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e4512cffc332936bddbe616ef049e8f641e12912cb81575bacb8189e483c7`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a87f3457dcdf6c46117821892a75a957ac670a3efc04a713b772bc37c6d150`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.6.1`

**does not exist** (yet?)

## `nats:2.6.1-alpine`

**does not exist** (yet?)

## `nats:2.6.1-alpine3.14`

**does not exist** (yet?)

## `nats:2.6.1-linux`

**does not exist** (yet?)

## `nats:2.6.1-nanoserver`

**does not exist** (yet?)

## `nats:2.6.1-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.6.1-scratch`

**does not exist** (yet?)

## `nats:2.6.1-windowsservercore`

**does not exist** (yet?)

## `nats:2.6.1-windowsservercore-1809`

**does not exist** (yet?)

## `nats:2.6.1-windowsservercore-ltsc2016`

**does not exist** (yet?)

## `nats:alpine`

```console
$ docker pull nats@sha256:f9fb49bcb658924ee2b299455aa09a1574b0edd78a04e157ce90b6c300c67fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:29e48bbbfabc68bd286161dd7b59b86ae9877601ba9a88578fcefa440f7f0434
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b274482e0b37c592f58b2c2b13db977af601c57886e25a1d2c502bd4d37e191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:20:16 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:20:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:20:19 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:20:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ed26ecc69fe2112cec367d3ba1751ac3f5ee981612711832d5e3c0efe0be9d`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 4.8 MB (4837177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4f7d9ca9e69cf94643d7c04aeeec199c0ac3e04d418a3e93cc08d47c74780`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76f2651885e7ca41e0f02191fa386cb990fb9e0d0d7c8ac3f88c1fef6d9fac`  
		Last Modified: Wed, 22 Sep 2021 18:21:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:a34ac0e31ba3a92b96600275cecf905613b5787a2abdb52e17c0376a6ce05ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7129168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d219fd32cfde7b620cd71920812305af0ec015ab9d4abc91a3310197786348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:49:41 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:49:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:49:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:49:47 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d2a30e1afb94108b4740597e03e612718f5459f533e4d9c4317ebb677ea7f`  
		Last Modified: Wed, 22 Sep 2021 18:51:56 GMT  
		Size: 4.5 MB (4500751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77ac3089b37eeef71ddc37c1b1e00b7e9c5e78d3fa2e06fde1c6da51397af0`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77690a748c6dd95f7fb19c68f9ff0d403ab5b71b6c9644baffb81f40e95e661c`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:972ab950f2b66e74d87d22da4b1839d39668d5edd9101b890132a231497292eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e52058719acb3fa32fb129feb81f0056b2a7736696b0694669b38a2978d60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 21:32:10 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 21:32:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 21:32:17 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 21:32:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f3df2cbc3c87820b00184dca6f1f0fc56066b82a951efe785873912615010`  
		Last Modified: Wed, 22 Sep 2021 21:34:28 GMT  
		Size: 4.5 MB (4494903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac9dabd3dd6b459696ed61905b261fc5d2119025e1a4f11e4f28ac3148b5eb`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3893e6935065d5383621afd73fa5b94df41b088b8a86c1d0bc95fb287a88ed2c`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b3d4a84a592a481ce06edda2e809e1eb0d816832b4675bc3dbd4839829108c77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7160174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce75dadb60225019e9a3fdd6343ba2eaedfe3632f8c39a5fb677701ea67ce1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 19:05:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 19:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 19:06:02 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 19:06:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f7295ad0852b3a6a04040d1e7caff544aa6b162e8ebf10cd1275d1fc84d7a`  
		Last Modified: Wed, 22 Sep 2021 19:07:11 GMT  
		Size: 4.4 MB (4447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0ad901f967d763a163de035129a0507cebce7b1f2e72a73f56361210914ce`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c5bd7249eaa792fd6e725e8170fa00df0cd00b28ec5cfee698c8643177a52`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.14`

```console
$ docker pull nats@sha256:f9fb49bcb658924ee2b299455aa09a1574b0edd78a04e157ce90b6c300c67fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.14` - linux; amd64

```console
$ docker pull nats@sha256:29e48bbbfabc68bd286161dd7b59b86ae9877601ba9a88578fcefa440f7f0434
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7652594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b274482e0b37c592f58b2c2b13db977af601c57886e25a1d2c502bd4d37e191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:20:16 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:20:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:20:19 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:20:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ed26ecc69fe2112cec367d3ba1751ac3f5ee981612711832d5e3c0efe0be9d`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 4.8 MB (4837177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4f7d9ca9e69cf94643d7c04aeeec199c0ac3e04d418a3e93cc08d47c74780`  
		Last Modified: Wed, 22 Sep 2021 18:21:37 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76f2651885e7ca41e0f02191fa386cb990fb9e0d0d7c8ac3f88c1fef6d9fac`  
		Last Modified: Wed, 22 Sep 2021 18:21:36 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:a34ac0e31ba3a92b96600275cecf905613b5787a2abdb52e17c0376a6ce05ed5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7129168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d219fd32cfde7b620cd71920812305af0ec015ab9d4abc91a3310197786348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 18:49:41 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:49:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 18:49:46 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 18:49:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 18:49:47 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 18:49:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7d2a30e1afb94108b4740597e03e612718f5459f533e4d9c4317ebb677ea7f`  
		Last Modified: Wed, 22 Sep 2021 18:51:56 GMT  
		Size: 4.5 MB (4500751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77ac3089b37eeef71ddc37c1b1e00b7e9c5e78d3fa2e06fde1c6da51397af0`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77690a748c6dd95f7fb19c68f9ff0d403ab5b71b6c9644baffb81f40e95e661c`  
		Last Modified: Wed, 22 Sep 2021 18:51:53 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:972ab950f2b66e74d87d22da4b1839d39668d5edd9101b890132a231497292eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6926291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e52058719acb3fa32fb129feb81f0056b2a7736696b0694669b38a2978d60e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 21:32:10 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 21:32:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 21:32:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 21:32:17 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 21:32:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434f3df2cbc3c87820b00184dca6f1f0fc56066b82a951efe785873912615010`  
		Last Modified: Wed, 22 Sep 2021 21:34:28 GMT  
		Size: 4.5 MB (4494903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ac9dabd3dd6b459696ed61905b261fc5d2119025e1a4f11e4f28ac3148b5eb`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3893e6935065d5383621afd73fa5b94df41b088b8a86c1d0bc95fb287a88ed2c`  
		Last Modified: Wed, 22 Sep 2021 21:34:25 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b3d4a84a592a481ce06edda2e809e1eb0d816832b4675bc3dbd4839829108c77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7160174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce75dadb60225019e9a3fdd6343ba2eaedfe3632f8c39a5fb677701ea67ce1ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 22 Sep 2021 19:05:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 19:06:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='1518e0538b62b620c95b2b24da650b0997a911c244884135436d419f18ebee5a' ;; 		armhf) natsArch='arm6'; sha256='9800707e517cbfcc5aa4d00a0aea3026a504199160755896ae62564435acc539' ;; 		armv7) natsArch='arm7'; sha256='e61087a29c2a329f71d818e8e64efcc48e05ff79fedfba0e7e4a51f19ea39e08' ;; 		x86_64) natsArch='amd64'; sha256='61caa7c475fbb2fe5e741b1efa9b3e575f78982d4f74a3f3f75af9a2413bd88f' ;; 		x86) natsArch='386'; sha256='2e936537a8ea3fe634ad90791facd846bf52a1eed0af9d4559192560ac7829da' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 22 Sep 2021 19:06:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 22 Sep 2021 19:06:02 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Sep 2021 19:06:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8f7295ad0852b3a6a04040d1e7caff544aa6b162e8ebf10cd1275d1fc84d7a`  
		Last Modified: Wed, 22 Sep 2021 19:07:11 GMT  
		Size: 4.4 MB (4447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0ad901f967d763a163de035129a0507cebce7b1f2e72a73f56361210914ce`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c5bd7249eaa792fd6e725e8170fa00df0cd00b28ec5cfee698c8643177a52`  
		Last Modified: Wed, 22 Sep 2021 19:07:10 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:ac522b93125cafb92647e0c2154f3d84c626eae402ae181227f55073c8d02957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2183; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:3d957fe6ccb80c520c21ca16adfa1afeb0739e8f3dd29b57c84af876a2989310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:7220113a349a14783135a4042e0e44a361faccd9128716d206a3b676b00fd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:7220113a349a14783135a4042e0e44a361faccd9128716d206a3b676b00fd5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:e1cb2f4abfedd4b6ca379ac0ceded28e32a8282d87243a2a37f0ac16ee5aa768
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107321930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bc9d181f50ce6dc8d2679504117826f19eb81aa6c266189dd13dae0052e89`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 15:43:05 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:49 GMT
RUN cmd /S /C #(nop) COPY file:d8b36ddbb8e586e71ce6a43b9de9f91b50ffed57602042fcb7a25fa548d57fe5 in C:\nats-server.exe 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:52 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:66dbf96361e9ec1f64f66e255a947eab476edef46c3f9a3b4ede943fa8b87699`  
		Last Modified: Wed, 15 Sep 2021 15:46:11 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c0f0eda1a3fbf8b235391059da7dba48f172e2e89330fd3dec72c9c1549463`  
		Last Modified: Wed, 22 Sep 2021 18:20:46 GMT  
		Size: 4.6 MB (4611816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db73c034c889d68ba8dd841e9c6e0373c01a9c4a5581bb68dfe9bee46b708ab3`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdcf9ffd0d30f8610cc00606d12d2b23f9fbcaaba7efc8fb8927f7a08d06ffd`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aaa4b6d7993d4e053b3955e6f23e5738d53ac864fda3e017b1ec619edb323d`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3fa65a8f5c761117aa00c8105a1306f2bdd4ee253f48c25d1c5ff05bf57d63`  
		Last Modified: Wed, 22 Sep 2021 18:20:45 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:3d957fe6ccb80c520c21ca16adfa1afeb0739e8f3dd29b57c84af876a2989310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:720b32319601e71ad92cb37b596c67286d8356f0fc99bb3985efeb81de19bf75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebf49e0598cea644a2c8f54b146389171120b923107b7f80ee89e9930b93c6e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:dba1491f5fb1a7abb3a82b949b04b3859f0394414e9c3dd2e4546801ef43d235 in /nats-server 
# Wed, 22 Sep 2021 21:32:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 21:32:44 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 21:32:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 21:32:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:76297dd4956814327bf3af06c45650023637259efa5fc56f10378efaaaa77d9a`  
		Last Modified: Wed, 22 Sep 2021 21:35:05 GMT  
		Size: 4.2 MB (4211932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25474082518fff83a43a45000bb17e1b65c2f2daf22e437a170cc277fec57920`  
		Last Modified: Wed, 22 Sep 2021 21:35:02 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:fdeb661f9c106521de9c0e4ee3957743c6a01bc53dad9a910000b17181c280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:6ddc52d3e875f9554d59a33b5d1104fb42532c547d4d8f5206d8c781bbb5a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692032377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79640873e27f02ba95f3fe49da175373a8a9ad553ad317e65a82f3f013c619d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:14:08 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:14:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:14:10 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:15:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:16:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:16:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07141c7bd13ff557354ae70dc72a7227ab19912c70d3c3cc4bec996a7655fd56`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77418125b04da08a7f44f805ad699df7585eee0222040b996e32ec745a6fb697`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e4e9c985c834ccbfff1ff7ad155154a05369a7f919fab1c5bbfddcc785707`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620819d7f2e3d530e1ec4c86284a111b32e0762c5d2c6e4143432838d163d5d`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 365.8 KB (365754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12675a3560b6328442167831b90f74ab44ede0be36abda31297d4e58d10cc5`  
		Last Modified: Wed, 22 Sep 2021 18:20:24 GMT  
		Size: 5.0 MB (4955548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c4436ed073542d01e386f4bc5f03d020ecd52dad574b31970789141c1de78`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb89b26f377943b12e1fee4cdb39bb72bd8df511dfae8a449036522f487945`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b9e214271ecaa071b0a98ecf97a0b2f5855eb783d34be9bdd2531fd2129e`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ca19ac6ce761f376a3c541e1df6f545e7d529741b14181e8f220f419c88ec3`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:windowsservercore` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:314877eef7766a391b52ecf69b974a4748aa31d2fb95fbcb0e1a5d8e42c69377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6281135566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a54daf861376ae8610d058e173573fb604a26caaf14af1c5499bbf441eaf`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:17:01 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:17:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:19:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:19:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:19:45 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:19:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:19:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88fe5c5a961345978d08184ec37560319c1f229ebbb4d863376aefcbad7b4b7`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2304c6367aed5770ee0a8bd54e7dea8f2a203e192b70eeed63cd3408617f5b`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d959edd2154d9d22f4a4c4012edcd1822a540ffb5b202b6558510034cd763b13`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7fe2b4f2c28b84cfc71adcd6641ee59d1f42e7ed6931b962ec99f025abbee`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 342.7 KB (342699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a306cebcc4ab9ab2ac8339cd5d2b9f688dd69ec9868ff507dd8f90cb3fdccca`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 9.5 MB (9451560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b41fa3135fdcb6be75fbbd16394a5b9a17c1f92002f24c09376761f8147244`  
		Last Modified: Wed, 22 Sep 2021 18:21:02 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91141728f944a1bd37f7c330b23c424cb2c8bde47c1448773a1e6bd5632ad6`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e4512cffc332936bddbe616ef049e8f641e12912cb81575bacb8189e483c7`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a87f3457dcdf6c46117821892a75a957ac670a3efc04a713b772bc37c6d150`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:1e2f1cb87735039a34afb74ec52511a20dbed7d38f0cd8d92a8c7ad413bbd4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull nats@sha256:6ddc52d3e875f9554d59a33b5d1104fb42532c547d4d8f5206d8c781bbb5a6d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692032377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79640873e27f02ba95f3fe49da175373a8a9ad553ad317e65a82f3f013c619d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 13:14:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:40:54 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:14:08 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:14:09 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:14:10 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:15:06 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:16:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:16:37 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:16:38 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:16:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:16:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c4091e033b8590db7b89fded6d31ac2224162744daa4d7a7a66cbebd4b8c228`  
		Last Modified: Wed, 15 Sep 2021 15:04:44 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c75402e6fab70f623ca8becfa5bb563e5630bbb4dac8adb11e385d75e171aed`  
		Last Modified: Wed, 15 Sep 2021 15:45:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07141c7bd13ff557354ae70dc72a7227ab19912c70d3c3cc4bec996a7655fd56`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77418125b04da08a7f44f805ad699df7585eee0222040b996e32ec745a6fb697`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e4e9c985c834ccbfff1ff7ad155154a05369a7f919fab1c5bbfddcc785707`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3620819d7f2e3d530e1ec4c86284a111b32e0762c5d2c6e4143432838d163d5d`  
		Last Modified: Wed, 22 Sep 2021 18:20:25 GMT  
		Size: 365.8 KB (365754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12675a3560b6328442167831b90f74ab44ede0be36abda31297d4e58d10cc5`  
		Last Modified: Wed, 22 Sep 2021 18:20:24 GMT  
		Size: 5.0 MB (4955548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c4436ed073542d01e386f4bc5f03d020ecd52dad574b31970789141c1de78`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccb89b26f377943b12e1fee4cdb39bb72bd8df511dfae8a449036522f487945`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053b9e214271ecaa071b0a98ecf97a0b2f5855eb783d34be9bdd2531fd2129e`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ca19ac6ce761f376a3c541e1df6f545e7d529741b14181e8f220f419c88ec3`  
		Last Modified: Wed, 22 Sep 2021 18:20:23 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2016`

```console
$ docker pull nats@sha256:596e47f6ddc0d8a87611a5de627d10bcba30f83b51e4c67582e928e4b414fcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `nats:windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull nats@sha256:314877eef7766a391b52ecf69b974a4748aa31d2fb95fbcb0e1a5d8e42c69377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6281135566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed46a54daf861376ae8610d058e173573fb604a26caaf14af1c5499bbf441eaf`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 13:26:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Sep 2021 15:43:15 GMT
ENV NATS_DOCKERIZED=1
# Wed, 22 Sep 2021 18:16:59 GMT
ENV NATS_SERVER=2.6.0
# Wed, 22 Sep 2021 18:17:00 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.6.0/nats-server-v2.6.0-windows-amd64.zip
# Wed, 22 Sep 2021 18:17:01 GMT
ENV NATS_SERVER_SHASUM=deba2c9db4dbbd820bc351efdb6cbe36a52e88dae6fe504e71fb1003012b733d
# Wed, 22 Sep 2021 18:17:55 GMT
RUN Set-PSDebug -Trace 2
# Wed, 22 Sep 2021 18:19:42 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 22 Sep 2021 18:19:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Wed, 22 Sep 2021 18:19:45 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:19:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 22 Sep 2021 18:19:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5796468f91731000e9a76e836156826a1cd4ed963bcd80e6558c538a12c2132d`  
		Last Modified: Wed, 15 Sep 2021 15:05:15 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611fe9c559abed986280087eef7d362a6ecb9ad281b1427395fdfc2d99d3d9c4`  
		Last Modified: Wed, 15 Sep 2021 15:46:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88fe5c5a961345978d08184ec37560319c1f229ebbb4d863376aefcbad7b4b7`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2304c6367aed5770ee0a8bd54e7dea8f2a203e192b70eeed63cd3408617f5b`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d959edd2154d9d22f4a4c4012edcd1822a540ffb5b202b6558510034cd763b13`  
		Last Modified: Wed, 22 Sep 2021 18:21:03 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7fe2b4f2c28b84cfc71adcd6641ee59d1f42e7ed6931b962ec99f025abbee`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 342.7 KB (342699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a306cebcc4ab9ab2ac8339cd5d2b9f688dd69ec9868ff507dd8f90cb3fdccca`  
		Last Modified: Wed, 22 Sep 2021 18:21:04 GMT  
		Size: 9.5 MB (9451560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b41fa3135fdcb6be75fbbd16394a5b9a17c1f92002f24c09376761f8147244`  
		Last Modified: Wed, 22 Sep 2021 18:21:02 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a91141728f944a1bd37f7c330b23c424cb2c8bde47c1448773a1e6bd5632ad6`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e4512cffc332936bddbe616ef049e8f641e12912cb81575bacb8189e483c7`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a87f3457dcdf6c46117821892a75a957ac670a3efc04a713b772bc37c6d150`  
		Last Modified: Wed, 22 Sep 2021 18:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
