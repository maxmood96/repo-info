## `golang:1-bullseye`

```console
$ docker pull golang@sha256:cf29cafe674ad5e637311148fb7933f67c4e8cafa79ce066aad0e7aa708fc287
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:a3242a0d5c71b9e83c2996daa91ae2b97e0c97c4508ee6a0689ca767ff3d91ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288826206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310589e8caeec01b6fd57ecdbfbf8b2c6090d0840b36dbc1548528f1099dbec0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8be860c3465df97622b463fd27eb858a2f846c9e8c7a42e2cfa408671173bc5`  
		Last Modified: Wed, 12 Feb 2025 17:30:14 GMT  
		Size: 86.0 MB (85971501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a60326dddc23e8774b39171d6496c16678bd44e52909e9a94763d62f3cbf89`  
		Last Modified: Wed, 12 Feb 2025 10:27:40 GMT  
		Size: 78.8 MB (78805485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f410da82edec733531122027386baf32484bc05e1943eee408fe3fc829ce26e1`  
		Last Modified: Wed, 12 Feb 2025 17:30:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d957a12dc192427f3e106e345b7150f8f61b50b8309dcbaf9da26bccbeeed1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46db11983eebe95e3180f16b961fb213d50900ba31bfed749868a7060d3de1b`

```dockerfile
```

-	Layers:
	-	`sha256:fb40ae18b8d808c3eb8e70fdd7cb1606f62171b04ee5db8121b5ac31ba7afde0`  
		Last Modified: Wed, 12 Feb 2025 17:30:13 GMT  
		Size: 10.3 MB (10271760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f44a37a8bc8d406a1449e0504c4a265868082bebfb0817fe780f973a2f1919`  
		Last Modified: Wed, 12 Feb 2025 17:30:13 GMT  
		Size: 26.5 KB (26467 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:f104c6b9406d1a9a992e20418c5dee9664a3e7f7f8ca3d36cff016436beb15e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256199781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f6ddf02ca6866fc9cbc6777e2bf396f347831be35125bdb2d32c1e27971829`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7c48b43b3adcfcfb794cc307d61fbdfd95ebf9cf80b1a014e90a497356d90`  
		Last Modified: Tue, 04 Feb 2025 16:21:50 GMT  
		Size: 50.6 MB (50640069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d641c4fb5f7d6edca115cf3c6db8bc11e32ec83c49422dab7839f4914e1a2`  
		Last Modified: Wed, 05 Feb 2025 00:36:13 GMT  
		Size: 64.9 MB (64892491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff7ce8adbb73c193102166498a2962195641bfa6bbc14e5dfa44f02e4d7d0f`  
		Last Modified: Wed, 12 Feb 2025 17:45:53 GMT  
		Size: 77.0 MB (76968450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd24fa4f3f91ba9a82542866d5b47b49e4c06a8a39ea189a296e687fb2d5206f`  
		Last Modified: Wed, 12 Feb 2025 17:46:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:dab90df725fb11504eac910a0c7ccbd5b782890161f7fd60e97df0ef318445ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10104690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b332e058a34f4abc3ab663216ccea1ec62e45b70d53dada51d5b425dbc0806b`

```dockerfile
```

-	Layers:
	-	`sha256:92b583d0df52aa3c51d13a22c3173feded4f3abfeeb9b6cf47289d2f2edaee32`  
		Last Modified: Wed, 12 Feb 2025 17:46:53 GMT  
		Size: 10.1 MB (10078120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f18009e887412f5fcbb2c89cc19266c5e983c2355c8389657f4123ff4ecb7f`  
		Last Modified: Wed, 12 Feb 2025 17:46:52 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a692552f6607c29c8bfaccc327b4d11d0ec0efcc4147c5f4f3692515e0a55fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279085052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa8b8b96151eb33ea94b1029eac5d4ff89dd39771f582494facf81610674ea8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Tue, 04 Feb 2025 19:02:31 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645f8f0990a7270606266e36ae54950c498997c10e31242c830d3106f5fd7ed4`  
		Last Modified: Wed, 05 Feb 2025 02:02:38 GMT  
		Size: 81.4 MB (81382226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18364ce0d2587c74fc30d8602f743c52178d9e6408c64d9091baffbff467af7`  
		Last Modified: Wed, 12 Feb 2025 09:53:13 GMT  
		Size: 75.1 MB (75060222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e03cd62280c6dfb169bc07d29507c76d88cffa0e95c43f23928425e0aa97d79`  
		Last Modified: Wed, 12 Feb 2025 17:43:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8a2dbcc93d143ae1a2f718121a7f33d333011a0b4d460f61c4ee95fc41373c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368c4ef9110e3ce30d400ec8c78a0371dd2957130bae7d754aaaa6f7ecb29ddd`

```dockerfile
```

-	Layers:
	-	`sha256:1fe63bf355ff11350394da5c7b2bc785272b96d7aca28a06db023719eaaa648b`  
		Last Modified: Wed, 12 Feb 2025 17:43:37 GMT  
		Size: 10.3 MB (10273356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60efb9615aa7c8b7822adbdd208c5af6101ebdb1c359bd6ffca302027213f21`  
		Last Modified: Wed, 12 Feb 2025 17:43:37 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:641d2e1480c57b97df7c8fc8585822264aa37c8d0b25f2905046624a72d77807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290896241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce5e06b462abfb27a0097e1c8ad97864932a8e7ae8b3370807052f4d413a351`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOLANG_VERSION=1.24.0
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOTOOLCHAIN=local
# Tue, 11 Feb 2025 19:31:16 GMT
ENV GOPATH=/go
# Tue, 11 Feb 2025 19:31:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 19:31:16 GMT
COPY /target/ / # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 11 Feb 2025 19:31:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 05:15:33 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745c484ba6641447501fc8ea417761718f1061ed009c38efa118df9340c89ccb`  
		Last Modified: Wed, 12 Feb 2025 18:31:31 GMT  
		Size: 87.4 MB (87398119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366fc1b7517b38e35749547747afd275840849b03e59ce7bdb829acdcf634998`  
		Last Modified: Wed, 12 Feb 2025 17:30:21 GMT  
		Size: 76.7 MB (76730079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eaf4d1639dd8bdd5567cea1f799b7fb31bc8cf40e7cb3ab540b74814da632e3`  
		Last Modified: Wed, 12 Feb 2025 18:31:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:416d08335bc35f72db6d12263c2456561b72ae942b4b10f286db463cdf0db591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10287977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98fb52ca1cccbae052c03531f8b5ee6389d57a218df5a157f5492b83ee75ad1`

```dockerfile
```

-	Layers:
	-	`sha256:865c40b3c30a6383e5da9d5771702ead2ce6dc0ea5365355fc96c0195ed396c4`  
		Last Modified: Wed, 12 Feb 2025 18:31:30 GMT  
		Size: 10.3 MB (10261545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375c8d0a7e82556dbccd97c51ccc756b21deaf1b296eabbde792cbb7bdfbcfb7`  
		Last Modified: Wed, 12 Feb 2025 18:31:29 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json
