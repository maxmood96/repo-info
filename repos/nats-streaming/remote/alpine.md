## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:bf3b12972df0718ccda9b7c8b7e7097b91225443fbe489aeb37deef6cf1437c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ce864616072144f7346b9b972536450e6383b279369e87cb8cf2c51d6b708d41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10251348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bc35ecea3c9509ad47eea096fbbcb2682e5c01a8bf43018c9ba8c7b6385886`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:49:46 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 19 Jul 2022 23:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 19 Jul 2022 23:49:48 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 19 Jul 2022 23:49:48 GMT
EXPOSE 4222 8222
# Tue, 19 Jul 2022 23:49:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 23:49:49 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4cce35c8d4c0bea6d81baded8c907b3c6220bbba48a90d2c5b36d205ebd3802`  
		Last Modified: Tue, 19 Jul 2022 23:50:17 GMT  
		Size: 7.4 MB (7436284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c119cae69fe72beb67163ef130566d86f25d4ef9d88a72e25491c1fbef9aeb1c`  
		Last Modified: Tue, 19 Jul 2022 23:50:16 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:368fa2e3833b201afe0b714f352912e356d75a663b9f1c5be95a9ad4755cf5a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8043abb9e9dfe7b0a21e62a4189408480ccce003157b18d18b5673d492d0e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 19 Jul 2022 22:49:49 GMT
ADD file:4958b5356608921fe85d83047b74d1cb4a53de78c3465039ac4e60a68329da64 in / 
# Tue, 19 Jul 2022 22:49:50 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:42:30 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 20 Jul 2022 00:42:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 20 Jul 2022 00:42:35 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 20 Jul 2022 00:42:35 GMT
EXPOSE 4222 8222
# Wed, 20 Jul 2022 00:42:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:42:36 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fcc62ebebb3542c1aad49c3cc072a98cf619f67e914baba1ea7dfeadcb32cbdd`  
		Last Modified: Tue, 19 Jul 2022 22:51:27 GMT  
		Size: 2.6 MB (2622400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc7d94c6b026795a893e476febf1c2bb497685578b70fd215f4ad9311864b77`  
		Last Modified: Wed, 20 Jul 2022 00:44:16 GMT  
		Size: 6.9 MB (6944759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfbd55097111480112a2de08fe6f673c03bfd4f0a307cfe1abdb4f68897d881`  
		Last Modified: Wed, 20 Jul 2022 00:44:11 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b12cb36dcce5f20faa3742bf9bd14c2559760051aa2be370d4f1b96e91eaf17c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9359152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9b0429032556b1ad034641bf82dfc710affbaa234ffc89097df2216359510a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 19 Jul 2022 22:57:50 GMT
ADD file:eb9518889a2987adfe1dfbeb786888817d6b767409b0102155094508f88b8798 in / 
# Tue, 19 Jul 2022 22:57:51 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:44:19 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 20 Jul 2022 00:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 20 Jul 2022 00:44:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 20 Jul 2022 00:44:25 GMT
EXPOSE 4222 8222
# Wed, 20 Jul 2022 00:44:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 00:44:25 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:4a43ec7a7388a66102a4ef9408174101a21dd2260a6deb956929f7eda8cde610`  
		Last Modified: Tue, 19 Jul 2022 22:59:36 GMT  
		Size: 2.4 MB (2424551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801b595ed50b7b23fde0e03d8f32416359158ad94094a355cc52d6b3374616d0`  
		Last Modified: Wed, 20 Jul 2022 00:46:10 GMT  
		Size: 6.9 MB (6934182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9d608658c81b9f79d859b11b4612873c2339cf14107f8dd8a11eb1ffdd353a`  
		Last Modified: Wed, 20 Jul 2022 00:46:05 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:9e609fc11fdbcc413fc8fc33648a25f227b70c8200c3edea3358ff7677b7018a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3281b1f52f27da891a3dd932cdc6b9045c3d13541da112c9d473424553a1c3e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 04:11:44 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 20 Jul 2022 04:11:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 20 Jul 2022 04:11:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 20 Jul 2022 04:11:49 GMT
EXPOSE 4222 8222
# Wed, 20 Jul 2022 04:11:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 04:11:51 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42abf80e72c84bc6b2a2d668547d24df9de3986b8bb5cd3ef1fd429618ae3085`  
		Last Modified: Wed, 20 Jul 2022 04:12:39 GMT  
		Size: 6.9 MB (6854299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3541fa4495998bfff1611458688dedd40af42213bd9b7ef374f7fbe0fa249b4`  
		Last Modified: Wed, 20 Jul 2022 04:12:38 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
