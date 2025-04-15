## `golang:tip`

```console
$ docker pull golang@sha256:eff3ef8b3fe21ff499ae6e6a8fc832731b348cf35783b8fd8df0b4ddf1c4f44d
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:1af17f66a25a02d82b53bc9edf13fc243add6a90f82a4519dd633487fff41d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355306960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88034c6f7bdaf9bf8072a4f4abbd497e3a36199c03b14f0c524d27601ef3dea4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b2962fac15503e8352335fba0f64b1324263e3550c9bcd812f221960cec0c4`  
		Last Modified: Mon, 14 Apr 2025 21:51:26 GMT  
		Size: 92.3 MB (92331625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013504ab5187d636f1901fcb4a6eeb2b2ad7ca1cea03792606973678944bf0e4`  
		Last Modified: Mon, 14 Apr 2025 21:51:15 GMT  
		Size: 126.1 MB (126077078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db8cb71570f2762499004fcf3cf974fe6f066664fbacc07d34edf28699a9c14`  
		Last Modified: Mon, 14 Apr 2025 21:51:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:cf94d0cdbd816dd08fb5e23c92eca6c39bb9d99a37a751019fb6a81d688aa822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4624847a30a85b248de8a1d4a611f90d0e9d4dc4b0a2dc2f7a58201495455b9d`

```dockerfile
```

-	Layers:
	-	`sha256:8ee45753a0b78dc615a22d5e1a88c8381c5eb05cfb4d6bece756fddf17be2057`  
		Last Modified: Mon, 14 Apr 2025 21:51:25 GMT  
		Size: 10.3 MB (10271868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ecd5ed96ee733cbeffbcba29b741275e5659fe72eeff22dc736a369e7653ce`  
		Last Modified: Mon, 14 Apr 2025 21:51:25 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:2b1a8ddc5a7fa4b5b8cd98364d0e630bb0b66bcfcd470882bd6237ea3ee01fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313060156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffff45d2601e554a3e3209369ad1bc3153732ba9dcf51a542707dcb221f6b1a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a9e8df2c13231c1e0a205f7e3ac9fa85454d09e0c0e5c18afbd185b211ea`  
		Last Modified: Tue, 08 Apr 2025 20:42:26 GMT  
		Size: 66.2 MB (66197481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131e20eff5d97e9796f801f5335249fcb3b27557a67cdb1b0533cbc32974fff`  
		Last Modified: Mon, 14 Apr 2025 21:52:15 GMT  
		Size: 121.1 MB (121108078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea719ed4b4186c6ca36e4f05988487816bec1deaa276fd3f91061ed29b7ca34`  
		Last Modified: Mon, 14 Apr 2025 21:52:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:34969697e2ff357fd6433c019dcfd544fd568f3517680a7edbb3fd25d0710cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10107976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a138280a3b04dd3cbac364ab60b369b98675a52c1d03bb66b04960562a9a6a`

```dockerfile
```

-	Layers:
	-	`sha256:06327fb12099724b80c4f8596b08cfa9af8d5bb97ec2ff9779e2b292780b661a`  
		Last Modified: Mon, 14 Apr 2025 21:52:15 GMT  
		Size: 10.1 MB (10080190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597d17457c3806e50f2875e639b938905457572392c9d2a729195a26c1ee773`  
		Last Modified: Mon, 14 Apr 2025 21:52:11 GMT  
		Size: 27.8 KB (27786 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3a3da1e6bd6f8004a6fc6212de6180b84fa5a8a8701b9edc8b104812e65a5800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341394557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7f7be87bcc9856a78066a2dc001307d74d51de13f44a2e7463883c565fee9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72691c55039fb058e42d1e7433c859beeeeaa9e1b1856b791ba59bd1bc0586`  
		Last Modified: Mon, 14 Apr 2025 21:49:56 GMT  
		Size: 86.4 MB (86397123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b206f4f1851ae209ce8b8172ce5c71a21bf857b5a5fc8341f94dabec27aaed`  
		Last Modified: Mon, 14 Apr 2025 21:49:56 GMT  
		Size: 118.8 MB (118769688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcff756ccf44280a2e96732072b375bc4c4f78ff4c70cddb814fca383a07be32`  
		Last Modified: Mon, 14 Apr 2025 21:49:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:7639b65473dd26caa1d93269fa7f3572be84533c2cc355312dcd57b3d37c4d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f9a3be5f52f137d2e603adab4aac467ce8165f684c05d8e943cd4fdb0c5285`

```dockerfile
```

-	Layers:
	-	`sha256:6ee3ea3ec0926d8b3d9b22f21a7f3032356f59825f40d309cf89c4f6fe51a764`  
		Last Modified: Mon, 14 Apr 2025 21:49:53 GMT  
		Size: 10.3 MB (10299715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29c2fd50290470f18aef73b890f6d296bbc264a120942a5fab37a29d39ec0d2`  
		Last Modified: Mon, 14 Apr 2025 21:49:53 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:262ddb201957f1185f972b039d076337291b4f106ce47c75d8a3c9f09bf0e032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354568531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7133de51a57770cd1bd37120bdcba6ddfe7ee33eb0334a3ad7632fe90e4911`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a372e36842cab873ede07e00a5b1bc6b604633fa4c93b226f06ed801ae89c105`  
		Last Modified: Mon, 14 Apr 2025 21:52:03 GMT  
		Size: 89.8 MB (89755613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a1236535bef233193363d469e87ef11dfa5b282a53e3685fad2f41147bdd6d`  
		Last Modified: Mon, 14 Apr 2025 21:51:51 GMT  
		Size: 124.3 MB (124250003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd0b5922ef96dbfa59df37719d1eb6ec7d3a4462c9b4a1933d401506dea8d0`  
		Last Modified: Mon, 14 Apr 2025 21:52:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:5f47bc07127a86e3ce65f91e012dac4d00aa053df2b51cf759d5dcf2454f5014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee68c9e704d36a0a167742d581c991caf2d1aa7de1de2102f9a708d0f9e02e9`

```dockerfile
```

-	Layers:
	-	`sha256:c70be9159139f8e3af61d1f2826da0aec85f6e63ce47c99b732d4946983385e5`  
		Last Modified: Mon, 14 Apr 2025 21:52:01 GMT  
		Size: 10.3 MB (10251942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3692df1bc4343e5ef6493eefe4274f986bf5dc843c7e85d46981d2ee1720e44c`  
		Last Modified: Mon, 14 Apr 2025 21:52:00 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:cd70a4f5432b45d5a007da1575cd39fa4e9b7488174d073462ccac4b83056c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321978110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378b7bacec50cb8f9ccdd5502d7cd2d7e04a0528db4ee16a03c59f4ddbeb6843`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Apr 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 07 Apr 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Apr 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Apr 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f5e7682657f9515783d77fb7efbdd12ea81bbe4c750080727193e5396dfa344f`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 48.8 MB (48774861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca83e3505dc809d18860248927308a5c27c298583b9da5817d702111bdd65622`  
		Last Modified: Tue, 08 Apr 2025 16:31:05 GMT  
		Size: 23.6 MB (23595612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89ecdcc124054ab515f88e8a0bc5260e578fb23450a3ca215363db6cf689231`  
		Last Modified: Wed, 09 Apr 2025 00:38:14 GMT  
		Size: 63.3 MB (63308311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67fb97ca2e19f9a62b9988d33fd9b65b01ccb5cc564c412de1d8c73ed7b28fc`  
		Last Modified: Wed, 09 Apr 2025 08:20:47 GMT  
		Size: 69.9 MB (69916439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217715ff223da784f1dfef1ab407185f2f404c6c9eafd7fec335ed813e934ce2`  
		Last Modified: Mon, 07 Apr 2025 22:59:57 GMT  
		Size: 116.4 MB (116382730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0806d0fb0f53fced45d6892b0272fa708faa99447d149d207b8e941dc6d72a90`  
		Last Modified: Wed, 09 Apr 2025 15:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b667f964c3a1dcfe2120e6d11094f365977d3fc8ccaa7d64a4fbc604757a4c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aac67113fe2f93a1b685eda050be86e14a432593d14d674d5b3310f337b999`

```dockerfile
```

-	Layers:
	-	`sha256:a6e2755416439ef55b9f3a3c538a0d7e66a283a9eab577d75e0eb1ee4e8324a3`  
		Last Modified: Wed, 09 Apr 2025 15:19:00 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:16f61633807aab36e65684efc16155af7163c01237f52166b9646f735efaa4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359083924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e9606e29735565f33e6b7c5cf36c9e39a6dde9c9f90914a2d12ffe0b6bb465`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ab73478cfc6c2c81f66fffabb6adb3536b4880f0b0cb959b34167c62eb4cc2`  
		Last Modified: Mon, 14 Apr 2025 21:52:04 GMT  
		Size: 90.4 MB (90350288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394c4e947a61e9f0edca853e080387bc94a62b435ba7141bd2b21c9acb3149`  
		Last Modified: Mon, 14 Apr 2025 21:52:05 GMT  
		Size: 120.9 MB (120907733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d0e5f547256a0e1129376d1950ea996ea349ef3d538b9e48c42d4195e3242`  
		Last Modified: Mon, 14 Apr 2025 21:52:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:ddfb647a84a8e79501d5fb2cecd8d477e56e1d8a6a6362784e2e5d4e47ed5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10272281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c18b7faafa919147c8cbd5097d93e6ceb21286cd8e4fa546a072e56cb805df`

```dockerfile
```

-	Layers:
	-	`sha256:9ed35b749678c154a0a6de3cd2c64ef64d0879c6e14bfaaaad17bd0a722e1f83`  
		Last Modified: Mon, 14 Apr 2025 21:52:01 GMT  
		Size: 10.2 MB (10244561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a70dc6eed77d592dc292f185049740e43ab129b93f9d46cba9ddd96633b8f0b5`  
		Last Modified: Mon, 14 Apr 2025 21:52:00 GMT  
		Size: 27.7 KB (27720 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:cf1c6d237c0394c4b32c6fb17e0752ce28e55625ae57bb1da0fc503e416aaacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326925056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4759be9734a66713278425c5085db314c0650977f3a0d8bbce83248d592102f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac9900eeeae74e6b991013801dd4b548da42e9a24a8a017f2f933bdd60bd62`  
		Last Modified: Mon, 14 Apr 2025 21:52:33 GMT  
		Size: 68.9 MB (68936844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3413729307d44114afade63be5a02a91d2719dffc8bdec785d42f725815b7f`  
		Last Modified: Mon, 14 Apr 2025 21:52:34 GMT  
		Size: 123.3 MB (123330348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf98db1172c6ae242a02d961c9ebb33bfac64d2bfea72f9e62cced6e61afb5a`  
		Last Modified: Mon, 14 Apr 2025 21:52:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4da58b105f1246be2ca739298706cc549a1b4f2d42c39cb7cfdd30725fb39dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824933b761f5a277263aed4105a78de250dca38693f9ef046e05ce7861b8339c`

```dockerfile
```

-	Layers:
	-	`sha256:c8956245ba3507af28834c83d36957e2baebf4c0ccf9c01dcb7e2935f92ebd91`  
		Last Modified: Mon, 14 Apr 2025 21:52:31 GMT  
		Size: 10.1 MB (10107848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b148d84604de40e148e9c87971bd56536a057086f3a70b84d262d9a9253084`  
		Last Modified: Mon, 14 Apr 2025 21:52:31 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
