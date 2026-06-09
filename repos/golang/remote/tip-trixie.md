## `golang:tip-trixie`

```console
$ docker pull golang@sha256:3ee99a95e7e870e99d65ba9a9b496de5a65e13ad2d3e8a09c81210e440a8e96f
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:2369c3e343b715fdc595fcb64b54bc0fe75865c69f91f58277a8eb9925d8b36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.0 MB (347011029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607b41f5c4da0e4e845218031a6aa795f8b9049687db68d524674fc3827483f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 22:44:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:46:11 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:46:11 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:46:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:46:11 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:46:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:46:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7725aa85eabfa6f6975111b36ad49b7b5e6b8f64d0f45995ae488d359db09245`  
		Last Modified: Mon, 08 Jun 2026 22:46:42 GMT  
		Size: 102.2 MB (102236231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9caf2b5917603f564e8b31c080871596acbc699caf5fd0fec4940c836746ec3`  
		Last Modified: Mon, 08 Jun 2026 22:46:13 GMT  
		Size: 102.1 MB (102052370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643e7f81e8d4deb76226a16aa6ac1584edd1de438264a5b22c20f2060fb1c036`  
		Last Modified: Mon, 08 Jun 2026 22:46:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:74a1c0ae01df847409a6f182c642d880326fa421126f3d86584a096cd04413f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353ab52025c626e0639e1fcb685057ad70cb5fd14cb452016e8ed320186d3200`

```dockerfile
```

-	Layers:
	-	`sha256:5f6f2d258e8dcd3b2f632cd3700400cfd01b95e91538fa2298a5f04ad4da1657`  
		Last Modified: Mon, 08 Jun 2026 22:46:40 GMT  
		Size: 10.8 MB (10785863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5d8fbb1a541497cf2c8b20be9eabf3352d3c3e7375b9751831464a190bc33f`  
		Last Modified: Mon, 08 Jun 2026 22:46:39 GMT  
		Size: 29.0 KB (28972 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:51b040c5f681c8641a5c738f083f877b9226fdd25733858572fb259687e075be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302734144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57e344e3c03dbcdee6283929f42fb713dcc9a6d523e130cad313ec286deb1ae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 22:45:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:48:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:48:21 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:48:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:48:21 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:48:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:48:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203c225dd8522bdd8715f76203677e263257613c0c04e14fd9a434bee887dba`  
		Last Modified: Wed, 20 May 2026 00:04:36 GMT  
		Size: 23.6 MB (23639255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ada0eefe1ba158f90c1cefb9bda61c8de2e55c4f9c92965b87f7151a892d`  
		Last Modified: Wed, 20 May 2026 01:34:53 GMT  
		Size: 62.7 MB (62740413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7398a827b5bfff4d35191143ec061c5e5589e30c6634bad578e7ce484d831df7`  
		Last Modified: Mon, 08 Jun 2026 22:48:50 GMT  
		Size: 72.9 MB (72877251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017a74f67fe3bf0e9dc5d0c334ab5929b4a454a86c2f391ecc6e1d3f6697e53`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 97.7 MB (97735035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca08009aae72ef892f399b869d22433e48fb029cb50cb977e6708e928e7b9f1b`  
		Last Modified: Mon, 08 Jun 2026 22:48:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e105085715762c164f6b84c07aab994fa26d00474f14422500e57023c5cd8811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591d23aa41ee00ef219edc0334f1d857ad6fab310724b9a04a4d071917e5cc3f`

```dockerfile
```

-	Layers:
	-	`sha256:2b712d56311357749d05e689f75b97d0d436340dee73402ac94e330bde86b180`  
		Last Modified: Mon, 08 Jun 2026 22:48:48 GMT  
		Size: 10.6 MB (10581750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44769c4edb3e2a3bcd75b8381b0b4ea839a21fe1a1586305d1ee11a3a2e07fb8`  
		Last Modified: Mon, 08 Jun 2026 22:48:47 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4cb59d2a13efbaebaece4f863ddc16838b9ccc25d8df0fc48e3c86afc1445cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337140607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696d954eb8ecb47eb3aa887a8ee384c7b9a98c120fa33ab26e093908d77d7c91`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 22:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:46:15 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:46:15 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:46:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:46:15 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:46:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:46:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e09ae9f11907442ba90fe6c8cf6912969f3686792492a97dc21a8301281674f`  
		Last Modified: Mon, 08 Jun 2026 22:46:45 GMT  
		Size: 98.4 MB (98380357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2308f1cb629a8c8fe52b3b591bdcfb51ba3716d584492ccac8858ffd19fbe4d4`  
		Last Modified: Mon, 08 Jun 2026 22:46:27 GMT  
		Size: 96.5 MB (96469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167e0af29f4a62e36790e1c787a7da0c03c600e0effe61161459ccb73490bc4`  
		Last Modified: Mon, 08 Jun 2026 22:46:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d070bcb1058337bfa082189c477cb7ac7e927325818e94d48a4c29b349cfe112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb5c5bb78033a299c7d5f33e5f018d0376a9ecf286e74ea5645aadc7738c111`

```dockerfile
```

-	Layers:
	-	`sha256:8b4a81e2b357e6271f5be6c500cabc464778b8d79c5471101f7a447826624af3`  
		Last Modified: Mon, 08 Jun 2026 22:46:43 GMT  
		Size: 10.9 MB (10905681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b145abc1ffcae696c556904400f6c858b9d4d2b25af6d0ad2b4c4b62b88970`  
		Last Modified: Mon, 08 Jun 2026 22:46:42 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:52c3c29fb2e81290fbe45334c1fa6f018dba37ab21192cc7e67956bf3243a5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347902750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8446f2940e40a931ebffc7ccb2481e24e0cfe5263217b7a5e42008a7182d2b1d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 22:45:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:47:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:47:14 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:47:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:47:14 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:47:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:47:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7297938c03ac6ad4e53525c3e0002337292340d300a5508ffbc391176c4868ac`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 26.8 MB (26795141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6db995dae312f4650e9596da7587e265fd6b48ac92ee4cf787e012233b3a9a`  
		Last Modified: Wed, 20 May 2026 02:45:55 GMT  
		Size: 69.8 MB (69824667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450100fea4aa47e2907316efebe678bc77647667c0e2e71dcb906e38c425f577`  
		Last Modified: Mon, 08 Jun 2026 22:47:44 GMT  
		Size: 100.7 MB (100675221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c856874e83d87ce8611744942560effd5d1e879f3a49a6259f9e0f789a54f9b`  
		Last Modified: Mon, 08 Jun 2026 22:47:42 GMT  
		Size: 99.8 MB (99778009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f3fbbd41eef4dadd32a3493eaa207f4fa7720ee7b918dabe9d87642836eeca`  
		Last Modified: Mon, 08 Jun 2026 22:47:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6260ea973072c636d9a42c73a7fba4fbb03eb07fbd6f346932af6726a052225a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d820bdf554a9e3883cbb74da7cfc71127a3291be356f6ad2194229713aab3d42`

```dockerfile
```

-	Layers:
	-	`sha256:6233abdfe1bc8c7eda87a364e663036f415054afec330f2054dab0ad7b03bdde`  
		Last Modified: Mon, 08 Jun 2026 22:47:40 GMT  
		Size: 10.8 MB (10757126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1093bca2358641f2929005f32bfd8cd298a9afac3afbfdba74df04e7fc402c`  
		Last Modified: Mon, 08 Jun 2026 22:47:39 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:6e139ac231a4409074f21a374eb340e9e0cf843dd036347abc10c07919108103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344564825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a135390aa2bf5fe0dfadbf807f022187d9343c28644239f119b90cae13cd7769`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:42:23 GMT
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
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396fcf223bd659e5dda1b961ab403e3df6f9d118708751addc02badc2015799`  
		Last Modified: Wed, 20 May 2026 06:53:00 GMT  
		Size: 73.0 MB (73042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ca70e542a2f090e02cf1f610dbd33362e2bd92c8b359416ee87a47168f5d0b`  
		Last Modified: Tue, 02 Jun 2026 16:43:27 GMT  
		Size: 92.9 MB (92941610 bytes)  
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

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ee447f23252520d54e2f552aad2193add538009638ac869c584a04da20a00d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05611365397fd46577b242a42334a60b1d8ad75d7552f578d84b140caef38334`

```dockerfile
```

-	Layers:
	-	`sha256:cbcd24863a961868d3e228a08d482ffc326a5d4047a6458a481451b856c38b06`  
		Last Modified: Mon, 08 Jun 2026 23:07:13 GMT  
		Size: 10.8 MB (10781651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601c935c750f7576a83d3d7e77fc9be3a036194be4fb1cd348b615746440e591`  
		Last Modified: Mon, 08 Jun 2026 23:07:12 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:4e76f9bdf1f66b4689d536d1b2ba341214b2a8f5d2beaf4d1fe5beb460466660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.5 MB (370502562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d375018e2a5695e6690c8c1c338bd923b72fd0051d155d6e57737e6de578df5d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 23 May 2026 06:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 24 May 2026 16:39:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jun 2026 06:45:18 GMT
ENV GOPATH=/go
# Tue, 09 Jun 2026 06:45:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 06:45:18 GMT
COPY /target/ / # buildkit
# Tue, 09 Jun 2026 06:45:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Jun 2026 06:45:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6afb0d9fe2fdfebacf2ccb9782fd129d9e416f637c13f72c2f0427e69c04c88`  
		Last Modified: Tue, 19 May 2026 23:49:54 GMT  
		Size: 47.8 MB (47796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db76586e2d1a29e7feb120e0fcc7fa49e8df54823efd2e1b4e13ca0fe4ab60d`  
		Last Modified: Thu, 21 May 2026 14:02:51 GMT  
		Size: 25.0 MB (24966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bfe91065712f707f8614b6bb5478bb453a0332b440e47735c29ab8e1ac33e`  
		Last Modified: Sat, 23 May 2026 06:51:24 GMT  
		Size: 66.7 MB (66673209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398a312ecba685f463e19d1da6c4ef550fa865a7e4e10e59224662d013f3fc84`  
		Last Modified: Sun, 24 May 2026 16:47:40 GMT  
		Size: 131.7 MB (131719359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5a55eb95001de7bce5a945456836deb24c4f6ef91e17b9ea69478ba20a16a6`  
		Last Modified: Tue, 09 Jun 2026 06:52:30 GMT  
		Size: 99.3 MB (99347186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122d3bfd97f8064bca11f84445e6813249e663e61cb2d4e5fe6341f2263455af`  
		Last Modified: Tue, 09 Jun 2026 06:52:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c46d3a135fae53c9f6ead6f5541d276318252e5326818d5028a4981cd17bf09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5314529577138f01d9b925457100aaf3b5550743af0f538b7bc0b51b14f46992`

```dockerfile
```

-	Layers:
	-	`sha256:62e1b1cd605436ce2a089ddc3419bb2568bb7039b248ad7b2866c90c0135af49`  
		Last Modified: Tue, 09 Jun 2026 06:52:17 GMT  
		Size: 10.9 MB (10855484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667854db8cf7ad56e5cac6d775f4fc2ab5117158759f5c83247c98353c0d7357`  
		Last Modified: Tue, 09 Jun 2026 06:52:13 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:13e8be382d6264254263f3aaff254dfe9b78b78997fce48e1517ebde58cfb620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321363591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de15ba30cf226c2db90b1d86db5f3147cec36c8c6ac71f8e778af6a4fe830ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:52:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:52:41 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:52:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:52:41 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:52:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:52:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a95ac44f164c9c275ab328d3f5219a9cee0e2be081ed2ce1bb7cb8135bd49f`  
		Last Modified: Wed, 20 May 2026 00:19:10 GMT  
		Size: 26.8 MB (26804813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab366c3de62691a29444d50ed3d26e9d7524b8314a9b46521cbec555e978032`  
		Last Modified: Wed, 20 May 2026 02:06:37 GMT  
		Size: 68.6 MB (68638051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd22048fba1465d35621d768bcd327fddf66960714d773f1e88209e32b1e38c`  
		Last Modified: Tue, 02 Jun 2026 16:42:51 GMT  
		Size: 76.0 MB (76049556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56217687aa3cc648280b9c7052cd68f26077339d92dab45c68b721ed5388981`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 100.5 MB (100491232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905755a093489ba4e028d96f97d08a1513b5935413269c114ebf8e980436bf0e`  
		Last Modified: Mon, 08 Jun 2026 22:53:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:93474fd728c96fb07fb2bf8608aaeb0a08c412b116c20b394fbf6e83031acf1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743548ec5c274d9bde2b713365077ee792a2e9d2eb69c849e0672632db152c8e`

```dockerfile
```

-	Layers:
	-	`sha256:e749f60843c4eae91b9fae633a811850934aacde510b0ffb4cc1543b68355a3d`  
		Last Modified: Mon, 08 Jun 2026 22:53:15 GMT  
		Size: 10.6 MB (10597011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0372b0747d32a456f7512c5b41b7d40adb53ef4d24a90aa6e41a8ca4849d3fd`  
		Last Modified: Mon, 08 Jun 2026 22:53:15 GMT  
		Size: 28.8 KB (28794 bytes)  
		MIME: application/vnd.in-toto+json
