## `golang:1-bookworm`

```console
$ docker pull golang@sha256:55e23b3c4e7d4ba9063c783aaaf2967b7285ecaeb756ff92a16433b882c4675d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:142d465fdd7fb0e9864a4bac6364562823f24081e42053aa63e4c326d54e9c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299341618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b30c54f7d8890673f9bee020521882061f06f899592a843d6e6125736bd2dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c817f6eb2a1d22b828847dc91009271445aa7655a24a4edfe2dfed28f23bac0c`  
		Last Modified: Tue, 06 Aug 2024 22:56:30 GMT  
		Size: 92.2 MB (92230832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c08045297c877b698a8fa5aa6b5d3ec88c34ba7415eb1f83746a1f6babd1cf`  
		Last Modified: Tue, 06 Aug 2024 22:56:12 GMT  
		Size: 69.4 MB (69362558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0f6df320ae4b21423414f205f9f95f5ba6bd75383196599e73e408a672d7d7`  
		Last Modified: Tue, 06 Aug 2024 22:56:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:947dfa2a693dfd9bf0541fe5d2fcd01e3e3ccfeb8b9a15dcb6bbca683ff45c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fd744e3d72be8dc7ca276fcbd7ab0e3ed16a0e2dcc29b9f09ad87b8ae59443`

```dockerfile
```

-	Layers:
	-	`sha256:e1f64b7508b327746bf6b5c625eddcce13559ff9f4ab301abc12cc1752da758f`  
		Last Modified: Tue, 06 Aug 2024 22:56:29 GMT  
		Size: 10.3 MB (10257409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1764e8dadbaf0d839b252d9cb1be33cf79d2ad4d7b98832d3e4e55eda0eacdb`  
		Last Modified: Tue, 06 Aug 2024 22:56:29 GMT  
		Size: 27.5 KB (27524 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:8a804ab08d571b44c6f3678438fb014cd13613a9bc1c7978186f5f5d7e374571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260143972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719062d90cadceab8b6328bf6cf3869dd1e33f2f68df845292e775d28eda3fdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:02:52 GMT
ADD file:0720f70c193e9f94fb459bb92eee636993260decc5545549294c0b9bdaa3364f in / 
# Tue, 23 Jul 2024 03:02:53 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:34:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f609d8ed6026d83f6aa3a833181e8d9c14ca7ab3d98c1dfc289bbd9807a77b6a`  
		Last Modified: Tue, 23 Jul 2024 03:06:32 GMT  
		Size: 45.1 MB (45148058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36910eca5110cc53bc8b0d74e0b5dd2cc4af95aa0a68ba2b84e7ef0d4e42e8b`  
		Last Modified: Tue, 23 Jul 2024 03:46:54 GMT  
		Size: 22.0 MB (21954727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1185bcfb3ddfcc9890c788f4fe00f9a9ad7e2fc66be7241e9e81a7d730324549`  
		Last Modified: Tue, 23 Jul 2024 03:47:19 GMT  
		Size: 59.2 MB (59222815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba288c9524a6e86c58b6d219e99de053c730cd5ad2874ff0bf150aae5e641e5b`  
		Last Modified: Wed, 07 Aug 2024 00:08:56 GMT  
		Size: 66.1 MB (66089221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38353948ef7c4a85c3e42510197b5f321621d39f3094140f1496e3ba11d3156a`  
		Last Modified: Wed, 07 Aug 2024 00:08:57 GMT  
		Size: 67.7 MB (67728993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c303db8ad8242a52c6b9f1fc87d252bfd0390ecbb463ba54689a6aa7d5e11a`  
		Last Modified: Wed, 07 Aug 2024 00:08:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8799f634cb2406faf091c55f5e5eb096a19dc38352f7ff8c755146dddaeffeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10093801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d42973c6cf97b2293e358ad4a7328edbac98afdbeeaf23719010a446d1dd877`

```dockerfile
```

-	Layers:
	-	`sha256:3d237d20c15da73bd20661f74ea3e1497bc31f0376750f77438a135c38624467`  
		Last Modified: Wed, 07 Aug 2024 00:08:55 GMT  
		Size: 10.1 MB (10066146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772ab076d403daa47c1ee6db06b49fa0b901577377d79060ef4c8d73468091e`  
		Last Modified: Wed, 07 Aug 2024 00:08:54 GMT  
		Size: 27.7 KB (27655 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:78304fb408aec6ade99028e97ff5cfc56af6ab8a39995846b0bbe40604808d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289741512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903949e7a61b60fbcb76d82b38a7288e8c28a148f7743d6e4554ee16680883db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d1e618634249770f61f298c9b26207e1d24959e6f27ea9cd2f1bc91bb5fe1b`  
		Last Modified: Tue, 06 Aug 2024 22:56:17 GMT  
		Size: 86.3 MB (86282930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edaf09ec107de8a2f93a55fc7fad71182aeefb0572c5f2e2f498d1ab1fd3b77`  
		Last Modified: Tue, 06 Aug 2024 22:56:17 GMT  
		Size: 66.3 MB (66283242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d874e1aed2b840e3248ad9951e5827e4a8b291cf437cf17803a9b8e5c26e9`  
		Last Modified: Tue, 06 Aug 2024 22:56:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:abfb862dc0884b8a43e31cd92a182fe0e409a2b84e1933ed544b7cc2f2e149f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10313226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10eb488df6fdc6aa90709894772a2943a6828dade926c9a17c08f3743a7a4f59`

```dockerfile
```

-	Layers:
	-	`sha256:8ba1c01d7052123e582b81b1e3b35a3caf92b3c5bc86d9c718b225802e98140e`  
		Last Modified: Tue, 06 Aug 2024 22:56:16 GMT  
		Size: 10.3 MB (10285335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23e154b600feb7782655697d6a30776b862f372d125cee58ec9dcbf2beb009b`  
		Last Modified: Tue, 06 Aug 2024 22:56:15 GMT  
		Size: 27.9 KB (27891 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:87248ae6528fb91b4c6778b4ee56278cf2ff28c5517055b0946dff90de579280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298451351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a8222be806decfc187decaad69d8e14d408953565456ce87d812e4dc94e27a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:01 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Tue, 23 Jul 2024 03:54:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efaef3f6cdf274629a3d4f2c4f9acc4232b4a29e76e45a59befdcd15dee71a5e`  
		Last Modified: Tue, 06 Aug 2024 22:56:42 GMT  
		Size: 89.6 MB (89644820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246b2845dd9f2f6bf65a392e8e3a4218cccd6b1dcbc03a828b579ac7aeea4f4`  
		Last Modified: Tue, 06 Aug 2024 22:56:14 GMT  
		Size: 67.3 MB (67346683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db742ac1d809e3baeff41d7c3ff00ea00d6ea90430ffcff58e96e9237b5e618`  
		Last Modified: Tue, 06 Aug 2024 22:56:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a3be9834ebde098789dfffb5acbba3778d1c7b2e94965e014177453c6fc0c107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afde9e7bd7899cfb2adc32567ab89a0aa6549056f6bc03c68ba9f15798ba079`

```dockerfile
```

-	Layers:
	-	`sha256:36b9aeb930820881fd62bedc532879a73c1131a8d50f05ef90b93fca0540bd3a`  
		Last Modified: Tue, 06 Aug 2024 22:56:40 GMT  
		Size: 10.2 MB (10237667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c472d4f244d4220e90d1ddcc93ac7b05c86e1c662430c60757a500dbfd932f13`  
		Last Modified: Tue, 06 Aug 2024 22:56:39 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:b049b6223a09cc520d0306f25608b8a5d0b8bf92f0991d4e9a40e0cd7962e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270095661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af592bd4eaf4633ff36c54afbb023e6ec8a4a3c292c66c4324312ab1ed723da9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:36:56 GMT
ADD file:bc2014dd4183b8b941ef345add7dfa4a5b389afd70c64828331a9e51522a8c03 in / 
# Tue, 23 Jul 2024 00:37:02 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:05c2d132d3391d998ebae95f3de018ca09dc34d9bfbb160a1b6d662ebfe22612`  
		Last Modified: Tue, 23 Jul 2024 00:48:21 GMT  
		Size: 49.6 MB (49563161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b431e247f5dc02821a251567e4e81f86ada15613f56a6428e9d515728a3248cc`  
		Last Modified: Tue, 23 Jul 2024 01:58:32 GMT  
		Size: 23.6 MB (23636541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b6025db3aeb726503a6d775307c4881743edbf88fbefd8a997f66bb236e568`  
		Last Modified: Tue, 23 Jul 2024 01:59:26 GMT  
		Size: 63.0 MB (62965755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384a4864817e575bb9be405b8211a736dc0d9f4c7a7a3f3a69362908649b06f1`  
		Last Modified: Tue, 06 Aug 2024 23:00:16 GMT  
		Size: 69.8 MB (69804406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec510b2b8fe8d60e2b414c455523b255d2db4e07537481fb550635278f8c2a`  
		Last Modified: Tue, 06 Aug 2024 23:00:16 GMT  
		Size: 64.1 MB (64125639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677390295ff7019b7fabc9ca6abd29b1c6fe12e2b57476435284656da6bd16b7`  
		Last Modified: Tue, 06 Aug 2024 23:00:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2feb75c909ebf27c1de5ac46c68fa91d3bb79bfa2168602f03babe51a3c75e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b0e1f94cdd94e91d19ac71efbb35d1462c4ca885e11e767abee31600a762f0`

```dockerfile
```

-	Layers:
	-	`sha256:9c9d6c07df9800db780266279e283eb439bbf9f1148b285bb4417222353c4271`  
		Last Modified: Tue, 06 Aug 2024 23:00:09 GMT  
		Size: 27.4 KB (27407 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:98cb8c5a3ed3cb6eed1a8ec9b1360ae57df567db1b8642db60ab5f7c8d7b03da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305506568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d03303323dd8837781237a22bae82b2a1a3b9fb6a8716ccc49dbc3f26de261`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:43 GMT
ADD file:4c03acbbfde6668c4063631c28ab78e7a946936cd04ff5e70ad0c4c31002e72e in / 
# Tue, 23 Jul 2024 01:26:45 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d2bd554d7c1800c60e12fa0592644a8a0996b7198d6b9acc54de2b97ceca080`  
		Last Modified: Tue, 23 Jul 2024 01:30:49 GMT  
		Size: 53.6 MB (53557034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b62a22b9a049c9f95de177f7487bbd79f2210b069b22d4bcb70a746b369250`  
		Last Modified: Tue, 23 Jul 2024 02:41:58 GMT  
		Size: 25.7 MB (25695545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820239b953ebf111106a2c9f4d7ea847e4b73b2b422aaecff3b5ee0f1771ba9d`  
		Last Modified: Tue, 23 Jul 2024 02:42:17 GMT  
		Size: 69.6 MB (69582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c6079496e8075450646b804bc7561fa8e5a51a5e6ea5ecc8bb95e91d1b70f`  
		Last Modified: Tue, 06 Aug 2024 22:57:05 GMT  
		Size: 90.2 MB (90217721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa907a73ecb9721e6fd07eeff45b3daafd73705b1b26a4ab050075d2da72289`  
		Last Modified: Tue, 06 Aug 2024 22:57:05 GMT  
		Size: 66.5 MB (66453881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a21c8cb3eff742a557bca6af5e67c7fb11c78c96a3ee5bb3605ab7b3c9bfbca`  
		Last Modified: Tue, 06 Aug 2024 22:56:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fb1a58d3db0e9b122017e81c5fc463e4d5292e8d8715cf2ccda5aeb407ccc776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10257855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6e3d2f3bbefe1a839f98ec9131cd8c4d9566b0c21fce53f0460ceed9f835a9`

```dockerfile
```

-	Layers:
	-	`sha256:93538a60a38af45702d55646c1d4c70d748872296e749031aebe3bf9355e588a`  
		Last Modified: Tue, 06 Aug 2024 22:57:03 GMT  
		Size: 10.2 MB (10230262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff1b3ef2842bf300bf20068757b5f7d562229efe3e0a459f851c74ea9b9c84b`  
		Last Modified: Tue, 06 Aug 2024 22:57:02 GMT  
		Size: 27.6 KB (27593 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:856bbe1613b7ee1894179db4d7bbcaec30b2089bb0acc421446d48719b9231a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272320948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663003f3c2fa9446546e507ae485bc9ecbd560275489535c25b7460acaed1b5c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 19:33:45 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 02 Jul 2024 19:33:45 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 19:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jul 2024 19:33:45 GMT
ENV GOPATH=/go
# Tue, 02 Jul 2024 19:33:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jul 2024 19:33:45 GMT
COPY /target/ / # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jul 2024 19:33:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4f87d9d3d1a12e583bfd5c38f6805e9600ccb4b6fc9d71add6b80cbaed626ca5`  
		Last Modified: Tue, 23 Jul 2024 02:32:29 GMT  
		Size: 47.9 MB (47931525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4649256f3bb52f19db7f8b7f488538d723236cd6b0819dadbf70b417d1cf1e`  
		Last Modified: Tue, 23 Jul 2024 03:14:23 GMT  
		Size: 24.0 MB (24048784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ece0de0d68a1bb10e9a5909215d95a2dd64145cb7cf0cee0748ec861449f71`  
		Last Modified: Tue, 23 Jul 2024 03:14:39 GMT  
		Size: 63.1 MB (63125117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e029c6b6c3eb45cdeb91c216fc1a75e4d6c3b9863aaf0fe26be152a47e02e170`  
		Last Modified: Tue, 23 Jul 2024 15:52:43 GMT  
		Size: 68.8 MB (68803794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36325bf1498477d36098ce5907eb7a794a2e7eb1ff088a91163f8cf4d9ca6b9`  
		Last Modified: Wed, 03 Jul 2024 01:08:00 GMT  
		Size: 68.4 MB (68411572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c81dbf8fe364500b0ccc6bb80b53cab37618501f2a4f18f7838e9904fe4f5`  
		Last Modified: Tue, 23 Jul 2024 15:52:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:26daf21371a83c89fed6b86a460bc5993a3ade8aa4ac92d075e24199a375196b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e05fd6a5636452b051074f94251a5ac198a5846509e956f7c4fb96c9dbd0822`

```dockerfile
```

-	Layers:
	-	`sha256:0defc4249d20f91d8f8d3ae146b2e1011231a6b3e682bc29dd27326591db0af2`  
		Last Modified: Tue, 23 Jul 2024 15:52:42 GMT  
		Size: 27.3 KB (27308 bytes)  
		MIME: application/vnd.in-toto+json
