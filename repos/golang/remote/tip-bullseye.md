## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:3bb9813a6cee327dce995439ffc10986bce4b645de7b7c7194f721f51aec9540
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

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:83169a05a5d395c21e7de25257fed11d39ae23c4935ce0718a33085890b6f977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336924632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346d88e155a510a7224f44c682d9615c6e6c1a7543e5fb9fcc6699a49a467e5c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
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
	-	`sha256:380df467b2c00e27480b4b19de7c220ff1ffb2ea899436df46540f0d505e83ce`  
		Last Modified: Tue, 29 Apr 2025 00:14:24 GMT  
		Size: 86.0 MB (86000838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65846c33088373b4d6ff39b83056f623dac3e1cb831137df32e4e70bf9d848be`  
		Last Modified: Mon, 28 Apr 2025 18:22:59 GMT  
		Size: 126.7 MB (126656346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0ff624f204cc263ecbee9c5baeaf0fb18cbc9ce066a5ce846c7609011d43af`  
		Last Modified: Tue, 29 Apr 2025 00:14:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:4c4f1145aad930f709e29b4fc044dc5784efe53a41da6e6b649d7fa071fc21c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b06577f25f51f31e7ccd18a44e4fcb9dc9540456f3f545bc2128fd6905a67`

```dockerfile
```

-	Layers:
	-	`sha256:9bd8e83fcb71aa2ab8b9f50886dc8a4ba253093a7cea59974140cbcdcfa61f45`  
		Last Modified: Tue, 29 Apr 2025 00:14:22 GMT  
		Size: 10.3 MB (10266397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b28d4f8727a210d5c8c41a2d1ba516b568e02f32a9acd4c241efb2facb276c`  
		Last Modified: Tue, 29 Apr 2025 00:14:22 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:021876b0696fde9639c7efdf54db97745195a4c37e86004d8d8f5194ddeb9d78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301141821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55742d8ef6ebc49a23e522c4587eca4ee9cacbae7e9cc03004022d7329e78219`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
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
	-	`sha256:e33618dace1ba528dcd7b40e80a4e895530a8d058bda71f5a87abf8312ed70c2`  
		Last Modified: Mon, 28 Apr 2025 18:46:15 GMT  
		Size: 121.7 MB (121674729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ceea6a7636866521ad3aa1c655845cb34684f7da1aa9d722269515407ff13d1`  
		Last Modified: Tue, 29 Apr 2025 20:36:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8948ab289f453ff411081e7682a8b62c6934738167a6412d00204b7c1c095573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10099905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1f84d652f34ca3b3fd31fa6d892e06081c28fb7ab7c277cca95cc1fbfb42c3`

```dockerfile
```

-	Layers:
	-	`sha256:1dd61536f11426bff7aba2ecb69e57be4feddccd8902a9c75e1de0f548dd07f3`  
		Last Modified: Tue, 29 Apr 2025 20:36:23 GMT  
		Size: 10.1 MB (10072737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d6c6e944e005a6ad3ad5e53216bfa76c93df538a439250b7f987da5f9edbe7`  
		Last Modified: Tue, 29 Apr 2025 20:36:22 GMT  
		Size: 27.2 KB (27168 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:227e5eef20cee0ecf69530d772e8588a8f81815dee1f04bc394b179f761899c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323659762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf81a9d6f202a3f36100c306df1503c82e92cee44830c594297f3af3bd97c59`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
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
	-	`sha256:280b2cbe9b185a145cd427125ccd35e0250a80679d21036014ab14fdf1e6e707`  
		Last Modified: Mon, 28 Apr 2025 18:48:43 GMT  
		Size: 119.4 MB (119400389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12c9ef03829f9f93482e2f4c6cb93cd98b206c7cf209957447bf934786176b`  
		Last Modified: Wed, 30 Apr 2025 06:52:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:22e2e63b0e43db234186ec7ab155fbc3e28bc08bae5ea9c8459a0b0002c870c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86d9db00e40a68e08191a7a00aed73c15862b42bc03fec2a91c08443f1d87a8`

```dockerfile
```

-	Layers:
	-	`sha256:88170b2f4d9a098fb655bb36958d46c79df05e68e12df289df3c703064630f3d`  
		Last Modified: Wed, 30 Apr 2025 06:52:16 GMT  
		Size: 10.3 MB (10267969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62f48c3eccddd88df8363d25a9601007b17a3138998a48dde9068ab286f24db`  
		Last Modified: Wed, 30 Apr 2025 06:52:15 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:50a4a1d62930d67e186dd9db7b8a2710dd9d7f83cabac75fedbc46471b49e736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339467020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6935aa702628b5313b8f96a93db3a3a70649a11476eb3a0d136d21819b5aea7b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
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
	-	`sha256:b2978ba8c54b38937837ec33f24f1f728220997db133f61911da08567a04e3f7`  
		Last Modified: Tue, 29 Apr 2025 00:14:49 GMT  
		Size: 87.4 MB (87426396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42eb229ffaec8bb2d4ae5f6af15344b1b77eb404d2dcc67eaa5dd80ff2f2957`  
		Last Modified: Mon, 28 Apr 2025 18:23:36 GMT  
		Size: 125.0 MB (125042685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039899b90cc4498831059d9beb94071f67547f5eb20e0974ccb7b83ccc17fcd9`  
		Last Modified: Tue, 29 Apr 2025 00:14:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:842f846a39b18d5e19ff0d575435b18a468650667ddbc90dd44d734a02c95fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa1fa6862fec0837a2c2194cd2648011911552d3f70f439b0ba8bf92a045518`

```dockerfile
```

-	Layers:
	-	`sha256:1a2517a04c90a5c6e1da1b2da78b9825e91602d89d6241c935df522c6d6514db`  
		Last Modified: Tue, 29 Apr 2025 00:14:47 GMT  
		Size: 10.3 MB (10256188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e8edef7e02a0d5d2554232003c4652489c5e80f2739f9566955ff89c89644f`  
		Last Modified: Tue, 29 Apr 2025 00:14:46 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
