## `nats:alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json
