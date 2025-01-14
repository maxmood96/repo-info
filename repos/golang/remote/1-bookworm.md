## `golang:1-bookworm`

```console
$ docker pull golang@sha256:4a222c0c58da863e2e19328d3f15adbed2603b94068a6050dac5161a1e9cd8b4
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
$ docker pull golang@sha256:ccdca3b3bde3bfee2518a087b467f2b452fad9ba3e378d3c1578db494c8cb13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303310601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bfd58a2b2f6f482b58cdaf1c2ed75daa4051e6c1e1d33c5241bc8ac62f0347`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 02:32:44 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941421258b3c3deeecbab281e8e1836075180e4878a3512c5a71f0a7fe7ecd57`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 92.3 MB (92325709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a103a99567f138de13ccae12dfd5f1ff5dc696ceb7a9105ef4d10e2d839e2f89`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2ed556caeb47f0237b761ed1c91da641ae2fe25cec96901c3b4371d6510d83f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10306951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ecb05001b82a7a49d537e94a7726c40e8b7256a5078d45d17007d2aede5b1d`

```dockerfile
```

-	Layers:
	-	`sha256:b0e1f88ea6d9baa681d56412adf5dfb719e36850f70787a0410c21f8e9e07d32`  
		Last Modified: Tue, 14 Jan 2025 04:16:36 GMT  
		Size: 10.3 MB (10279306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418c667e89176accaad14217132a601968fafd6b7a79076a4cb409ff35485662`  
		Last Modified: Tue, 14 Jan 2025 04:16:35 GMT  
		Size: 27.6 KB (27645 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:e5c1bdcc5826d123e09031b167f0fd4927f64d00489acc029b3b2a3b28f6932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (263971429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f31e410dba82b15c38a44b71da93cf6c8cd554cbfa11f83215d19f45467bba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d13f1db6dbfd0088e8031b3d81dfa082bdcf5c4b98bb6406447ce39e0a33588`  
		Last Modified: Wed, 25 Dec 2024 21:18:30 GMT  
		Size: 66.2 MB (66166658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec60510747e26b9a6cd19343f21f1b5c7296dfce5dc07f3f5b68066457d253b`  
		Last Modified: Wed, 25 Dec 2024 15:56:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8294c1fab93cd38cbf3f3f2aeea5759716ae2fd0d7651143b103032f56412c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10115425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dd7378dee248d4465bcc4c86979bbd9421c3e104526a4d87159b258207f03c`

```dockerfile
```

-	Layers:
	-	`sha256:369eb31cedbfd418af230d9b45dcf1cc7bb86ab7f224526c5d33e3044d4dcf00`  
		Last Modified: Wed, 25 Dec 2024 15:56:18 GMT  
		Size: 10.1 MB (10087646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e721417f8b9203dd9b123547924de96a44572526e12e453a0d2658d983a4436`  
		Last Modified: Wed, 25 Dec 2024 21:18:35 GMT  
		Size: 27.8 KB (27779 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:98f66c0f9a34f98f31ceec0be5cdc77dd77eb7a050280b079462a0cfdc22b9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293096837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b811b0aa52884991c6d5944ea68fa43e84ab3083751b07f04a10bb19bf6514`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f0760d52ed73adddb3508ddcb5b6593cb64ca56a1ff03102d680fcf2358d2d`  
		Last Modified: Wed, 25 Dec 2024 15:24:13 GMT  
		Size: 86.3 MB (86344558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3aad8f12f66060f1575c7562f8831493595038c34f14527da5ffae2ea0332e`  
		Last Modified: Wed, 25 Dec 2024 11:27:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:196f08ec480972fb0a93a0a7e1937bcbc16a204a18ad4a3b17d1fb9023a5132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10335011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4361b1814cd12ff8fc0da22c5419de37c010c7d8e20cadbd2d939e3fdf48f80c`

```dockerfile
```

-	Layers:
	-	`sha256:d47ea32bd1cb45c9e5e39bf504202d6a16b7a01169f29fa1d08c56d7f90ddd1e`  
		Last Modified: Wed, 25 Dec 2024 11:27:17 GMT  
		Size: 10.3 MB (10307183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5876e03af24adb7d1985ce97f77e663bbf7e6213ec0a42315d065b5e00aef29d`  
		Last Modified: Wed, 25 Dec 2024 11:27:17 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:49ab3ae9b2553ad0398193406da024486803033b73ae47f6d95d067b3390df69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302229714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3955f74426019809214bf44e5531dc8abdddca03d422bda99850c61211a1f8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 03:18:00 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf22217c3e84cad5a62591ea73a73e4b93283f4807f7e3532ffdb2931f49a3f`  
		Last Modified: Tue, 14 Jan 2025 04:16:45 GMT  
		Size: 89.7 MB (89726832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ee978a239d9a54a2ed89c291f3c5c0ee5f67c1dc8c9ff24b239116398d826`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 71.9 MB (71913121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20249b245589493f03ed997a1a515316cffb7a68309c38de24dd877f17c94ea`  
		Last Modified: Tue, 14 Jan 2025 04:16:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3222822a275dbc9ce2210be65b09f53180e523114e37df00f2985086a9cb02b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10286951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d02db4c7d64c73d10ad47888f3fa2377debdb909c2c3a20088c8838acc8fd52`

```dockerfile
```

-	Layers:
	-	`sha256:6f512d728c2a67d38c6e5aa40df1d9f796bddf03a3c8248779a298d0052efcec`  
		Last Modified: Tue, 14 Jan 2025 04:16:43 GMT  
		Size: 10.3 MB (10259361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74a3454d2338454f5662971f2519be4c2280ab5d9830edcf68d3a550e480bbe`  
		Last Modified: Tue, 14 Jan 2025 04:16:43 GMT  
		Size: 27.6 KB (27590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:6c17b19eeaece765e9326ef3470cb63c3bc5a1e2639040793eeddf7a41a41f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273709435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d425142b622ee01c8c0a4bc47364f6d352f8714bbab3b0af9acc3e30a306e0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce254d10016582282d02d849a1fd4f7ae3009b347bb00698189b72412df1a3`  
		Last Modified: Thu, 26 Dec 2024 01:07:45 GMT  
		Size: 69.9 MB (69882841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b544eb792289f36300c86a5b8384bf187390efc35d3ccdca9105fbca1a4630`  
		Last Modified: Wed, 04 Dec 2024 05:01:52 GMT  
		Size: 68.3 MB (68313685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1523ad0f09a3fb0f35d784af9329e229abed3f954971ed41f19dae7eb139cb1`  
		Last Modified: Thu, 26 Dec 2024 01:10:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1719b551f4ee0295bc9b40330c87ae601f08202a34089dd96a4defceb859ecb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f368ad282e1d2afc464548b58d3ede81fcbac0f63574a7f00397ccee7711b7`

```dockerfile
```

-	Layers:
	-	`sha256:5e55270f3a5b141fa9af12d293c87eeb7996b0033a0ee5014df868de29b0cf89`  
		Last Modified: Thu, 26 Dec 2024 03:32:04 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:959687539d9ed5e1a7d98f130c1bc321fb5557db2bd67711d9deff20c1aa41f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.0 MB (309035449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd243fff8d1a73de2546529b6777a79971efa043a3f2b3791e95e6cbf127ae5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 01:36:59 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c03af048a442cc8e051bc902b70c30f75e83952993dac48094c108d53fb99bd`  
		Last Modified: Tue, 14 Jan 2025 13:10:22 GMT  
		Size: 90.3 MB (90320681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91a259a07865746288d1b28127693b3ba2bb41a4fc212519c1e4889645b084`  
		Last Modified: Tue, 14 Jan 2025 13:11:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4c8177118decfe502e3d13472c2270b676f933aad6e97c5b674b45c3e2e9b28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b99e32fd3a40a19c090b06fcec884b639abba07ef716046da7d977fee53d48`

```dockerfile
```

-	Layers:
	-	`sha256:73f56ca09b32ce7a9158e46a99590989fc1fe3337e4cd2d98cf0ebab79618516`  
		Last Modified: Tue, 14 Jan 2025 13:11:56 GMT  
		Size: 10.3 MB (10252025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cdbafad37195c407589e71e56f874fd04b23d16d8582a69858ccb22f0f9f2e2`  
		Last Modified: Tue, 14 Jan 2025 13:11:55 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:7b46d5cdcc6a2e30ce4729ceb5c45b9b7fe78b045e06e9b74dc9bc6f8afcba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276565195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edd0bf6555a16df4cf5633e4d1d5418fd39684ed29cdb064f9d5f0c807a0d89`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 01:34:07 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 04:59:37 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01efc275df65925eac4d0751075d4662dbb1f25949df2abd249bd7ca26b4c480`  
		Last Modified: Tue, 14 Jan 2025 11:21:34 GMT  
		Size: 68.9 MB (68907405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0e887134b9df5e925b11e26e955f40d06b1fed9dcce6e4444b3086a2f79c9`  
		Last Modified: Tue, 14 Jan 2025 11:22:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c912f5fcc0604f025e2fd92f7beb75f1c383638049e9a0394b46364def15aa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10142932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8847f6fed2bf746536ade66190d0e4cc537d07023345f6b0fe17adf3a77cf30f`

```dockerfile
```

-	Layers:
	-	`sha256:90c90e6c94c0cb410e8d30e6a95ec093b4b09ec17906cdf36130a1e529d25c38`  
		Last Modified: Tue, 14 Jan 2025 11:22:49 GMT  
		Size: 10.1 MB (10115286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d3389abed43438774d9462216654b87c6f9df84542fa9390f3412a24de192d`  
		Last Modified: Tue, 14 Jan 2025 11:22:49 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json
