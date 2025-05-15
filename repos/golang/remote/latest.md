## `golang:latest`

```console
$ docker pull golang@sha256:86b4cff66e04d41821a17cea30c1031ed53e2635e2be99ae0b4a7d69336b5063
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
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
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:631c39509701926f8250cc55a81ef158c702c0e735a9c6e49928e896930f4309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308228282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f254902cf370928b679920608e9c01b79b786322f05fdabc39fbf8477c21a91d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb27318808bdf2908c6efabaaa47a7b8f17111ed03f186e7378c131461c189e4`  
		Last Modified: Thu, 08 May 2025 17:04:43 GMT  
		Size: 92.3 MB (92349744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b00dc8dfbaa6cd7e39d09d4f1c726259b4d9a29c697192955da032f472d642`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 79.0 MB (78981573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9984258df29b0a9d740d2cba51aee36ece6978141ba637b98e384247989a2b4`  
		Last Modified: Thu, 08 May 2025 17:04:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:f20b8b03efdba1e03e574c0ca7c3dadd613947c657659d12c0065306d764a26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e10f4bb790985cd2c402fd386875d1ab806167a4d57f380537fe9805f747794`

```dockerfile
```

-	Layers:
	-	`sha256:1e4b191401b9637c3ff4dc579c94ab8d710f015331eb911c05690199764f0a8c`  
		Last Modified: Thu, 08 May 2025 18:02:30 GMT  
		Size: 10.3 MB (10271524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933dfc1cb9b235720ceebe55cf80365fe4701ca30de2f24afc9c17a19d96f5e2`  
		Last Modified: Thu, 08 May 2025 18:02:29 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:e3bce7b117061d486167719971921c04b01f3d57fe25eb514f10b08c38ceb32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269122738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab9aa2b535498d01d83ac982cae5737cc7a8678fdce51863a5c2a22983c2a1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Thu, 08 May 2025 17:05:35 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Thu, 08 May 2025 17:05:43 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6442f47db55887d087c4346d5fccc35d5cd8441653b35deaf402943d7978ae1`  
		Last Modified: Thu, 08 May 2025 17:05:40 GMT  
		Size: 66.2 MB (66222470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f32012e82345c04270d988b1e520857596a775a43ec4b22744ab73bea39d15b`  
		Last Modified: Thu, 08 May 2025 17:05:42 GMT  
		Size: 77.1 MB (77144440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5990b5a81657a0809a8fb517e93ee0b51b3a9e125ff9de60773f933a595a08e`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e4afe800bc5b716c09c71c8692ea14ed963960f411a44a733471d599a6e1fd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10107662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fc3e72650b1485841f7b3910f94a0f40d7f3d6b18c81ff732abb64c6507170`

```dockerfile
```

-	Layers:
	-	`sha256:49a42d11fd075b714230bce370e690ebe1f41022b6173b493408aeeec2175d8d`  
		Last Modified: Thu, 08 May 2025 18:02:30 GMT  
		Size: 10.1 MB (10079882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a899346f436399dbfdc30942269e8d3d9664863ab812dd200edd09bce3e95cab`  
		Last Modified: Thu, 08 May 2025 18:02:28 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:50c0ead56e09cadf5155ea729080eb6e027bea74732105ff2cf49f76fd61c662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297873705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c6e3bb3e5c7b020a44163a3e8a1b9b30143638872a19bdfd2bc91a854cf03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919170863bb5513bdfe1ce20b4f372538ef99b950b570408aa6aec57bfd91916`  
		Last Modified: Thu, 08 May 2025 17:05:19 GMT  
		Size: 86.4 MB (86415404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae64884db43f30f8dbc9ec3362124d99c8bad23b957254ac52fb30413bd14a7`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 75.2 MB (75230554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5990b5a81657a0809a8fb517e93ee0b51b3a9e125ff9de60773f933a595a08e`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:5dd346e4397fa731fb8a3048ae5464293ef3dd35e84c02d776268dac44484b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fde0e27d8ceb432867c5aea09769b368f6c76a54090160b580b53fcbae5457a`

```dockerfile
```

-	Layers:
	-	`sha256:e10badb12bd366fdef4e4102994fea2350fb7a54538ab5aaff409a8624952360`  
		Last Modified: Thu, 08 May 2025 18:02:33 GMT  
		Size: 10.3 MB (10299419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a503c46a6bba924d3691a44cd94653f44923741be3c323f19746e4cfc49758d`  
		Last Modified: Thu, 08 May 2025 18:02:32 GMT  
		Size: 27.8 KB (27828 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:246d1b250184326fdc19a5e00ce712b6fcd6fb4ed5ad37ec076652819646bb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307231939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cd65804207e5431deed9fd850a9065f73e3eab49e2fdf99cde5ea072db7eb1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Thu, 08 May 2025 17:05:06 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Thu, 08 May 2025 17:05:07 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfeef1e6990a6b5d7cc38187e5c3e9a0d284ac176bb0d828d346655c7529be3`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 89.8 MB (89777261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db714197af43811f01d03462392675e848884e82b9483811c21c83a08d3e7834`  
		Last Modified: Thu, 08 May 2025 17:05:08 GMT  
		Size: 76.9 MB (76899879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d420ed634aae4ba011e789094581b5a40d30c046e7ee8d53ba05601b09d9e4ca`  
		Last Modified: Thu, 08 May 2025 17:05:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:7b15e8681bd65e0e4eb4ae92c12d0ab11dc2c79f5d3b505a61ecb5a04d7ee48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c0d16d78e26819869b46fe0960e258d66e0ec6762014d5813201dfc9745766`

```dockerfile
```

-	Layers:
	-	`sha256:c61cfb542105182b64493a8e0faca30d07569fd3dc5eb8fba50f31b8580fe9d7`  
		Last Modified: Thu, 08 May 2025 18:02:34 GMT  
		Size: 10.3 MB (10251582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2967391b5bab98ab9a177e2adc0f1e27de2649bc789a9d27b637f31c6e4bd0`  
		Last Modified: Thu, 08 May 2025 18:02:33 GMT  
		Size: 27.6 KB (27589 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:75222353b111b18ec5d0f62f3802dc3e871dc7e8f190dc181fbbb2eeb1b36a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278551738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73288ccafbb97ba8d1d0b9ecd07877fdbe53ac0518be78685da58cfcb7bdf459`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Thu, 08 May 2025 19:59:58 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Thu, 08 May 2025 19:59:57 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d30b00e6e88ef455123e625951481f519a50849cb9e967c590e851c17b408`  
		Last Modified: Thu, 08 May 2025 19:59:58 GMT  
		Size: 63.3 MB (63308148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c420f992cbaa8d211ae04be243041a640a38dda712f3d832718a146e390dd6fb`  
		Last Modified: Thu, 08 May 2025 21:10:27 GMT  
		Size: 69.9 MB (69942341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1867a949d6ccbea12d3fff41faf48179631d5f8ade3c5dec1f8b21e46bc082f`  
		Last Modified: Thu, 08 May 2025 18:02:37 GMT  
		Size: 72.9 MB (72929920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d89dabf642b4ea5c3400271145fe2dbb5688d2978d889be559b3cac16d37cf`  
		Last Modified: Thu, 08 May 2025 18:02:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:9cd9f9e95e6efe788ff0aaf1a4d25ae3043fc03d5b6f32d22891762218e226a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e518cf8fa6798c2206a9f98af786b3eafe438cae0a7dec033ed4bef2bbb749`

```dockerfile
```

-	Layers:
	-	`sha256:9f94d2abe0f8afadb086b53349bb8f4894830fc272edc302dfcdd6b36cd3ecac`  
		Last Modified: Thu, 08 May 2025 18:02:35 GMT  
		Size: 27.5 KB (27538 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:0e08e9d1d2a0d58b1f1668bf7ada7071154ee379cbd1a2a7e9d8c3bf3db0eb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313717706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a510dd2a17f63579db0aa98d8c4cac7324fed93181a9c076cb8bd9c4f5bf6f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Thu, 08 May 2025 17:13:13 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Thu, 08 May 2025 17:13:18 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d38985afc96fb14b472c445470120222b7866d3e3e26c3337d073be6739a829`  
		Last Modified: Thu, 08 May 2025 17:13:19 GMT  
		Size: 90.4 MB (90350389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f44821f8171df650a338e8fdd3b017af075382eee8cc2d34256864c2264897`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 75.5 MB (75544493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608b635add8ce41b37f3c8708da012f4d2bf05def08b3cbd9e183453c457c65`  
		Last Modified: Thu, 08 May 2025 17:13:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:cd6954cdc5268b01e7d83b4cfe1291fa1ba505700ec2e8b78f33bda40be324f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb568d134596fd482963e901a9d5c6b6def3606e230aca8d7f4da08fc05f3192`

```dockerfile
```

-	Layers:
	-	`sha256:74e355788e2d25d5f48f52c2926bb04c0916155429850b7f219ec832e8f1912b`  
		Last Modified: Thu, 08 May 2025 18:02:37 GMT  
		Size: 10.2 MB (10244237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a12818e04bce2d0e9528d6d1a31ea00b65f675aedefbfb47ff2313d6ba3cf81`  
		Last Modified: Thu, 08 May 2025 18:02:36 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:647de022a8ad6cb5f41b9b20414a4e39aa755484498f23ecdd626e733b4284cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281382724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7ecdedd57c126c60f9bcc8f535f03c1b04ade25f9c0d44399f3506918a1623`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Thu, 08 May 2025 17:16:24 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Thu, 08 May 2025 19:32:33 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09d77a76fd2957750185d2378dd52b653f61b03e2e717f3f19442ac80e377a3`  
		Last Modified: Thu, 08 May 2025 18:02:42 GMT  
		Size: 68.9 MB (68938149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e83890111f2cfa590a0023450ca3f44d60d123d688835ec1c4ba557b336f8`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 77.8 MB (77787898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32b7cf01d6298801ea0cd0bee6230adddebe89bf5647083fff7526c939b01e6`  
		Last Modified: Thu, 08 May 2025 18:02:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:133217abc739338591fbe6d1b967b95f967e0e31cca6a603bd877a16288f2727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f9f6ff5032129f61177bd791577c4e69d38dc22eb35f8bce662c65314c89ed`

```dockerfile
```

-	Layers:
	-	`sha256:6b086f114a030384f2e02e67e9c110ae73bda556029b016dfb7146b0173cabc8`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 10.1 MB (10107504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bcbde7d1a6c01d90c3bf4d848dfa73a36e9a1b66662d754c5a1cf747314b593`  
		Last Modified: Thu, 08 May 2025 18:02:39 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.4061; amd64

```console
$ docker pull golang@sha256:6bc0e0ad83257fb500878ea9f8790205a804635a7a600ae73181fcdd9a207079
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3564851150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a665a5561f38a12e5a3379a705e8f0dcbcbbc2cf389afed3e4eebed41becedb9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 20:55:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:55:01 GMT
ENV GIT_VERSION=2.48.1
# Wed, 14 May 2025 20:55:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 14 May 2025 20:55:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 14 May 2025 20:55:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 14 May 2025 20:55:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:55:19 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 20:55:26 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 May 2025 20:55:27 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 20:56:45 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:56:46 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f58aea4af0a553b6fdadf460858a20a917ca97ea643c9fb4e8c93cc19b0c41b`  
		Last Modified: Wed, 14 May 2025 20:56:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1986cdc301a9559a5076bda92411ca8c8e837cc2cf181ba17077e894f4c1f2b8`  
		Last Modified: Wed, 14 May 2025 20:56:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7271df3a042deef260e148381dec722c4b2aaf093ce962c2239855930233e58`  
		Last Modified: Wed, 14 May 2025 20:56:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745d303e1ccd8b005effd1a022752ed377fd515c2a56c8e21fd01319afe4a109`  
		Last Modified: Wed, 14 May 2025 20:56:53 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb006a817ce5ec8e63bc183e2d9badc4859a0609651402ea5307b653295d489`  
		Last Modified: Wed, 14 May 2025 20:56:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d7a57c416e28da6beb9828a82ee3f805680105aeea9a9b3f99345e014cc3e7`  
		Last Modified: Wed, 14 May 2025 20:56:59 GMT  
		Size: 51.2 MB (51228824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad1d23635c39fb2c923b711ab89cf42dbfde12792da14bfa9012022486b1fd6`  
		Last Modified: Wed, 14 May 2025 20:56:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1052ef7d8df05b1300a16dfb761a93b4620c225802da82c4f25847be300a31fb`  
		Last Modified: Wed, 14 May 2025 20:56:51 GMT  
		Size: 357.4 KB (357441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d107c447c15b32e7f8b481b732803d027666ead397d137b69b8aac5c09376d3`  
		Last Modified: Wed, 14 May 2025 20:56:51 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e58c5dd99fc3842c6d326083732e43e15edff97cdbbb90ac966774b8cd891d7`  
		Last Modified: Wed, 14 May 2025 20:57:04 GMT  
		Size: 82.5 MB (82488499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9477a2fb02c4f823c33ff1d0f9207d673d5f0936d4cecea3c905967bbdf5fb`  
		Last Modified: Wed, 14 May 2025 20:56:51 GMT  
		Size: 1.5 KB (1458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.3692; amd64

```console
$ docker pull golang@sha256:0b79514020751f04803faecbcbf5170dee5bab0d05fd6fa2ac346108809e8ece
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407455193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62120dcd9b1a56ea62585c43ba0ada6bfe7323893b3a828b943bce92379410e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:58:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:10 GMT
ENV GIT_VERSION=2.48.1
# Wed, 14 May 2025 20:58:10 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 14 May 2025 20:58:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 14 May 2025 20:58:12 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 14 May 2025 20:58:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:58:31 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 20:58:37 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 May 2025 20:58:38 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 20:59:50 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:59:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45127ee6ebf703baa05591c7a349c722e2b85b514cfec86d51bb45b63e371d`  
		Last Modified: Wed, 14 May 2025 20:59:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8441c7ef75b6ede4e8797bf6f6627e21a4959a98bac3f4bf4922cb12697dea46`  
		Last Modified: Wed, 14 May 2025 20:59:59 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9868d3324efa4c83a7e6b186c4a056f8743cb75b7ca2c959beb8ffdd4ae2acdf`  
		Last Modified: Wed, 14 May 2025 20:59:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e63f7f4cd114d851d2d54559a0058c7af5efc40551e51a1c3e7a1098801c7a`  
		Last Modified: Wed, 14 May 2025 20:59:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1254c7730cb2f149a17672b8880a740368cb9945466d7aea5a2ca3594ba1bb9a`  
		Last Modified: Wed, 14 May 2025 20:59:57 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef89c504a74e426e288400795138cbddd17e2e1353ffd2f2f3555da2301433fe`  
		Last Modified: Wed, 14 May 2025 21:00:03 GMT  
		Size: 51.2 MB (51195839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2751a5694075e34cda12f623f75a2fb4eab1414ed4559d352aa76ed6c93e0e94`  
		Last Modified: Wed, 14 May 2025 20:59:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8bd6074b14a6b660e43be5a6803a631dbe311950d4d5d3bd1de627ba819c09`  
		Last Modified: Wed, 14 May 2025 20:59:56 GMT  
		Size: 336.1 KB (336124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7215b89934579f955b47acae4b6f31125379782f2ab0b1f10cd8bbe4c266d7`  
		Last Modified: Wed, 14 May 2025 20:59:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fbb594a85027326471c7a9e7b8c4b1720b5d0c1074750e9967801d22e57e99`  
		Last Modified: Wed, 14 May 2025 21:00:08 GMT  
		Size: 82.3 MB (82284703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a26af9c470bae6f854049c6c58ecdbd4ca7f3438a2d7fbf5ffecc70e065bcf4`  
		Last Modified: Wed, 14 May 2025 20:59:56 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.7314; amd64

```console
$ docker pull golang@sha256:68b622deabed02180f6c985925143b02076942a3d5390e7bae36c037d646eee2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2317822209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79845e1e6db4ba224b3bea4f6a57e4754585372cca319fb3da1a55df8f25f18a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:03:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:03:38 GMT
ENV GIT_VERSION=2.48.1
# Wed, 14 May 2025 21:03:39 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 14 May 2025 21:03:40 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 14 May 2025 21:03:40 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 14 May 2025 21:04:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:04:54 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 21:05:01 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 May 2025 21:05:02 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 21:06:22 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:06:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae1d10c52ba30ae0aaff0842bd5ac1db29ff2a509262e6a69099ffef2e2eaab`  
		Last Modified: Wed, 14 May 2025 21:06:29 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b906e19596d76f1f62cb29bb4f9a64ea59543b8497da1370d2c120c4099efa`  
		Last Modified: Wed, 14 May 2025 21:06:29 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febee24bc823ff9c3d19fd79b83189fb17947498a9d91be3faa429ffc1a91450`  
		Last Modified: Wed, 14 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa1fa357b5ea0b14d584bf6b59b5a21273c979e15dabf02257450022ffe375f`  
		Last Modified: Wed, 14 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9a8d872e379038e66325ab145e0d0b8227d94799ab335f571f7e494cf673ee`  
		Last Modified: Wed, 14 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90524c93e0925b2e0549b02dc6ce0bcd1ccb51aab2267e4df18429a0129b4559`  
		Last Modified: Wed, 14 May 2025 21:06:34 GMT  
		Size: 51.2 MB (51217705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb6a608bcad4829dbc30abd0dbbd9e5fba4ad42f70c4ce02a0768dd4392f478`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51d9d62e3f9acfb7a57782ba95e0059ba66f86370b10b0e0e7c9b97c82bd20`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 337.1 KB (337105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69dd31260ac1011cb4c0dcfa0b3b682f52aaf100fee15c10ce3a8080bca2694`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e08660d7bc8fd0f271002cd3ca8eb1a69546359e3cdbf275c93240f61e5887d`  
		Last Modified: Wed, 14 May 2025 21:06:40 GMT  
		Size: 82.5 MB (82539039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc891f58f07d15e00c45bd15fe49ef30f48f716bab1aaf722548d3fb2c07a5`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 1.5 KB (1499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
