## `golang:tip-20260606-bookworm`

```console
$ docker pull golang@sha256:db564fd27a7657288603e876a92d6f8c8b22fb4ac1a5063444bfe9a53ab8452b
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

### `golang:tip-20260606-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:b291575567db8ce76e12a5b35854547741344da387e338b39a0e4500b3738d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331477454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c546785f32aafc344cac86b6745fc5d30f1d655a6cac75e48c16a151a8cc891`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:46:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:46:33 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:46:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:46:33 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:46:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:46:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc17f5bd527f995b02d3e50ba4039d983af556b457df949ad81d7d0efbae51c3`  
		Last Modified: Mon, 08 Jun 2026 22:47:02 GMT  
		Size: 92.5 MB (92481670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9caf2b5917603f564e8b31c080871596acbc699caf5fd0fec4940c836746ec3`  
		Last Modified: Mon, 08 Jun 2026 22:46:13 GMT  
		Size: 102.1 MB (102052370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d02901f331647b4ee58b7d57f4075e04e990bec4b4b945cfe38a4954354e9ee`  
		Last Modified: Mon, 08 Jun 2026 22:46:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1e6d5694318afeb6f9f197df06eb67eb3585565b1616cde893416d4dfc538c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842bc05543ac65ae24c5368bfdd54b4b1d446474da94c6781b04ea3113f9902a`

```dockerfile
```

-	Layers:
	-	`sha256:b1010a53de55d6a81a91810f83208c37cbf4299d4c6258d7e3164350ffba4f7f`  
		Last Modified: Mon, 08 Jun 2026 22:46:59 GMT  
		Size: 10.5 MB (10497055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8759e0a20dba15b0bc6722a0ba318e9535677153799e971f895897112c8ff802`  
		Last Modified: Mon, 08 Jun 2026 22:46:59 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:ffd74b7d1fef7f356be84b760a715696512b08ee5adbb741a69d567435b05d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289895106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755425fe292b1cc781c8ff45b7b631c199bc6be64dadad65d8136c538494aee6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:48:10 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:48:10 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:48:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:48:10 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:48:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:48:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56a54e4354794da97ac9fe5173f689d775d13afa792e8b390e49425c3caa6b5`  
		Last Modified: Wed, 20 May 2026 01:34:11 GMT  
		Size: 59.7 MB (59661818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904667d9e17358fa4e443ff3fc977db6bdb8bc42601ca587c637e9e923c6df2`  
		Last Modified: Mon, 08 Jun 2026 22:48:38 GMT  
		Size: 66.3 MB (66338807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017a74f67fe3bf0e9dc5d0c334ab5929b4a454a86c2f391ecc6e1d3f6697e53`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 97.7 MB (97735035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab6c2f34eb4a50e81841a803932b6cddabdef87cf3388f6ca98b4609bf52fef`  
		Last Modified: Mon, 08 Jun 2026 22:48:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d73c37812f5e6ae2579fa4bac596a217aa603ffe39a50d27f2179a372561f39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16dceb5f93fce48e48849be06d30a2bd9dab5d2cc568e6241a32629689e9b28d`

```dockerfile
```

-	Layers:
	-	`sha256:26a2a8c0a08ee7ca3d8b68d4c3c7f3ac71ab8f83d40a57ad0d06227884dd77b7`  
		Last Modified: Mon, 08 Jun 2026 22:48:36 GMT  
		Size: 10.3 MB (10303751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52eedd6db3ae7705e7f87f4fb3330e125682595d3c4d994ec8cc35e869ac6bc6`  
		Last Modified: Mon, 08 Jun 2026 22:48:36 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f1d039897deecd852125e3c46c462b8d5c0073404e3008141941c9ee24d94308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319504667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e8c3dd3b934bc48d829e55abd57e773b076553627128731e7142eea544d85e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:44:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:46:13 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:46:13 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:46:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:46:13 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:46:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:46:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3651da3ffae94e0e570a49224fddbae99b511524ad2cd95001dbfafdb7b3b0`  
		Last Modified: Mon, 08 Jun 2026 22:46:42 GMT  
		Size: 86.6 MB (86554611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2308f1cb629a8c8fe52b3b591bdcfb51ba3716d584492ccac8858ffd19fbe4d4`  
		Last Modified: Mon, 08 Jun 2026 22:46:27 GMT  
		Size: 96.5 MB (96469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57313919ff935afa10f29da0986841499d46ad0a1650d920a07fe69c2013df57`  
		Last Modified: Mon, 08 Jun 2026 22:46:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4876178c998364a86feba4d1db9799843393d659ce04d5553df3f646ca50dd2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db7e61b0f2c24d32069cac8b98a2c0e360d0642de2ae9a3208a84ad4372594f`

```dockerfile
```

-	Layers:
	-	`sha256:1bf832e30bbdd51a1a7cbed21f0841b9552211073275891209116c0b4b483fec`  
		Last Modified: Mon, 08 Jun 2026 22:46:40 GMT  
		Size: 10.5 MB (10524879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7efe32bd565bff3f59f3b26c7f23ba1a7a17e0595a3c67950ddf196031365a`  
		Last Modified: Mon, 08 Jun 2026 22:46:40 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; 386

```console
$ docker pull golang@sha256:51e3805060fb282534dcdfbcfb3afb0331181293b0cfdbc4d4f2a47fdb70e689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330288585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8b01de79041a2e2c99b818a6614bbf30fda0a7e69d03fc5f95b6842775c821`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:45:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:47:28 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:47:28 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:47:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:47:28 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:47:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:47:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2a05321daf588afd8b06b380f7ea0a3d7c0de2097ec6f355a74453e7ec6af`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 66.2 MB (66243865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eee686700d5928cefc6204dd62fb10cd53f3747a85452da838275205b69a8b`  
		Last Modified: Mon, 08 Jun 2026 22:47:56 GMT  
		Size: 89.9 MB (89903951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c856874e83d87ce8611744942560effd5d1e879f3a49a6259f9e0f789a54f9b`  
		Last Modified: Mon, 08 Jun 2026 22:47:42 GMT  
		Size: 99.8 MB (99778009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c371f91988b68642ddfa1ba5be7bace499e452713d2e9305be46f926a1ac6a1a`  
		Last Modified: Mon, 08 Jun 2026 22:47:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:27584d1848c9bb86d5cdb58fb345813b855cc774cb665b0c6303115b0634d50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1726cddd598016763addaf33b10475537c5def72f59f9d893320e7e26bbdc4c`

```dockerfile
```

-	Layers:
	-	`sha256:6bb04346d386136473bdad416a59aa549b6c3291934f60fe71f34592d7e7e0cc`  
		Last Modified: Mon, 08 Jun 2026 22:47:54 GMT  
		Size: 10.5 MB (10476635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c5651ce19170388fdc321cd660b451dd82bb7fc20bd99a3eac160d3efb38b33`  
		Last Modified: Mon, 08 Jun 2026 22:47:54 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ea9d993bf7a5d44bb2f592e60814e2a2364271b637ae7b2ccfe7c9599e803695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301237555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47cf17832096fbe1adfedac5b35d53e1eb3bab8d919224473bbb02ea14bc4fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 15:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 16:19:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 00:49:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jun 2026 00:49:01 GMT
ENV GOPATH=/go
# Tue, 09 Jun 2026 00:49:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 00:49:01 GMT
COPY /target/ / # buildkit
# Tue, 09 Jun 2026 00:49:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Jun 2026 00:49:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853b2ecd2cc91271c3528597da43fc45c41515894834d1de212a390afbf0ade`  
		Last Modified: Wed, 20 May 2026 10:05:32 GMT  
		Size: 23.6 MB (23621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf4bd887b67ee95b1804bd893717310da36bddd5a598cce7e9b621ff52ee05`  
		Last Modified: Wed, 20 May 2026 15:12:43 GMT  
		Size: 63.3 MB (63316337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d8edfd178bcf28b946d64eb3ad538d4ee96dacac854fd44ba3af295e68b368`  
		Last Modified: Wed, 20 May 2026 16:21:18 GMT  
		Size: 70.1 MB (70084514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb92ec573830782d1ca10f30b4f9a01477e80ea6a11033a9eddfae8ecb46681`  
		Last Modified: Tue, 09 Jun 2026 00:52:05 GMT  
		Size: 95.4 MB (95429106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8309b5ad60730b52d1fed4597ca8807ce124ceca387a26feab1d8f3ab4d7b2d0`  
		Last Modified: Tue, 09 Jun 2026 00:51:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5e5c51230604e3639b26b49798484c6b1c64409c1faee75c74b575fa496393c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd476f5d88d7fd37ad9b7623d6ceb3535bd728f2959869a5c3ce4e47efff4f`

```dockerfile
```

-	Layers:
	-	`sha256:964c6be7b8bfb44589fa18b34c23b8874b28d3ee0a6363b2e926d23fde56082a`  
		Last Modified: Tue, 09 Jun 2026 00:51:52 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f7aafc7587ede928b8c036c3b98c2f0312c527c6dcc922f156845b2f3a532e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336803225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f412d7b3e213cb5198ff7c012c9af331cd8d3b7b3540deb7da05870e20670f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 23:06:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 23:06:07 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 23:06:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 23:06:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67cb71cd5984ee53ab56bef57a29d3b0ef6e8939c352146b1efe66402d4c7ff`  
		Last Modified: Wed, 20 May 2026 06:51:27 GMT  
		Size: 69.9 MB (69853485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0548bbd70587587ebc4a21c63b5f4bd00f3fc220c1a3dc53c1a1b9debf81aa66`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 90.5 MB (90495650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d5d0b8da3315c28f7e047d6d8c920d4423531520a738d9dbd717fd24afb93`  
		Last Modified: Mon, 08 Jun 2026 23:07:16 GMT  
		Size: 98.4 MB (98427267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5778b7a3a72f40e37771cf0810028b6f21ab903020915686feec1da23d7faec`  
		Last Modified: Mon, 08 Jun 2026 23:07:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:72b27b298677b3e8d070e5ab508395e87768c1d1c7bde04449ca2577c50a125a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f517914df79d9313c91a6716842b3ceeb2cec95ccca028583ad2f68b93421e54`

```dockerfile
```

-	Layers:
	-	`sha256:c9737c6316324c6d5e55039bee74701c5f49db0c6d9d2fe05feb5cce630fc6f5`  
		Last Modified: Mon, 08 Jun 2026 23:07:13 GMT  
		Size: 10.5 MB (10469540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b0a99d34c1eaf2c303687207fa5e7e2de4017296ff8840ee83eb8541b1d66f`  
		Last Modified: Mon, 08 Jun 2026 23:07:12 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:50dbd3618d7f5a49db90d0ce0498a16dc5b11e0fae34617bd96942b0021f1e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304272503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429bbf6985f753e87da4eda1741f05a8587d371883a47c6b914b154aac693579`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:52:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:52:26 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:52:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:52:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f90b46dcc8622719e19e9e04b1bcb5bc39309966d69636e349c233ba832e30`  
		Last Modified: Tue, 02 Jun 2026 16:42:45 GMT  
		Size: 69.1 MB (69088003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56217687aa3cc648280b9c7052cd68f26077339d92dab45c68b721ed5388981`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 100.5 MB (100491232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd08ea32efd9c11828b1255d55ab235bb8c1c583bee295d934ea31598fce050`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:273e5a43e244d5924bbdc4767314a4dff32a3f6bb88de9685c20ebfd2507919c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a7cdbbb57abc0c03c2ccf94f6a45f999fb3481d1f5963277d86ec05ad508af`

```dockerfile
```

-	Layers:
	-	`sha256:698115f10be521fd06223098e65a12e9b483f4b1c345620b3eda36b15a4b92fc`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 10.3 MB (10329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716a0f057098121180cb9a966d1cce91bda9e050aa2170f742ccf0e93cb697cf`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json
