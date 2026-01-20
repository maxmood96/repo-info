## `golang:tip-alpine`

```console
$ docker pull golang@sha256:267af086bbacb4010da24804802c33cbd77547d5282bd9df5fce585e927b0edc
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:3fb5fe38018de909a0c9d443acda18c9cf90b1334245a72d484d97e21ed61e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99212748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74284769af55b4f7a3a6ba23e781f7b8343b15704ae032b1b494ccc51989af64`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:49:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:51:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:51:45 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:51:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:51:45 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:51:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:51:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a41ba6a7dd2c212823125801c4a4cd74be1c7df3c392945b369c8c0915af6b`  
		Last Modified: Tue, 20 Jan 2026 18:52:02 GMT  
		Size: 296.1 KB (296090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6a5b8343289eb0c3c52bf550e1fe8d1945ce754f136a34955c716ac7e17d7`  
		Last Modified: Tue, 20 Jan 2026 18:52:17 GMT  
		Size: 95.1 MB (95056396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513f52a799226dc1921be10767983cc9438fe47ecc61c4aa25b5c7302fc8f43b`  
		Last Modified: Tue, 20 Jan 2026 18:52:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:03de7a0e9a4dbe1b0f300550661a56dbae1bbecfeacf3753ec197354d4cc2495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298bbd1b3740fb67aa262d7b6330b5ebc26912f6dfdd8dc51697c912efbb91cb`

```dockerfile
```

-	Layers:
	-	`sha256:2d0087e436f7409051a9eb3bf8f4fbc898a9887024d57f92c434ffa47164daff`  
		Last Modified: Tue, 20 Jan 2026 21:24:14 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9001a47137bc9dd1d757eeacbc757a58d46d3087fd3b37082ffbef1537bfac4`  
		Last Modified: Tue, 20 Jan 2026 21:24:16 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:8d71ff45fd5e3a295b84c023deb030290ae17339b076533c8fa6aa561f48165b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95271583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d748cee16af19be2c468bb124ac0066f5fa6cc322a4e5eba941ce3e17942b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:50:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:52:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:57 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:57 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e3dd48ffa051eb40828f4e3774aeda245966b2d3c6136928a63b51458950a`  
		Last Modified: Tue, 20 Jan 2026 18:53:11 GMT  
		Size: 297.3 KB (297270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed3bda5a5c34f85b217d1a214cc216a3a9141352cc733d31928c895ddc9b66d`  
		Last Modified: Tue, 20 Jan 2026 18:53:14 GMT  
		Size: 91.4 MB (91405722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aacdf2917d2dd79ef75a59efbb434fa613e4f93d01761414c0f10c0b714cd12`  
		Last Modified: Tue, 20 Jan 2026 18:53:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f33bd06e0bf249bd316ef8849faafddcb84789f1cf8c61d9b0030d31465d1ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c53b9a66f3d94f00ba8842646871705b4b46c46086d78a8de7d2785bbc2c9f`

```dockerfile
```

-	Layers:
	-	`sha256:9c5b45ae1cb8705ca3c297963a999c55338270a767b1348abac8b8d949730d3a`  
		Last Modified: Tue, 20 Jan 2026 21:24:19 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:23667535757dd877fd7d7ab56ca21740dcb3e6127afcb2c25354b5a0e1f14de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94703533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a62fc0a4119e0a6fd53ecf754856800f00900bf1dcce22ae5c69e44851892f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:50:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:53:20 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:53:20 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:53:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:53:20 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94238ad6f0e28a9ba3ab1ad2425fc43e09520cbc12da8560ababba0a880e292`  
		Last Modified: Tue, 20 Jan 2026 18:53:44 GMT  
		Size: 296.2 KB (296200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbc1ebe88b1983952e0d3b08c79038602b5105dcae7c600fd0a26d7e35cad0`  
		Last Modified: Tue, 20 Jan 2026 18:53:36 GMT  
		Size: 91.1 MB (91127787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6454f1c637e6d24a3609765d5bf12fb6d1d88e7041f773bfe613b25dc8a5a25d`  
		Last Modified: Tue, 20 Jan 2026 18:53:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a7752e8f21583e4fd1e34a2138e702bedb356f77e0bc435e597fe0745e5e4ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d029d4fd4e00f920372212ea7dae3601f33e0a7498fdc016d519878d7c62833`

```dockerfile
```

-	Layers:
	-	`sha256:8c147a67c0f260a96b420d60a9cb8bb5fb69b5eb967a61f03fb9959a8ab75a7e`  
		Last Modified: Tue, 20 Jan 2026 21:24:21 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97bb403db1167110019ee585e8e00756f4365cbfeb5aafd3a084074a1914bca`  
		Last Modified: Tue, 20 Jan 2026 21:24:23 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3e5237f4ce56a8e1612a14448d7ae0a188595c275da633e95548480c1099934c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94626702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9137f2d7daf97123801faba81d9b7ae4a5b09c706d8246a4750703ddd36ce9f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:49:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:51:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:51:40 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:51:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:51:40 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:51:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:51:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eaf26a402eab5328073bd50df17cec079083915b456a9039e3516a5dff2b58`  
		Last Modified: Tue, 20 Jan 2026 18:52:05 GMT  
		Size: 298.8 KB (298847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8704a9b461e9f9c3cf81dacaf53a5375b1bb82e9194e9ce88802dc458b5979`  
		Last Modified: Tue, 20 Jan 2026 18:52:00 GMT  
		Size: 90.1 MB (90131959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a40d56dc39b0d559503ecf7321809858fb903ccf133787ade8d04d86e80469e`  
		Last Modified: Tue, 20 Jan 2026 18:52:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d6f01b7ba29ebf374f8a069be9614fcdbefeafec7a12184ee0ba6178ef7551e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171b1d399fd8161ad82f500ab4212a31ad25e0abcaf5ebad19b4550fdb2b5ebf`

```dockerfile
```

-	Layers:
	-	`sha256:40120c9b2faf5a804ddc4763d2c7835824e0c6b49c333a2d1db8a1efd02ed4a6`  
		Last Modified: Tue, 20 Jan 2026 21:24:25 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ce8883e6ce68a9c80ada8e823c02f70b15a1790529af252002978b564a51686`  
		Last Modified: Tue, 20 Jan 2026 18:51:57 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:82364f37e5b17b1bf2bc3430531a018d1b5c656b10fad1588e05501515e19177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96930976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0722cb954d2d6769b2922a8f3a1beeb091d498013cb0b5f2fd6e414148a9c955`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Tue, 20 Jan 2026 18:52:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:52:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:52:10 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:52:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:52:10 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:54:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:54:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eb81f868cc2b25cc90fd19a6b814d4bd2bdbb61593b7cd8386e288187d74d4`  
		Last Modified: Tue, 20 Jan 2026 18:55:00 GMT  
		Size: 296.7 KB (296676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2898920cb13c505259be6cf40bfc2b763657f2a33b173994b269e661d72ebfad`  
		Last Modified: Tue, 20 Jan 2026 18:52:39 GMT  
		Size: 92.9 MB (92948041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0050b4f4814ad88fbc6c8458612a15f3e2b9d508c9db9500fcef471438d254ca`  
		Last Modified: Tue, 20 Jan 2026 18:55:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6d016d7cc5f384f61614d7b8f0e17d101e1e564c3596bfff24776a929701c70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85fb99b332b540a94036f1ee495baf4db3715a7ba87e643e0d77ba64ce87adb`

```dockerfile
```

-	Layers:
	-	`sha256:c577104cd337424870714fba99be6e0da31477c242f1caf2bd7ef21f375bf58d`  
		Last Modified: Tue, 20 Jan 2026 21:24:29 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28d70d5ed87e05548ac3f5b81c3982b9b2fc737a3d7c82d78cf563f63c897b92`  
		Last Modified: Tue, 20 Jan 2026 21:24:30 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:1eec7467dfb77edd098a7742c3154dc2df2cd8a005d3fc1b2c3facbd89527cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95809027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfa463b486172394281809ae9ac1c9faac7f353d3e627e065a66cb312ba0d18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:54:57 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:54:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:54:57 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 19:02:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 19:02:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251744709998ea3415429d77aa83c1ba367b71bf12c4b11c84d3ff1d0c4b550`  
		Last Modified: Thu, 18 Dec 2025 01:37:40 GMT  
		Size: 299.3 KB (299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daa35feb63e7ef5c9399e73cf4420af92b3279e1deb9e79d9f88735b792386c`  
		Last Modified: Tue, 20 Jan 2026 18:57:28 GMT  
		Size: 91.7 MB (91681857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa22a461b8299a8efea4fb8feb4163d12abe53de426ee55f2ce166fa6046ee`  
		Last Modified: Tue, 20 Jan 2026 19:02:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9133d7e9e2e0820117e99ace8075594fa45abe504b0d8e923eed7c26e8e6d1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (219980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02c79b117524f67adfe735599cf611c6832dd61626e97638d90021363711f77`

```dockerfile
```

-	Layers:
	-	`sha256:19931097886e9ef1876708ff3f6afbf35832e755d4f3bc86f2f8bed272646daf`  
		Last Modified: Tue, 20 Jan 2026 19:02:33 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be4c8146c71bf68c63b8eae0f7fbe1751f37e431ae4fa30f416fba7a918c96c`  
		Last Modified: Tue, 20 Jan 2026 19:02:33 GMT  
		Size: 25.0 KB (24980 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:1112467c6f8dc6c131eaaaf3c10dd61aa4efea6d864503705a777f9d388cf2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96196492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cb3ea042884f7dc2d6ff19c36b19aee9a4210dff0e30b74856dd651809dbbf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 Jan 2026 21:38:33 GMT
ENV GOPATH=/go
# Mon, 19 Jan 2026 21:38:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Jan 2026 21:38:33 GMT
COPY /target/ / # buildkit
# Mon, 19 Jan 2026 21:38:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 Jan 2026 21:38:50 GMT
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
	-	`sha256:22a3cc83856871e3a177f0a6b27128217f73d5993c49818bd1374bd92a6bcb48`  
		Last Modified: Wed, 14 Jan 2026 03:12:04 GMT  
		Size: 92.3 MB (92315877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7242b94826dd420ff8c2d4627119cbfee3a19b68631deed9e43378fdc64a07`  
		Last Modified: Mon, 19 Jan 2026 21:41:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dddc3dc1a0341fe9af936a10147a2d07116f8e88d81c0c7e2b70091c61b6bd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410373d1530b7ced2347df60dd704f87f0860989be72439e903566ddd260bfe4`

```dockerfile
```

-	Layers:
	-	`sha256:2ddda32af16ff3032981d9b9f3eff0f3a6e583b38978a985d0b01abc6efca828`  
		Last Modified: Mon, 19 Jan 2026 21:41:47 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40868836c9697a635b369afbea4702d5bce3da5c83bef6056e5ba3954043bb16`  
		Last Modified: Tue, 20 Jan 2026 00:24:03 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:0b04db8c0dcba671925f7885e60e7c56148ef788213f4d64f61aba6f495a1756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98254347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a5f91ea9d17773030c09978004770597206edb15d077298c0b12f39df56e23`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:14:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 20 Jan 2026 18:53:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 20 Jan 2026 18:53:28 GMT
ENV GOPATH=/go
# Tue, 20 Jan 2026 18:53:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:53:28 GMT
COPY /target/ / # buildkit
# Tue, 20 Jan 2026 18:53:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 20 Jan 2026 18:53:30 GMT
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
	-	`sha256:7ee8ceecb5a37e7411922ba0485d5dd3cc40ab1953ffe651cbe56f40f79a249b`  
		Last Modified: Tue, 20 Jan 2026 18:54:10 GMT  
		Size: 94.2 MB (94232686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e380b8f90c511e00b91f803659765e9fe11871e6eaee11447a8841b5d2e15b`  
		Last Modified: Tue, 20 Jan 2026 18:53:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c6c9e62c68fbd7ba6397ac172f21e5e434d3c9aa2ad035c422754a59676f2fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f606dc061a9931c510d6d272805761b172d67cc2a69314fa404e63c683d0edf`

```dockerfile
```

-	Layers:
	-	`sha256:1c5bc56b5a70823d08187d1b41e906503610c186e900b6da43b05f959506d6b6`  
		Last Modified: Tue, 20 Jan 2026 21:24:40 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b868528b18f33b77247a0dddbeadfa971ff5667af91b3e7c981a2972f896a08`  
		Last Modified: Tue, 20 Jan 2026 21:24:41 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
