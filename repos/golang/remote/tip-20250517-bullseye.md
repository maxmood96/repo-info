## `golang:tip-20250517-bullseye`

```console
$ docker pull golang@sha256:790f8e1b7a91c2773d53a0d4ffefb3082300c04c08ac9583e85a24e63c4375fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20250517-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:c7d749059883258e979f28ae289e052620d7e3503662d181a5478afdc223583f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343594514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ae37541a02da82eeee1bceadc06a7b9cdff75bcda038167ab57c5e69a93eb6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b0dddba96b261d43c8ee32aa2e55e3ba144538bd240a5f61a6949850a2832`  
		Last Modified: Mon, 19 May 2025 23:29:14 GMT  
		Size: 91.7 MB (91712937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152514912bccc29796b149fde0366f2c5aabf882d40321f8719bdbe9b9c2cb5`  
		Last Modified: Mon, 19 May 2025 23:28:50 GMT  
		Size: 127.6 MB (127614129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6396f2daf6ec7d74233617af66732ea890edfae83dc247de56e2f0e15fcf11b0`  
		Last Modified: Mon, 19 May 2025 23:29:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250517-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:6a64fc6642e4cea3bb02203312b191f12b9e6d13f1e9248cb371fc65814df168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10342120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e09b2fa59d63b4aadddcac3e14e6e5e49157c5ac79972193b2245a71c5f3712`

```dockerfile
```

-	Layers:
	-	`sha256:68435251dd09843f111fef54253715ab54e7e2cb71e0a97238cd77e8af8dd9e1`  
		Last Modified: Mon, 19 May 2025 23:29:12 GMT  
		Size: 10.3 MB (10315059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8402d49c9262a0abbb9b380a13fb69d878eb5677b48dd5f0f77590520f989374`  
		Last Modified: Mon, 19 May 2025 23:29:11 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250517-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:2b30fbebb4111d80dd597d594f6878a4ad6c6e7f9b022bdbe9b030d63cd00178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301975039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29e24323ddf5a68ad884e4f67c2ed888064749600a9edc453de55be1cb2e0d9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dc7e83fbdf292bf0238a22da7ed8a7b954d4a791ff1772973394bf28d278ed`  
		Last Modified: Tue, 29 Apr 2025 17:00:23 GMT  
		Size: 64.9 MB (64922699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57e96661f23b74a5007ca5b539e5d28d960192676ad8b6b38063081e7fce05`  
		Last Modified: Mon, 19 May 2025 23:31:19 GMT  
		Size: 122.5 MB (122507949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53021caa77e8d08a82b32675a78bd202238304d118ac9ec4988bf29897a34997`  
		Last Modified: Mon, 19 May 2025 23:34:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250517-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:1242197fb8961ab123cdfa9dbfe21d8f8d702495701d9b626d2c2776631037cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10146167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18aa9e461823e9e98ce63e17fab4c60653cf4efa7b9b7b19425d99d331baff9`

```dockerfile
```

-	Layers:
	-	`sha256:d4bb2f0dcb9766a8eeeb977c50cc83fcd44cdf8fa1ed26ba4f0af4e1bbc5a364`  
		Last Modified: Mon, 19 May 2025 23:34:44 GMT  
		Size: 10.1 MB (10118998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fe4fc15f9fa6327855648ec0b2fccc97028c4f0d20ab531d0b8a9cafccedc2`  
		Last Modified: Mon, 19 May 2025 23:34:44 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250517-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a560a2adec2884b207d4ea2330d15d3adc9ab20e8becdd719e1f41b454ef6f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.5 MB (324525523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3cd2d3b1ee00ad23f32144c3c18fd10a3ac1501dcf9f27f1448f262773be95`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c6322f6933d3c7c501627d667e914654793c3d67e2daa5122b6519e08d8af`  
		Last Modified: Wed, 30 Apr 2025 02:35:23 GMT  
		Size: 81.4 MB (81414127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af8027226f07cd540ce15387789410501e4b5b5d00ffa1a05fcb1dc81e7e9`  
		Last Modified: Mon, 19 May 2025 23:28:57 GMT  
		Size: 120.3 MB (120266151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd26f44229d4b8a1cb708cbc7e648b04279d22ba7ae00321e28d6e33058d7acb`  
		Last Modified: Mon, 19 May 2025 23:31:13 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250517-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:df4f1b14a68fc972abde34deef24a6dac6a4e488f47dc6b356b613b752625dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10342297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56b851dc28d0c8b0ebc40249082b44e38ba90db7a6d6996f15519e7a3b60343`

```dockerfile
```

-	Layers:
	-	`sha256:271e1bb9deeb8fa4aa293cdc2f5d9c4f454439c6d7390d74ce44e7440cbf383d`  
		Last Modified: Mon, 19 May 2025 23:31:13 GMT  
		Size: 10.3 MB (10315100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617c4046253823c542f038acc456d211c388b5acab34828e6dd81cf273c3123a`  
		Last Modified: Mon, 19 May 2025 23:31:13 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250517-bullseye` - linux; 386

```console
$ docker pull golang@sha256:5b7176cfcc692cc45ad1c1ee889543b08d7470cc1536f454cf962348a8637770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345406550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50d3b79cfc395949b5c3f48355ee3b1e50281e7d66b47a516ba297c4ae957aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a88766b95a2f208cdc40767a07e47cdce7dd9c4028fca752f5d8e3ee2515590`  
		Last Modified: Mon, 19 May 2025 23:29:36 GMT  
		Size: 92.7 MB (92711171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24d8be6f5d36fbc3aec81708ca11efa4fc67dbd10e5ba59a5e7c3fa29e59478`  
		Last Modified: Mon, 19 May 2025 23:29:26 GMT  
		Size: 125.7 MB (125697440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98e21891196147a58824632206a6fb657510c80020000121d602b35083355f8`  
		Last Modified: Mon, 19 May 2025 23:29:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250517-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:358f68ef0c4d85c9f129d6fab53310b4667176bb0bb4e676ae1104abc08025e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a520174610e66de6adea35bd7500bb8a00ecd1a7906d2f77f425b53dd5958f`

```dockerfile
```

-	Layers:
	-	`sha256:b658b73ac796ea9e9596a0ef5aa6090c36537a0fb012d865cd5d414b7b8c2fbd`  
		Last Modified: Mon, 19 May 2025 23:29:34 GMT  
		Size: 10.3 MB (10304372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c55bdfb74527fc5b21b32be7a23f64c5a621fe902a9890631ebfad9a96544a`  
		Last Modified: Mon, 19 May 2025 23:29:33 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
