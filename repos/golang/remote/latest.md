## `golang:latest`

```console
$ docker pull golang@sha256:305aae5c6d68e9c122246147f2fde17700d477c9062b6724c4d182abf6d3907e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:63faca1fd8d85713bc6730e51a31a1155d19703a1e2637627daeb60729573b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39037e2be1b348d071dea0628a94d1559c0c0102f44102632ca343473d63f5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Aug 2024 18:18:42 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Tue, 06 Aug 2024 18:18:42 GMT
CMD ["bash"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f02cee7a92d575f9531397d0f4f9de025996c9d6e3b90dbe9a2d76dcec82d`  
		Last Modified: Tue, 13 Aug 2024 02:05:33 GMT  
		Size: 92.2 MB (92230622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c08045297c877b698a8fa5aa6b5d3ec88c34ba7415eb1f83746a1f6babd1cf`  
		Last Modified: Tue, 06 Aug 2024 22:56:12 GMT  
		Size: 69.4 MB (69362558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aa3786ec5fc20b549f7fe03f6b9e12fb2e1120b786fc611baca0c01fc4288e`  
		Last Modified: Tue, 13 Aug 2024 02:05:32 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:3097c8c1341a6ff3757cbf0b8dc22d495ffedd811b7b72be21c47c93a135450d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf07197470983d4e8c36596207bd67e62a1cb8bdc2dcb3c0edf262eb6af46de1`

```dockerfile
```

-	Layers:
	-	`sha256:11ca4ac20c04380b26ea6d6ed0b32e0fe0d5660b604841c11adad3db77b742aa`  
		Last Modified: Tue, 13 Aug 2024 02:05:32 GMT  
		Size: 10.3 MB (10257409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b1e06cf207562c4d7c1772c16da617341db898a406eb1a2c84cd67423b9121`  
		Last Modified: Tue, 13 Aug 2024 02:05:32 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

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

### `golang:latest` - unknown; unknown

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

### `golang:latest` - linux; arm64 variant v8

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

### `golang:latest` - unknown; unknown

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

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:8ae92b0f1598356df80f4e9bd682c4cdbae8f1a3fc9cee1f05ce88a00462f05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298451422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87dc27bc5cd8aaff4b6579229d92b391e75ded6308e66d5c2ed84b3e9b8a9ee1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Aug 2024 18:18:42 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 06 Aug 2024 18:18:42 GMT
CMD ["bash"]
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
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
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8689b3f6e17656c27a59573a3e44e3b600a79271a09cf64fb87bc31cd68ac0a6`  
		Last Modified: Tue, 13 Aug 2024 01:13:40 GMT  
		Size: 24.9 MB (24891499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3393c41a8406d190eb7fe061fde8daaa2b0fa20c672505d04631bd52a1325`  
		Last Modified: Tue, 13 Aug 2024 01:14:02 GMT  
		Size: 66.0 MB (65988846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e4669f96b4d6920c1c88d460383b24621e38fdb672d91622b5435dc41713e8`  
		Last Modified: Tue, 13 Aug 2024 02:05:54 GMT  
		Size: 89.6 MB (89644805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246b2845dd9f2f6bf65a392e8e3a4218cccd6b1dcbc03a828b579ac7aeea4f4`  
		Last Modified: Tue, 06 Aug 2024 22:56:14 GMT  
		Size: 67.3 MB (67346683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4588000f1c19583392b8d06b235e355581bade6c11ee8188364be9e678f97d4a`  
		Last Modified: Tue, 13 Aug 2024 02:05:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:425e83d1d3b06ce3b73f8949c903d3c2d0af15c1dda0754c7350880884f41def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ec430b42797e633af20f69939b8e992356d0ed7529d7790d1f9fed918fdaa2`

```dockerfile
```

-	Layers:
	-	`sha256:61c3ba7830526821359b0f7787c3c69103afa17d457ea63311ff76c3c0ac494c`  
		Last Modified: Tue, 13 Aug 2024 02:05:52 GMT  
		Size: 10.2 MB (10237667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab2eda2aa089532985336b8a8a96265d1c160fc8bd863492342a9f964fb91b84`  
		Last Modified: Tue, 13 Aug 2024 02:05:51 GMT  
		Size: 27.5 KB (27474 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

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

### `golang:latest` - unknown; unknown

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

### `golang:latest` - linux; ppc64le

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

### `golang:latest` - unknown; unknown

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

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:77e43fea0f4bbdd4138d56ba40e896f6b96069d700aae7e141f2c05d56ff3fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272330782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d47b27a7d325d4ae5591a6d9e053975a58c856937db2c29f4ed3b4fd205d975`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:27 GMT
ADD file:9880abf9fcde2467a1b0168e3bfe59ec79b20177b6deafdce0bce74d155da254 in / 
# Tue, 23 Jul 2024 02:27:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:05:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:05:38 GMT
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
	-	`sha256:6595192cc94e229d993517278145a78a10c23a885c080ffcd19e97a74f180eff`  
		Last Modified: Wed, 07 Aug 2024 01:54:05 GMT  
		Size: 68.8 MB (68804230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4f522c886389638258537d7ed45e62dbad030e5ed340cd291df30569fc9288`  
		Last Modified: Wed, 07 Aug 2024 01:54:06 GMT  
		Size: 68.4 MB (68420968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f7f1eb41bb96f5f742ac40dcc894d30f1b7995564bd1e690ef4a6d53c03e4`  
		Last Modified: Wed, 07 Aug 2024 01:54:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e6997e042ac3149006703f6cc9e62089a647d3be6caa33ca3917d791dea5316d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10121335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4676e8a7562f230e1785f021bc78edb2f97793ef6c2cbbff3e47e2a88c6c321b`

```dockerfile
```

-	Layers:
	-	`sha256:e59dfede12bb94fa3d1f68ec080ed96540be201102a0e815b96d6ae33e3008e9`  
		Last Modified: Wed, 07 Aug 2024 01:54:04 GMT  
		Size: 10.1 MB (10093808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4619ec6d32588ef6fbb317cbb131c2904c19ac3ce592f184eef3c9de66dabcc`  
		Last Modified: Wed, 07 Aug 2024 01:54:04 GMT  
		Size: 27.5 KB (27527 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.20348.2582; amd64

```console
$ docker pull golang@sha256:7637c7373102d976b3cca870e77aece580b8f3ac03fd98e142c7ed6a934da849
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2237103691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7654f1dcb66a061d38b396d055408d4e3b1d85f73580b94311a157640d0b94f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Tue, 06 Aug 2024 22:56:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Aug 2024 22:56:09 GMT
ENV GIT_VERSION=2.23.0
# Tue, 06 Aug 2024 22:56:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 06 Aug 2024 22:56:10 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 06 Aug 2024 22:56:11 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 06 Aug 2024 22:57:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:57:20 GMT
ENV GOPATH=C:\go
# Tue, 06 Aug 2024 22:57:30 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Aug 2024 22:57:30 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 22:59:09 GMT
RUN $url = 'https://dl.google.com/go/go1.22.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6023083a6e4d3199b44c37e9ba7b25d9674da20fd846a35ee5f9589d81c21a6a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:59:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab43240dd2735372d70461d57a5491631d655ca1e301e5e9e5241f4d383f5ba`  
		Last Modified: Tue, 06 Aug 2024 22:59:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc03124665d1ed7f649046d5c428f6c6a51ac751a9b9351cb019450c5a3f2f29`  
		Last Modified: Tue, 06 Aug 2024 22:59:15 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c0d6bad3dbd7733cc22b59a014d7693aed7a3410806b7c599911bcd121889`  
		Last Modified: Tue, 06 Aug 2024 22:59:14 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f96585631a593d5afb9e8c44e29f29637fd34b074c0c018634cd0797d846c0`  
		Last Modified: Tue, 06 Aug 2024 22:59:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b101c5e86f2618ac4a982a40275f332bf9e3bb3776a079104ce3c54737c578f`  
		Last Modified: Tue, 06 Aug 2024 22:59:14 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5ba128107217d579d9a32654f909e3989122d46cc3a0bdd874467cad8d8567`  
		Last Modified: Tue, 06 Aug 2024 22:59:16 GMT  
		Size: 25.5 MB (25451374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9f7e14c690501a1170f1397428dc368941e3ee35ae4ee4a172194a30d8dcc7`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a267841d80890728c7b3ee800534c6c02fcf933aad5db3638c73be7c086bd033`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 314.0 KB (314042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930959aa4e525dc6464a16f9f6ad649425f6148d0a4d8d80b825e4296369aed5`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b089a5ae45e51abcb4164dc126b61d598e40ed6521b33a963cd2a65c3f5db9`  
		Last Modified: Tue, 06 Aug 2024 22:59:23 GMT  
		Size: 71.7 MB (71727545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014f7f8f75a716c9eb5c7d5bbbb5e317daa47b1f39c4f4bebec70d16599bed7d`  
		Last Modified: Tue, 06 Aug 2024 22:59:13 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.6054; amd64

```console
$ docker pull golang@sha256:1fe4ed239c2ce94d4fd1eaaa7cddc8953c8ade5bf1bba79648d6ba18b532d520
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336123924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ff9174fec453960d29f8723fa322bfeacdd3cf4b19ffc579e958ffdcc952da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Tue, 06 Aug 2024 22:56:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Aug 2024 22:56:01 GMT
ENV GIT_VERSION=2.23.0
# Tue, 06 Aug 2024 22:56:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 06 Aug 2024 22:56:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 06 Aug 2024 22:56:03 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 06 Aug 2024 22:56:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:56:46 GMT
ENV GOPATH=C:\go
# Tue, 06 Aug 2024 22:57:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Aug 2024 22:57:06 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 22:58:59 GMT
RUN $url = 'https://dl.google.com/go/go1.22.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6023083a6e4d3199b44c37e9ba7b25d9674da20fd846a35ee5f9589d81c21a6a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:59:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09177a2d8100731d191cc1f7268068fe9838aeb2c4082ff06b328709fd7ebf65`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f430bf25eee4267b1d84ea64815fb55a7d7cf85c8fa78ddd8485a195fb00cc`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0976710052c049e2f19bcbec09e706ab0805f3007984ffa21d58be92599740`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8186263fc237d42bb6e9f2bdf27e324ce393fc351732137e2a6f0bf6af1a256`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2b3aada17941bcb5f4d65c437730c3eb6330eafac2adfc5be0cfcb842b12d3`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb29c5f1c6b570e746a18be662c5fed69c91c6f9cd49817ddd368ec3d00945b`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 25.6 MB (25580557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9fe7afd5b5f0e04a762ae3584205d38d916b2a97b79b270145c6c999e92ac`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f752cb947fcbfa05ceaf706a0e7d09de2c5f6fb064c02e3ba8c08605e18e9a`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 342.4 KB (342379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5038a529a813e24653c828b04cedfb004652d03694ddf4285d057586181e3f`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a4a42e8184621546ae9b99673a7b5f26572753cb40d4f37e5786941b715f63`  
		Last Modified: Tue, 06 Aug 2024 22:59:15 GMT  
		Size: 71.8 MB (71761086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d71452634c4b504306599ea0b3fa0e112063e9436c281ba1b78b961368864b1`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
