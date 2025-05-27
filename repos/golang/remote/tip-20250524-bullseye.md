## `golang:tip-20250524-bullseye`

```console
$ docker pull golang@sha256:88ff606ad7cc609096160e008880a7f25e39091ee4566e042b73e988d2e42cd0
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

### `golang:tip-20250524-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:3261d8b251486d0b49605898dd92ee8bb6fb2ed47f7a3999f592842282302127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342243221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e358bf4a4501b4145638c7e5596f16225c1d6b5d7be977cd370bf4023237b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd26b91052ff6c0990a3dc46ab29356fdf3758b3df6a1f656f066d237dc581b`  
		Last Modified: Tue, 27 May 2025 19:05:51 GMT  
		Size: 91.7 MB (91729768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37739a11166de3eef493c06e2f945d1e527fcbc7b45049a9bf54b5049c44176`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 126.2 MB (126240918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038944916fa052aeed89c5f8f0894600493ca22396029760b048dabd72a1a2ea`  
		Last Modified: Tue, 27 May 2025 19:05:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8118dc29e20a1be4dd788c63393998aaa9c115d636d14c4267f347dd25e61189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10342120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe367b43b012d12e542842bb624e6ff1f396054bcf4b84199221c4e68a23215`

```dockerfile
```

-	Layers:
	-	`sha256:65659dabb20c31c7c736d86d776f614ea3d8d80c0dc1be0cec88b782fa40d472`  
		Last Modified: Tue, 27 May 2025 19:05:50 GMT  
		Size: 10.3 MB (10315059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc47e400df816b010c50e5140c02d835fbc27fc8757530d87088c9aa0f57005a`  
		Last Modified: Tue, 27 May 2025 19:05:50 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:b609eacc191589498b6232eb0ad12b86542db7be76190158be490365be95bb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300605357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a4347425009ee98cbf0326890e60e213de1b39a2ebb7a9d9208a5969e0db0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Thu, 22 May 2025 02:28:36 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Thu, 22 May 2025 12:12:20 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd4739ceb6e38b56a017a3579cc385de56e1cf7fc98c2c4b4dabd966a9c123d`  
		Last Modified: Thu, 22 May 2025 15:41:13 GMT  
		Size: 64.9 MB (64942454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0fe5e7d3d09e12944b416a2054aa6712ade9bdcb8b3878cad2dddeefd549a`  
		Last Modified: Tue, 27 May 2025 19:07:16 GMT  
		Size: 121.1 MB (121108917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147451190c650c6c45a359e06588d0c561d20fdc49b6178212653b97fc306a15`  
		Last Modified: Tue, 27 May 2025 19:11:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f96eb589ae34bad2418b0f031f0db9be06c7cd308d243bd0d1a0626714a7e52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10146167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eead97c1126d85135a13a87a404a8212ac6cceebdde47105a3796a13160de436`

```dockerfile
```

-	Layers:
	-	`sha256:0872c5df65062452a755a1f2e3f36fa4adcd7911ffa63c024e13652913366331`  
		Last Modified: Tue, 27 May 2025 19:11:58 GMT  
		Size: 10.1 MB (10118998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6a57f79cf031efd6c448550e660d364c22ba21af70eb38be87118f20e7109d`  
		Last Modified: Tue, 27 May 2025 19:11:57 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:549606e4c421ae003807d61198999b8a69219a9df68c0403f296b563e7cccebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328260472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f2f802ce6563e0da34ac36584b930488e76d468dad89ee1ef985bf40a78716`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Thu, 22 May 2025 02:47:52 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Thu, 22 May 2025 09:18:36 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4f13c9f2ba35edbb5cc356335d05db12609ba76252d1006e9168557548c91`  
		Last Modified: Tue, 27 May 2025 19:26:08 GMT  
		Size: 86.4 MB (86354667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea33ecb4b895f73f5e4d5736d5a0a4109e5ac27823a9c5ca57f0642e5a3d9a8b`  
		Last Modified: Tue, 27 May 2025 19:23:28 GMT  
		Size: 119.1 MB (119054274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fde0b4cb5f626b29c5d5d24c0e929c4713c7559bf258e92237b2b70d70156f`  
		Last Modified: Tue, 27 May 2025 19:26:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2ba665099c594f040296813558e8c96a71fc4069f8310ab0f63df9f0738aff3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10343538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf17e3a4bbc9169af70229f5269bdba31cd14aeb33c063a4ffc77b09f2e7a8ab`

```dockerfile
```

-	Layers:
	-	`sha256:2d529690e2ecfeeda590855acd50614ca035d4d2245a2ffc9440e499ba71b495`  
		Last Modified: Tue, 27 May 2025 19:26:06 GMT  
		Size: 10.3 MB (10316341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce84b8f7e2569dc7cf812ef2eaa64728b6446200dc7eef1daa500f621c66af70`  
		Last Modified: Tue, 27 May 2025 19:26:05 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250524-bullseye` - linux; 386

```console
$ docker pull golang@sha256:b9d61c170c0491a8dc632736e7d0e754ad4c67b68e82176cdc9e7e53edfa08e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343937683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3cd1c25fdc1ac5c552873cfb86128991c80cd43919a0a6352f3c9c10ea085e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b881253641f187a1de4710d06c9a855344b38f1480cdf2cf92d4f4a0c980f7`  
		Last Modified: Tue, 27 May 2025 19:05:58 GMT  
		Size: 92.7 MB (92726300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb63d3af1099d61647a313155e9eaa0aeecda078cbf5fcab7fb7996b234e196d`  
		Last Modified: Tue, 27 May 2025 19:05:30 GMT  
		Size: 124.2 MB (124207178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cffe1c6e2deea40806ca7888bb8d8e81c70dce11a17a19d47096ca203b6ab1`  
		Last Modified: Tue, 27 May 2025 19:05:56 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250524-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:bd7c7111148fe515f8620171d9b9a56b7102623c19fd05475d6baaf4ace8a714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251f0c6e600ed64245f43192b05db1b3661f651d97d4ad7651ec99c14e22a25d`

```dockerfile
```

-	Layers:
	-	`sha256:72dc8e8d295388118dd0490251f9b438d78e50afc91f07f9af67df862f5840d2`  
		Last Modified: Tue, 27 May 2025 19:05:56 GMT  
		Size: 10.3 MB (10304372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055b2588c8de541dd42877bb7cbe526972cc983d762ddc82d75de44330773ce1`  
		Last Modified: Tue, 27 May 2025 19:05:56 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
