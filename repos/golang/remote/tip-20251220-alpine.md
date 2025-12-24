## `golang:tip-20251220-alpine`

```console
$ docker pull golang@sha256:832369c8675a3c07396496375fa44d9bd06a35a449d3bfff7ef252cd223707a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20251220-alpine` - linux; amd64

```console
$ docker pull golang@sha256:8e373c50514cdfcdbd150d0ec5309ca20502c0008a2219780cabbd7870034377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99194010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04931c9b2b597016b9fca2f8ff0a9fc8e81b7e2db7639e94880cb3a09ca33513`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:19:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:20:55 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:20:55 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:20:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:55 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:20:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0afca8d2515f214b0f47364574701d449ffdb6dbd4f48e14ec3c070ff48fb94`  
		Last Modified: Wed, 24 Dec 2025 05:21:20 GMT  
		Size: 296.1 KB (296088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8ab74e427643c28187f0d3b567e6fea07c0d44d52df85de53b9ccdd7a063e`  
		Last Modified: Wed, 24 Dec 2025 05:21:26 GMT  
		Size: 95.0 MB (95037660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd9a5194362062b7cad8a567f4d55c178c59bab9b568996fccbdc31940c5a9e`  
		Last Modified: Wed, 24 Dec 2025 05:21:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:bf4c7d5e4455c9642a054589d0bedf6cee6dc7ff75ab9efe3f9af27ea01ca109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd59d6f4fcd01777de3ce664b463656a7a03e4d72f0ea29e0b31b0536667c485`

```dockerfile
```

-	Layers:
	-	`sha256:a1a69cd2abe189ea3db8962df66def6283b6e8cf6b02928836afc32ff8d22870`  
		Last Modified: Wed, 24 Dec 2025 06:24:14 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543c2582b0f2be00fba43e697639ae166db5a24a614795e21bcfcaebf4f8d336`  
		Last Modified: Wed, 24 Dec 2025 06:24:20 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251220-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:6d3782c447195cea7e5f53abfadf2eb65ceed40feb25393fb9373a9b19911a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95249378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9ddc00686828a2bd72116d60acfa01435e7930d7d05cb9da3d6ed8fdd47446`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:14:17 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:16:58 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:58 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:58 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6e1b6efc80095b479aeecd0579d79dbb5563c934617abdbaead285aad15d1c`  
		Last Modified: Wed, 24 Dec 2025 05:17:21 GMT  
		Size: 297.3 KB (297272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccd0041f8e1b8b3e27b5b75c781b1c5ce120805fd1042666bffd35913573ec1`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 91.4 MB (91383515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672ac98f794a1c26034b8a842ecfab567fd5c8a78b53a928868cb41416d4cf8b`  
		Last Modified: Wed, 24 Dec 2025 05:17:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:11b59dd83e9e80e5b4afc428daaf87d01e865755c944c6ab99376a2d33104a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a17f6bbc61e5c99561cc5f116231f9aa04f2d307c3cb1977a02f51490adac3`

```dockerfile
```

-	Layers:
	-	`sha256:6e4b5d8fd8ab6409b22d4d321afeaefe62199ff10cd4b31f4e1c67c9a0e49142`  
		Last Modified: Wed, 24 Dec 2025 06:24:24 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251220-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:80dba789992e60312a5ab793ce5b552ec42d05ae67168230bce8380436563213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94681579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae615ced8f28c839c914b0d607bd8231c9108e06556dbda5c9647a2cccadb99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:14:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:17:24 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:17:24 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:17:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:17:24 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0f1a7caa9c8f343c1227c838c365e253f6cda6e0a2f8a81643219e8161a9a8`  
		Last Modified: Wed, 24 Dec 2025 05:17:50 GMT  
		Size: 296.2 KB (296206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916e480570823a95137488489c184e78cf3bafa0a643be0c57f52f82930a006`  
		Last Modified: Wed, 24 Dec 2025 05:18:05 GMT  
		Size: 91.1 MB (91105827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a1364e49f487327810042bca28f745c4be447b7f30a59d9a92db207b9e18b9`  
		Last Modified: Wed, 24 Dec 2025 05:17:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f441db82338beccdb9e169be5738d3290f5a0f107491273642cad4d0255a586a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0940a9ddf3c5dcdd169840614f972162ae3266d6bdd9ee234e7917e8ada23eb`

```dockerfile
```

-	Layers:
	-	`sha256:4f8f90e8d2c593a86e656668e9d591d7674e2ef7613cbac642c1a67d0f84373d`  
		Last Modified: Wed, 24 Dec 2025 06:24:27 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212ba3e6381532bcd06f7b5bc91b0466c4c36e776f2d8113e121ffe5192f881b`  
		Last Modified: Wed, 24 Dec 2025 06:24:27 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251220-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:816bbf9a8218fbad9a1f9849230aec3ec35d7e469641141447e0d0de7dc1f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94608228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e141f1f472af4f623538e60a28c8bddc506bf83224984b988860db594a7c15`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:21:39 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:21:39 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:21:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:39 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:21:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:21:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e0a294027384c78dfff51211050f3460623e5cf2dfd441f1c120a533c3860f`  
		Last Modified: Wed, 24 Dec 2025 05:22:05 GMT  
		Size: 298.8 KB (298844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1a52724d12595cbdd937d1a6f8220032f161596f409cbf2928a4904bc545b`  
		Last Modified: Wed, 24 Dec 2025 05:22:14 GMT  
		Size: 90.1 MB (90113486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335b42b77bc67fe256c448a0770888a57b318965f643af51acfc902291205173`  
		Last Modified: Wed, 24 Dec 2025 05:22:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3e4b1a54f84277eb7c1f24a42ba1aef3da1b5368352465a6bff2daf6ce818935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdfe657a128ea49af9cb34e3b2e146cd90782d18757caa49df837d1e7c8bc31`

```dockerfile
```

-	Layers:
	-	`sha256:c288748b681847e4233c25a5f52e62c153d92f104300ed3b970d37b392a8ecc0`  
		Last Modified: Wed, 24 Dec 2025 06:24:31 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38584e498fa7037b04e17e7ac94d7dcf6d91c78f4dc41c7aae1205a5b207dbc4`  
		Last Modified: Wed, 24 Dec 2025 06:24:31 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251220-alpine` - linux; 386

```console
$ docker pull golang@sha256:12d811a171bbe792e0a3b9a23ab7f8651b5f9c7bb59a6e14324df93829c6f2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96906429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c842422de5d12cb4d46fae6b99ef2c9d68da47a41828e5ad7ceec2657bac9839`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:14:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:16:49 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:49 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:49 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:16:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:16:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c701b594784afd48d9ddc31a895451773b6725fab568db5199f03f881283d`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 296.7 KB (296669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fa6b6fe890c82489ba635114b540868912dc247cb535fd5b44aa5a94fb494`  
		Last Modified: Wed, 24 Dec 2025 05:17:06 GMT  
		Size: 92.9 MB (92923502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0a2f7f894b4418803957662205d1524658e0a48d2f1a6d6b39505ecdec1aab`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a8798d90c287abbb69030152a751a4cfc5744f85dbf7ad84c384f207e834bc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82dba4c25a424d6dfbfd8b77c8fad357e0731b5c0276539e4acdae8dbd1920e`

```dockerfile
```

-	Layers:
	-	`sha256:49ddd48765e15439d5bcdc52b3f07ee9f2715c1233c71defabca33a50b06fac8`  
		Last Modified: Wed, 24 Dec 2025 06:24:34 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c961d0389f2554eb245987100f5aa3ab9b4b3d1c4a02d854e338421f8caa2698`  
		Last Modified: Wed, 24 Dec 2025 06:24:35 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251220-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:489c6032eaf2177026f7118833530cd5fd9ce4676ac807e469b0f9130b9e33c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95782421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091ed8f3a86b96198f702a3b8216d4f8970cc64c2cb3a3f6c822f587bb0df38a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:34:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:34:00 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:42:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:42:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251744709998ea3415429d77aa83c1ba367b71bf12c4b11c84d3ff1d0c4b550`  
		Last Modified: Thu, 18 Dec 2025 01:37:40 GMT  
		Size: 299.3 KB (299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5de3a0302474d051f06a0dba49ec72e6a84fba75a10ec5c8dcfe3ca9da396d`  
		Last Modified: Wed, 24 Dec 2025 05:35:28 GMT  
		Size: 91.7 MB (91655252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f262625bddca985dec53a1982cdc62721b56fca78b48261a93a11cf7f7f8fb`  
		Last Modified: Wed, 24 Dec 2025 05:42:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e3f3c2f506f1af52e2b485dbc8b2d76e73e7d38943b003681a8020203d3c80ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a04fb7151c9be2684f4b06469fa2ad1b7d67ecac44a9df8e990db14f00484a`

```dockerfile
```

-	Layers:
	-	`sha256:74b669e3b894207f6ead529f8adeec3b5e09b830e607c55367314020bb04310d`  
		Last Modified: Wed, 24 Dec 2025 06:24:38 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00040fccff97d7665f7555dd8290d6cd15f11f0c42c4aab5dde6f79c3913a111`  
		Last Modified: Wed, 24 Dec 2025 06:24:39 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251220-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:d0b39dadd13e5adc16ce7ec7bdb5e15d9eed4ea244426427a36c80ba0e25ff7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96179253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3469fa9ec19052277ee531ae7d03fc7553332f4dcae39559f7199821dc1c995d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 06:56:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:56:42 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 07:40:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 07:40:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c358a50d2f39217ca62c3bf8831f5ece762bf2d424204f727fa6a6f9f5124f1`  
		Last Modified: Fri, 19 Dec 2025 05:50:24 GMT  
		Size: 296.5 KB (296519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efbeb47d67a4f0f513126184055d20de04c0261cfdbd8b06feaf3a27c3f0eb2`  
		Last Modified: Wed, 24 Dec 2025 07:04:00 GMT  
		Size: 92.3 MB (92298638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fef3ec5be52f1b1bff538da613c604f473030bff0b4fab2f5696c2f7d9102e`  
		Last Modified: Wed, 24 Dec 2025 07:42:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e88d4b61f4e91166d258128c9f1c75e9d7056be6c9247cae79c7f81cdd14f8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c0999ad3a793d4f0e0bd022102f2dbe1c2f249b633d4e8cbf3a359fb4d674d`

```dockerfile
```

-	Layers:
	-	`sha256:ac69014b03b099cf0e94925a6344a265c847b7e9c111c3edc3306dc5bf558e45`  
		Last Modified: Wed, 24 Dec 2025 09:23:53 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b264af81db5fccd0f3321c6d7a3e79411636b506d49a27821705361dd3ca650a`  
		Last Modified: Wed, 24 Dec 2025 09:23:54 GMT  
		Size: 25.2 KB (25151 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251220-alpine` - linux; s390x

```console
$ docker pull golang@sha256:dacfd4500ae1b5fddb81100290ea8e75bbe4cff7741cebff80514bb8c95886fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98220498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3463cb51ff8f568b4dd22b5e77a46e93e6177cec96aaa14e607b4357175e570`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:14:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:16:36 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:36 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:36 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:16:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:16:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7224d7d29671ca737c9ec945a7373478caed2bbfb74b122f8685b8c92149198`  
		Last Modified: Thu, 18 Dec 2025 01:15:01 GMT  
		Size: 297.2 KB (297192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eae26383a5ec3ad19d41ec233e74f5aea1ebfab7013779b5b7f518483b785a`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 94.2 MB (94198838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00369d20ce555056ad87224cbdb42597e250728553b8fba37387aac11b81531a`  
		Last Modified: Wed, 24 Dec 2025 05:17:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251220-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dc723c366891bfe9cae310416c031c7df0cb33c612ac615f410b77c597253627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cfc2b93b7cfe62c5184c7be1ebdf8912836608f04e2abe68d4d80dc34db5ec`

```dockerfile
```

-	Layers:
	-	`sha256:b4e42e54545f8ae7b3ab887918659cd6ca48a548a55056fde349e2ec8ecc6914`  
		Last Modified: Wed, 24 Dec 2025 06:24:42 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1764227abd8122ee4c3666255bcdddba4774c95cd87819cd86c047936e6e9e`  
		Last Modified: Wed, 24 Dec 2025 06:24:43 GMT  
		Size: 24.9 KB (24921 bytes)  
		MIME: application/vnd.in-toto+json
