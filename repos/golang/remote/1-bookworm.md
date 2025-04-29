## `golang:1-bookworm`

```console
$ docker pull golang@sha256:a642a07319c67a15d52049a16acd16e1da85e735a7b4647f3da51aebe2a277d2
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
$ docker pull golang@sha256:b98466189ff3043ddffe0c26a13510c6e2971ca331c7cf1528a6a970407b47ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308188824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce9b6e0085fc5bf5e265eec5334562e1510b02b0398dc45d5bfea419c6c4f96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46f54697eb97b3e550e762b20a1596c1b90956cb126063b68e9ec4b6584fcfe`  
		Last Modified: Mon, 28 Apr 2025 23:12:00 GMT  
		Size: 92.3 MB (92349642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d296901bdc593d88a0813bb00eef0974b68222cba6add046b831c086a1c68c`  
		Last Modified: Tue, 01 Apr 2025 17:07:26 GMT  
		Size: 78.9 MB (78942217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d58d3def14be9f0b0952450a1b36b47b8e3df75197d829797ed1325396349`  
		Last Modified: Mon, 28 Apr 2025 23:11:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0887be8e476b07da151c0d6ed847d3b371178a969f5097b48cd8d85cd8dff0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a6d6ed2b30cd3d854bbb14a3c5f3895a3cec658886fb9b9c98959f3570b015`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0a880942b6ea23ba49cd365603202705058321a5a39f8179e1cc2fbf69bd5`  
		Last Modified: Mon, 28 Apr 2025 23:11:59 GMT  
		Size: 10.3 MB (10271524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a52c0aa51fcd9b242ee52739c273c7f38e4ef570cddae8ba6f3edc05cced27d`  
		Last Modified: Mon, 28 Apr 2025 23:11:59 GMT  
		Size: 27.6 KB (27643 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:361fda01f0ae7140f45fe7fceb9d287ac62c12789d2a5e78f02f007936d9eb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269053288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430ce225bc899f47512ca3240ae4c1172136bb08a116552ce81375199e6424c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
	-	`sha256:a9003e8a4d55742a1a2128c3dabddda68ec2c585f52d2aac5eaee8bd68089640`  
		Last Modified: Tue, 01 Apr 2025 17:07:37 GMT  
		Size: 77.1 MB (77101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cabdd5ce0dc6c2cc2a5be4c94210b968f639888441acda83036485d8f742560`  
		Last Modified: Tue, 08 Apr 2025 20:42:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c119634881d06ed74441f7a69f3e371014b957fe3b17e299c655951392c81973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10107662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855eb6651c89a3f5aa96de034b1ca25546a452c9c8d9548dc1b4bc7a37e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:017911a3c155dd54e319b2a5e191c9fea9c69480ca1a3780057eda0aa648cde6`  
		Last Modified: Tue, 08 Apr 2025 20:42:25 GMT  
		Size: 10.1 MB (10079882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b60da6bdf0988cc4dafc5e1578ee91ba54de266261fb5e544733f36aba741e1`  
		Last Modified: Tue, 08 Apr 2025 20:42:24 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ac74596dd7c9a7afb1b9060358c2a48fb738f7047ff8464214e3ff90c6fe4194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297825457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f95322a4cbef0e1516d9010e45c7e31378ba66ccd6b7c0e6c9839c0df0075ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
	-	`sha256:3b9726b91366b288f3bf9f1b85d5cf8b7e50e8f51867ff670418d5b03a1f259c`  
		Last Modified: Tue, 08 Apr 2025 15:59:21 GMT  
		Size: 86.4 MB (86397502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a002eda2038f0953467f843586445333b2af3e827e57b15849040931f2903fb4`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 75.2 MB (75200208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56146eb78922cf6f61dd2c8d20c1d5940497be10ce6e425fd9e9044825f6f08`  
		Last Modified: Tue, 08 Apr 2025 15:59:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fd71dc79973d366f476b5c81b83d361c569403cd052037c8e0ddf141d7d4892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67a1db62b3de68766fca76726951dd4d77b5517ed1902081e05c293e6eb0bd8`

```dockerfile
```

-	Layers:
	-	`sha256:92162f0e478c5f9cbf7aa0ea75eec2d30c6025c8616be4e88266a708c91de27d`  
		Last Modified: Tue, 08 Apr 2025 15:59:19 GMT  
		Size: 10.3 MB (10299419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e70685990bfca539d160c1e92b6caa7e93d4a37892f6ff695d2ead96b5c1eba`  
		Last Modified: Tue, 08 Apr 2025 15:59:18 GMT  
		Size: 27.8 KB (27827 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:125e3aa7aa07127a3b53def8415b03aaa43b578c451b6d16e822dc0fefd145c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307205516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873fe69f3f1b2b32ee18e95a21530343803fc55d5861055a7900334d075d69fe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c1d032612535d234d3d73a4616da4f40748ccd693d2a47809db5b9e9a730bc`  
		Last Modified: Mon, 28 Apr 2025 23:12:30 GMT  
		Size: 89.8 MB (89777304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb556227a38cd463b29410ff393a23b771d304e2f2f265b6c233fe487c9ca9ff`  
		Last Modified: Tue, 01 Apr 2025 17:07:28 GMT  
		Size: 76.9 MB (76873414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5e9cf3b358f65b492e64e75e5e37b834a00a83c243efbdacf5ef42eddb8e24`  
		Last Modified: Mon, 28 Apr 2025 23:12:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:650cd5b72033a743fc5dc716497c8d1871b831a7714ec78b92b3289fb5503f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b9e0e014e62210d07b5cf04f5c1de588564a57153aff50443de2315439c2c7`

```dockerfile
```

-	Layers:
	-	`sha256:5c85a9a45b9c7f5cffb38ed3657a231eb17ec2492ab9e2ee0f81840f8b5ce887`  
		Last Modified: Mon, 28 Apr 2025 23:12:28 GMT  
		Size: 10.3 MB (10251582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06787cf93e633ef783f0cf8e5af8f18efde8457662680b75fafce9cf45b8fc8f`  
		Last Modified: Mon, 28 Apr 2025 23:12:28 GMT  
		Size: 27.6 KB (27590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:05deb961a4d1cdd30e9fb9df46ca9b1c2af40414f95b68882b8ee24c841afa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278499830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18abcc6c0a3e3c8f625e3661e916ef51dd1e0e09e3c215a422efaee4f1907305`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
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
	-	`sha256:4a495918ec5dbc0a69aeab6f4eb97f48d3402581aa82d0c68e55768767ae9863`  
		Last Modified: Tue, 01 Apr 2025 17:09:52 GMT  
		Size: 72.9 MB (72904449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef7cb7d1c230e73fa4b4370823cdab9de51fc1229f3d366b2d6a17d83ee5ec`  
		Last Modified: Wed, 09 Apr 2025 08:20:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:565a80b7cc6473ccfc590ca030aa545e249da377a7c2882d3da936be2c974058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f09428d2084a913850602907a4b065fdb490e5316721159b3243783fbe0979`

```dockerfile
```

-	Layers:
	-	`sha256:09ad673c79d7854270c2073a097c7696fee67a5b6b591ec8b7e27dd80f68de51`  
		Last Modified: Wed, 09 Apr 2025 08:20:40 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:a7a7659d42f12731038a1e251b1fab7236b658bdc2fe8635a2161494d11d42ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313674799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6948e3900225d569fb3df1c88f21942a1b72a062be0f0a2fae8299d6017b1da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f4ea6f35d734e3ff8a820a7991e5169d5d24e7cc87410ff1b6ff4af4451028`  
		Last Modified: Tue, 29 Apr 2025 09:16:22 GMT  
		Size: 90.4 MB (90350689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee95abad5ecea3c593f42714d65b6f62167cc9a1a7a50eaad85a7db940a3e7f3`  
		Last Modified: Tue, 01 Apr 2025 17:08:51 GMT  
		Size: 75.5 MB (75501286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620e8cd354037350a6422020f9fdf5434defcc04b3767a7c48b8216baead4f3`  
		Last Modified: Tue, 29 Apr 2025 09:16:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b73df6eb0454595d898475843001972173272aee57c07cacb22ec5946a64a491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7639f206a566a52366d34681f6df4486cb49b08958002ae8df7a29c44416e7`

```dockerfile
```

-	Layers:
	-	`sha256:98a52295af7214c22f578d8e013c59b777b7c2d9862c6de4a03842f4893e40d8`  
		Last Modified: Tue, 29 Apr 2025 09:16:20 GMT  
		Size: 10.2 MB (10244237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c6ac233f0a469d82e70f21e569be9f62e3a6058a530abb79686f905eedd5e9`  
		Last Modified: Tue, 29 Apr 2025 09:16:19 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:9fa5b950d5177871a6afa6feb79b5ec504594b735c89d12d9817601ec9b1ad1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281339620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8355f2bf0a23d3ecfe65723614a277a356f8c28359db86a57505c6b342ff7974`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21538ac18bce01dcbc388d1060d1f4c02072e1607d7a15b2413b5a33918fc4c5`  
		Last Modified: Tue, 29 Apr 2025 05:38:51 GMT  
		Size: 68.9 MB (68938513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64586fca58b7ef9b98d81252f6468cd1afe274720313716be72d0e12ecde9791`  
		Last Modified: Tue, 01 Apr 2025 17:08:27 GMT  
		Size: 77.7 MB (77744430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a70515753abdb627a40bc0372ab8aca9374fd23f4436a6965a39c00c3286b6`  
		Last Modified: Tue, 29 Apr 2025 05:38:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8d0d2a28bb94611156c9343b8c4bef2546b8de53ae16bd10c3f58cbdf2fd5009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdbed3e1d3732fd3466d71c2297d607383b4e22ee9e7e1b5178d823b381d6b9`

```dockerfile
```

-	Layers:
	-	`sha256:9db1c9fae8aba6bac104e40fa36c4e3e899163518df2394b1fff06a12fe87adf`  
		Last Modified: Tue, 29 Apr 2025 05:38:51 GMT  
		Size: 10.1 MB (10107504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:126687348e5482cf5767ff2fd282a04010807faea960107e4b218b62d12af00c`  
		Last Modified: Tue, 29 Apr 2025 05:38:50 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json
