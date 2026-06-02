## `golang:tip-trixie`

```console
$ docker pull golang@sha256:ecfe11cf52a7de3e62a8af10b961acb1215f7b9ee679d4f94593ce40a6a9dedc
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
$ docker pull golang@sha256:e5e88f1aa8ec4c41214106c9a588aef960dc9947d87441e67d563dec5e1ae447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.0 MB (346961178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e51408e0becf1f8ad72f034108fbac63b28fe5c26daf615d760f05ea58af5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:39:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:40:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:40:54 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:40:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:40:54 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:40:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:40:57 GMT
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
	-	`sha256:7ea8097a0851968236b50688f5b6420b3c18bada4489aabd0db540217578bae2`  
		Last Modified: Tue, 02 Jun 2026 16:41:23 GMT  
		Size: 102.2 MB (102236588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f29da6194068cf9bcb9d5261ce3db2ba9613e69bf068059cae42650df5c10`  
		Last Modified: Tue, 02 Jun 2026 16:41:24 GMT  
		Size: 102.0 MB (102002162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f56006f779e38be38096a3ba9e50e91ce27e6983de5521b6552e6a31fe4c2`  
		Last Modified: Tue, 02 Jun 2026 16:41:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:50f952d7f4656a0b73b3e337964f9ce5f498217145e726608d194abdf133d756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71182664dfaadec0ca6a61dbc21fed5875918a9f8dd035fb41cbaca3f86f11d7`

```dockerfile
```

-	Layers:
	-	`sha256:bef20b92b70404c9de33f552000425c4a4ac19aad6c9d836f3d0d42af73ab6c4`  
		Last Modified: Tue, 02 Jun 2026 16:41:20 GMT  
		Size: 10.8 MB (10785863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ceda8b94279dc7eb8c6a1a977fd21ba30d068905ec480b15f3aa4f795c94edd`  
		Last Modified: Tue, 02 Jun 2026 16:41:19 GMT  
		Size: 29.0 KB (28973 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:5f2d018db44870fb806730059e3102e62a4c8ff6456a46fb547804e4f8996a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302713052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1633548ac8899083d7b9d147a926e96c3a499c6d5c65ad5794aa963798dd4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:38:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:37 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:37 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:41:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:41:40 GMT
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
	-	`sha256:8dcbadaa4042ce8c47946f5d9c9fd419d68201ee1a8d529aac058841f195484f`  
		Last Modified: Tue, 02 Jun 2026 16:42:06 GMT  
		Size: 72.9 MB (72876140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c820ebe5b5536b95e87912c5dc1f2663a3e9f184b88c7a174fffa610cef8238c`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 97.7 MB (97715056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d5439770ef257779cc1851c60f5cdbe605956b532f8c9857bb9730e16e8d4a`  
		Last Modified: Tue, 02 Jun 2026 16:42:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:71517079959fa047253473110f8bc9a03fbfb9ba9ef3c86f88612c6e1e7ed0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104f55dc8b50610aa28d22e879769ae7ce6211f572f0122cbe62b050b03b77c6`

```dockerfile
```

-	Layers:
	-	`sha256:811e7a24611af74724d509ed708190b275a69502b48b67c87743b4a0942ed179`  
		Last Modified: Tue, 02 Jun 2026 16:42:04 GMT  
		Size: 10.6 MB (10581750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc59fa100cccb8e9225fd2e9e5d7515534aed6ec16fc102c51778205a37f228`  
		Last Modified: Tue, 02 Jun 2026 16:42:03 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bedbe12bc2ad60f43481d01b8fe01909e5efefd97050066d199d4f7c9f6ac1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337105703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f4f98dc4f0bb46b77da53a86a95470eefdf209c224cc958503ee9e116d3aed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:39:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:40:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:40:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:40:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:40:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:41:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:41:01 GMT
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
	-	`sha256:fcf6b44f3edbf6a0438e1a104697a461f87ea6e755d452f237a54e5d5d7f29ef`  
		Last Modified: Tue, 02 Jun 2026 16:41:29 GMT  
		Size: 98.4 MB (98380288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ffb09d61853e3fb3628a4cb3b2d395b59e27aec015f8f1626a8b2ce9bb2f2`  
		Last Modified: Tue, 02 Jun 2026 16:41:30 GMT  
		Size: 96.4 MB (96434582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7383574b23d0df145a15f70383208c9efc335ac78039585c03a372d000a9d782`  
		Last Modified: Tue, 02 Jun 2026 16:41:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1a5d2386158ca63ddb28e60d5f8d6682fa7d08600fd0d49e6e55bc005b14a528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235815f1fc4bc447e607e7cb44d0e948362b8dbd55ed33d01e2c0671b09bf510`

```dockerfile
```

-	Layers:
	-	`sha256:bcd2c5ba43266c98f0914a05410ccbe85f29c90187ac0ae563107901eca42933`  
		Last Modified: Tue, 02 Jun 2026 16:41:26 GMT  
		Size: 10.9 MB (10905681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9309ae991293ee47c7424c5ccecc2c5e4fd155cb882d54fb9054b7bf0de8a40`  
		Last Modified: Tue, 02 Jun 2026 16:41:25 GMT  
		Size: 29.1 KB (29121 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:80030e36967dca41fc6a65fb534eb40a08a66e5a162472e522261c07ca711e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347894414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e55a8c9016d60964e5e173a8276cda017315cdcfad8c8264d306a9572153c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:39:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:00 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:03 GMT
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
	-	`sha256:aa0f663830b2867c34c1026090631f5e729061b57242ea8c0d6d40db4d251118`  
		Last Modified: Tue, 02 Jun 2026 16:42:33 GMT  
		Size: 100.7 MB (100675365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f630b89f59dc6a4b85d53c6ab2696f0b52ea5d937a0bd9344e6c06fc5883a6`  
		Last Modified: Tue, 02 Jun 2026 16:42:33 GMT  
		Size: 99.8 MB (99769529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29493c47819a5a702989839699df869ea06d12f0d72ef41fe0a8295cf9eb4768`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c82e913f5b02348755e750bb331a24e6e55ae3c743a4a4c94eab604341febd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ce4bea6ca80f8dd0f370cea0901534b391e27b3892d3dd237ee3592afdf041`

```dockerfile
```

-	Layers:
	-	`sha256:3cb8580f0cf99ca54bde58993fd95357326ed6daabc3e2220661591f2eab690b`  
		Last Modified: Tue, 02 Jun 2026 16:42:29 GMT  
		Size: 10.8 MB (10757126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fea6c1a1dc570f66af865bccfcf0f2f2ce62e4ed54f1693b3878d5c08ea1a359`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:ec698e9c4dc6681c5b948c3def8a64f09fef9766292cfbd2ff904fb60ace48e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344524649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9865c75a258d6932093d2db5d31fa0c9648b048cf868de73f0383baa22da1815`
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
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:27 GMT
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
	-	`sha256:a4a76d2265265ac98a5752cfbf5ed880207c013050351547f0c225cf8c995ca0`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 98.4 MB (98387092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86a2dc335689548be6519a9c0f348c85e335d8c5acd7538e40702e1a96fe71b`  
		Last Modified: Tue, 02 Jun 2026 16:43:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:29fc7f39825e3e8e1b12ca3d63917dd76d9ef82b66413c21ca520346a4f562db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d1f84c27a748f8135af83f83bf1c11d3d5a91444636e85a7966d1ce846aea4`

```dockerfile
```

-	Layers:
	-	`sha256:bc0d860103ac9222d3c0c2434c2715554b00ceff4dc605d6864997631cae8b54`  
		Last Modified: Tue, 02 Jun 2026 16:43:25 GMT  
		Size: 10.8 MB (10781651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b1df3fcb033f06200731e34d0396f1410076f90ac03e7ab00693d817797fa1`  
		Last Modified: Tue, 02 Jun 2026 16:43:25 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:a5765226cc0398b7ae2fe6a43280412f2755e77b9ad6094c1306788a0067cff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370317797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2865308c3656a07fb4059f82fef42c5e3f4c447124414d63fc9ce5b0994fbb`
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
# Thu, 28 May 2026 11:35:46 GMT
ENV GOTOOLCHAIN=local
# Thu, 28 May 2026 11:35:46 GMT
ENV GOPATH=/go
# Thu, 28 May 2026 11:35:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 11:35:46 GMT
COPY /target/ / # buildkit
# Thu, 28 May 2026 19:43:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 28 May 2026 19:43:52 GMT
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
	-	`sha256:f9ba57acf5ba3d18b7eb9e4286139141d4a6480c2e9b8f4fd881334e86e5e1a9`  
		Last Modified: Thu, 28 May 2026 11:39:26 GMT  
		Size: 99.2 MB (99162424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1fc8cdfa505e7fa7d43a4dd0054a53b45bb9982c4094222a929df866cffa0f`  
		Last Modified: Thu, 28 May 2026 19:48:46 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:78f47bfa84ca419c3ad7fbe76170a391e0a6b7e0c19413213d680c62a0d3a590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1152827c70c650a1640bc0a1f788eba5f21211413d58561232566378d9fd7085`

```dockerfile
```

-	Layers:
	-	`sha256:b963652f7cb6435997ea31fd51b1ae3e9cd3bf99db97ec5b40f1036826016213`  
		Last Modified: Thu, 28 May 2026 19:48:48 GMT  
		Size: 10.9 MB (10855484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4a5198d4e092c0a15349b87a6c386d88799ed7839fd80f088662bf4885f6b3`  
		Last Modified: Thu, 28 May 2026 19:48:46 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:903d8a59fbf05e59d2aaffffb8e0564e37ed50036ffd4eecdafebe531b5fbc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321326009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5601be627df4b7cecd1cace96d3b7ae1994b57a9fa9e81562baf7837bec329`
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
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:00 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:14 GMT
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
	-	`sha256:cca767cc33ca0e2036ed1bd1b9a5ecdd963a3598306969640db0e92025a10887`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 100.5 MB (100453651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a8ee68c14b98afb3a8774d01717f9336661c63fb41da7ee6c6eb661b8a1ec`  
		Last Modified: Tue, 02 Jun 2026 16:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c5bfcc6415eea398f496e1d3fc7d599ee9c086f47575d58f834eb40e1188cfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02ecaf05c2721cd8aa7f5a36fc6ce1fef9c38467cece8728a38683bdfa9e9c2`

```dockerfile
```

-	Layers:
	-	`sha256:335d161276e322727925e7bb548db11aecc16bdb41306ccf95c7249bd6a51b7a`  
		Last Modified: Tue, 02 Jun 2026 16:42:50 GMT  
		Size: 10.6 MB (10597011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb8eed158c503161fefea3cd222bc38c1c4fa30bc339cffea8e8d0d1094b14c`  
		Last Modified: Tue, 02 Jun 2026 16:42:50 GMT  
		Size: 28.8 KB (28794 bytes)  
		MIME: application/vnd.in-toto+json
