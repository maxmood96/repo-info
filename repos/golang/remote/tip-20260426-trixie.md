## `golang:tip-20260426-trixie`

```console
$ docker pull golang@sha256:0a983e2977f2705b3f5e3153ad34fa3c35f390734f33ebc739a48263937973bd
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

### `golang:tip-20260426-trixie` - linux; amd64

```console
$ docker pull golang@sha256:c057ee27e3174abba1bcf6679789a5cec270b844914fed1f9325c146d021587f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342216741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83613eaa186916c896c16212d0ddd275bae23283fe18e7e57e7cfff4a91d558f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 00:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:19:36 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:36 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:36 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467f93954cfe1451f4333422086d00bd066cf33f42112b531804ffe06f0a929`  
		Last Modified: Wed, 22 Apr 2026 01:39:50 GMT  
		Size: 25.6 MB (25622443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d12c8f3f3fbb5bd2b8369adf3213e09d6b33f975462543ddfece85b2fe85e5`  
		Last Modified: Wed, 22 Apr 2026 04:45:50 GMT  
		Size: 67.8 MB (67790089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631da0143c92b2acbe4115728128cc86062fca30f60882da979821a4f4994c92`  
		Last Modified: Tue, 28 Apr 2026 00:20:07 GMT  
		Size: 102.2 MB (102169511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779709856b286b334888c2db50fa75d06845c18a6db8049d9f565750e3ae705d`  
		Last Modified: Tue, 28 Apr 2026 00:19:47 GMT  
		Size: 97.3 MB (97332439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7a7c6eca173c994c563cb3da47ce2bdf759ec6284a1b7c247df6506400fd33`  
		Last Modified: Tue, 28 Apr 2026 00:20:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260426-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d0a57212ca300983bc96c6a35b8de9879ca6d81441d19bd181139acd2b2b3af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59a86c2a4a6d160f00b421d56ddbceb30212235dc40f38cc3866b95444a589f`

```dockerfile
```

-	Layers:
	-	`sha256:a7c003d6cdfad69785ba3adf6ee6391fb2880d196c78be59710a5f13ae43bb89`  
		Last Modified: Tue, 28 Apr 2026 00:20:05 GMT  
		Size: 10.8 MB (10785713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603c452fc2571592f95a28c7b4080f6c42f5d47a45b666d32dce907f61e0f147`  
		Last Modified: Tue, 28 Apr 2026 00:20:04 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260426-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:174719ef0d98a83f4610434d0a5cd89d344f965563e021a21a05336a598c5bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298073983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe800aba3fe168b2d412aa03e18967bf3c8442f7b65dee20d3dbb1cb82af342`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 00:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:20:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:20:37 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:20:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:20:37 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:20:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:20:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cc74239df6a59971739f1b7a0758f97ae57e6ab4f74daa64d264ec77db24169f`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 45.7 MB (45738193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f411318175ae51ff20f60969311f63c366288f8aad04eda4d0389d8b016c9`  
		Last Modified: Wed, 22 Apr 2026 02:19:59 GMT  
		Size: 23.6 MB (23636616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341da7892f7aceb1342cb554bdaf16f78292d5247e1ef9fb0f351c24aadb1f0b`  
		Last Modified: Wed, 22 Apr 2026 03:52:40 GMT  
		Size: 62.7 MB (62721455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fc1801c8bd8ed133ad861d9b3d51700a64114224114f2dfd8d34fdd0b18bf4`  
		Last Modified: Tue, 28 Apr 2026 00:21:06 GMT  
		Size: 72.8 MB (72805097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d73ddf188a2e2e6775fd1105089506e6b38ccd4ec9defa63926d5363c7b9227`  
		Last Modified: Tue, 28 Apr 2026 00:21:01 GMT  
		Size: 93.2 MB (93172464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b615ac196fbcce73195e31fcc58c09c1f5e94c38dbf7da308693eed2d635cff`  
		Last Modified: Tue, 28 Apr 2026 00:21:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260426-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c6ff5f054bf60be8ce2e842133ffb867a0126930afe28f1c34f8832ac8c4219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26703ecf605b2b3f093422c0398969adc802ab0d34f53dac52e7aca49c44ec95`

```dockerfile
```

-	Layers:
	-	`sha256:541f9ddbce2015b74da06b0057d5e1ff12199ff02db1e7a7f5fa23a7185ada93`  
		Last Modified: Tue, 28 Apr 2026 00:21:03 GMT  
		Size: 10.6 MB (10581600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18315291fb4e3fa02e639c37e070aea8ea533d34ce3bdf86141d46e79c6f4174`  
		Last Modified: Tue, 28 Apr 2026 00:21:03 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260426-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b8359a748dfc0929b8c3914363ae3d636418f35a9c3da54dd5d26a1ce268b07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.6 MB (332627290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4272598bd825b5955519b65a62d6ccc45876eda76a5aac1f61feaa062ffec843`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 00:17:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:19:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:22 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:22 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705f67984ab3d0b84dba0bf1b9e75bc42547713ab962aa5b392bacb0e61fa68b`  
		Last Modified: Wed, 22 Apr 2026 01:43:34 GMT  
		Size: 25.0 MB (25023409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17e454c787ef19107fbea0250c33a4b6ca95fe0319ad68539a7bae9d9cad57`  
		Last Modified: Wed, 22 Apr 2026 02:32:52 GMT  
		Size: 67.6 MB (67584735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688a77cf5e5e0fdaa741d5241188c6f55952358e1038a31db898e1c801dc0263`  
		Last Modified: Tue, 28 Apr 2026 00:19:58 GMT  
		Size: 98.3 MB (98310055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324bee5f74040b6510924c3347f3aeb86c3579f67dc47584d6081f70bceb6576`  
		Last Modified: Tue, 28 Apr 2026 00:19:44 GMT  
		Size: 92.0 MB (92039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b324f6b162d6978294c10dd813f3d9c86c16996609f9d47e7c12fcd7878d9e`  
		Last Modified: Tue, 28 Apr 2026 00:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260426-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6693995b6f708e5561cd1eb00f3b2036b82dde416471a629bbe0faf0e4b4906e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864cca01da8d518dd84fcd4dec430050739fa669d792edb7cdb57752aad2dcc8`

```dockerfile
```

-	Layers:
	-	`sha256:9807bb6a3acdb9a076386b6063c5cd4745c18dcf3c938c0344a0981082000310`  
		Last Modified: Tue, 28 Apr 2026 00:19:55 GMT  
		Size: 10.9 MB (10906168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:742b88155de2f3701a08483ac4759a5f0aaf2cf5aee81ab3ac1ad2cac57fa7f0`  
		Last Modified: Tue, 28 Apr 2026 00:19:54 GMT  
		Size: 29.1 KB (29123 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260426-trixie` - linux; 386

```console
$ docker pull golang@sha256:d66ef55e0af7d68fb2700374cd04b650e03d631d272c796f0c1ba6f42a07e2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343116443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0b2e2c8c4565c063c1750d99c949629b516462de5e8e758971743de83f172e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 00:19:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:21:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:21:39 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:21:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:21:39 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:21:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:21:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321bfd0f3573fe94aa2216d1519cf604989d7a9e912196633f5d9b7a4e8097c`  
		Last Modified: Wed, 22 Apr 2026 01:43:12 GMT  
		Size: 26.8 MB (26784835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cdc00799a2a5d425863c783516cdc5139f867d081df458a78cfa749e9d7c3`  
		Last Modified: Wed, 22 Apr 2026 05:03:55 GMT  
		Size: 69.8 MB (69809793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad18476d7d96e288ca55a02ab819e3ed928c119ac3de7acef31faeae9b94c34`  
		Last Modified: Tue, 28 Apr 2026 00:22:10 GMT  
		Size: 100.6 MB (100608477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d6a9c589b969b9eee8b2fb5a3d53dcb1feacb04a0d56a4902866f913a72511`  
		Last Modified: Tue, 28 Apr 2026 00:22:10 GMT  
		Size: 95.1 MB (95087823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a429de5d1682d4da4e1a28cd992f4879c800daab16e457abdd48bb7617f9448`  
		Last Modified: Tue, 28 Apr 2026 00:22:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260426-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:848c3931f487d0b1770b1981163c25bcb6b76cfaf6ce400396e2e0970365ba3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adafc36051023d59424a44de572dbce563608f46099ba2842f408d6e7bcccfca`

```dockerfile
```

-	Layers:
	-	`sha256:0104be862af59ad459c387c10750ba846444318803f2759d1e75353ddeaef797`  
		Last Modified: Tue, 28 Apr 2026 00:22:07 GMT  
		Size: 10.8 MB (10756976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1922f0a484ed8ad68de3973e61f97f6b6d9c19deb5063ba4911c76bea77b9a3`  
		Last Modified: Tue, 28 Apr 2026 00:22:06 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260426-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:bf45b9f3f6d457c23037d48e5e61ffdf59089da95a75522d85e16412e5df36bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339945359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fff40a2e12bb09c69ec9973cf8320b17031c3cb2783e8660a46ae6310666a8f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 00:22:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:21:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:21:51 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:22:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:22:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2454d511c21492888baf49902a298f334e8095ce0fe93b53b274ab3f39febd31`  
		Last Modified: Wed, 22 Apr 2026 03:40:51 GMT  
		Size: 27.0 MB (27014616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9e1a80821bce13187cd275a074ab44791a07c4796e61afbcda3a692b97ac4`  
		Last Modified: Wed, 22 Apr 2026 09:39:58 GMT  
		Size: 73.0 MB (73039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a983d4649ce6abe29559fea98afadecc2c2046d72659e362c49cf7c2007da507`  
		Last Modified: Tue, 28 Apr 2026 00:23:17 GMT  
		Size: 92.9 MB (92870376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e34165e157d14e975c070ad73c3dbd1767de1fa84e282e6505d64626df00ff3`  
		Last Modified: Tue, 28 Apr 2026 00:23:11 GMT  
		Size: 93.9 MB (93897536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31cb20e029767efa1657865e46ad351c81fa282dc3fcfc754fcdd510193ce9`  
		Last Modified: Tue, 28 Apr 2026 00:23:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260426-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bfeb41b600b099ab52bf07b0c93f933a6a60da3ade575996d8c8c7c0ea53d02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f38010248b28eb37139f3dc603732fb22acc3a97ced7119ff47bc8ec2e1615`

```dockerfile
```

-	Layers:
	-	`sha256:e3d0335c44d1ecd14696ff53df5066003bc9a07e546c6ba416883f1781efbfb0`  
		Last Modified: Tue, 28 Apr 2026 00:23:14 GMT  
		Size: 10.8 MB (10781501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96a850357baad08381f412a830bdaa11201f46b170d119193b2a946e31e61e14`  
		Last Modified: Tue, 28 Apr 2026 00:23:13 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260426-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:4b52ec5138439bdc0ebea6bf22dd9027c6b33b03701634dc00d245ca19e66657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365476009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bc11a3b2bf799928534ba3e40981a54566dec2cda8dc4d34cdf59b69641599`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 19:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 20:31:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:56:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:56:48 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:56:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:56:48 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:57:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:57:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad20ed76b58e7abcec15ac3129845a802887c092560883b4939e006992099b`  
		Last Modified: Sun, 26 Apr 2026 15:22:58 GMT  
		Size: 25.0 MB (24955805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233e35e9c32890f2d416d3e6707a14b173707fad25985773c22f4606dee5c05`  
		Last Modified: Sun, 26 Apr 2026 19:10:01 GMT  
		Size: 66.6 MB (66648074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954c4b6ce8f364903d1d8a7ac953d1cbfe6ecf95f3d8c267e0b27a58b6e61bc`  
		Last Modified: Sun, 26 Apr 2026 20:39:36 GMT  
		Size: 131.6 MB (131649887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f21692e8d3232006360c86abeb47c76c05ae0fd9556f2ba4bef366f9fde74f`  
		Last Modified: Tue, 28 Apr 2026 01:03:40 GMT  
		Size: 94.4 MB (94423868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6037a21fdf5c0d96a153e04c9089c02c9a046ff402277b70f5df997346a46955`  
		Last Modified: Tue, 28 Apr 2026 01:03:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260426-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6abd87159cdc1bcfb1b82c41f94bf10d2c9b79b6fa3cbba8cb6c4e4925e7db8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910095e0292d1c6ef44f0a2cb35bf1db5c19cdde66b8e205c1edc0d5e2d5042f`

```dockerfile
```

-	Layers:
	-	`sha256:19a3637a71fe188002f2344d4c5cc8cffa760248743758c568e0d4fc4180d20a`  
		Last Modified: Tue, 28 Apr 2026 01:03:28 GMT  
		Size: 10.9 MB (10855334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40371607227770f52d8dee9a160450e39c5be2bb04b88c80700a799ee95897c`  
		Last Modified: Tue, 28 Apr 2026 01:03:25 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260426-trixie` - linux; s390x

```console
$ docker pull golang@sha256:ac517c2f4fd37be72945bca661d41bb9d7c27093502c3f484eb250627a8fae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.7 MB (316675535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b793eec18edbe6d0bac3edabeb9f26ec7fa1bcc47f4252ab8fbad61131a91133`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 28 Apr 2026 00:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 00:35:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:35:11 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:35:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:35:11 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:40:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:40:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a3da428dd91e4b5df556514e279e6a571eec116b1f2b3ed1bc95489fcee4`  
		Last Modified: Wed, 22 Apr 2026 02:32:51 GMT  
		Size: 26.8 MB (26802425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81397603fbb04688ca83ea8697469c3a01388a59e003d38dd37d22beb13789`  
		Last Modified: Wed, 22 Apr 2026 04:21:39 GMT  
		Size: 68.6 MB (68636900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fee8c54311f96935e9a24dbc2079cdad989c86f5045a5cce3743c2c51afdac0`  
		Last Modified: Tue, 28 Apr 2026 00:47:07 GMT  
		Size: 76.0 MB (75982488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c795090f7b3ba987c0e4ca6fd1eb3c889fe964ab0c0eb932bae581f24e4f796`  
		Last Modified: Tue, 28 Apr 2026 00:37:36 GMT  
		Size: 95.9 MB (95881458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6102d697beeddd6c0fe58bf11844fbb76552ae248b9ffb2ccbf347e94dcb5b35`  
		Last Modified: Tue, 28 Apr 2026 00:46:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260426-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3bad2a6a43a865eb1e5a524978cad066a9d53947c984f2dbdb8b7d9a3a80b330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4402d96ce5c5c5782182c62fef6dc25c2d0d7415f2cdbbdc0598b28098e037`

```dockerfile
```

-	Layers:
	-	`sha256:c7b8d117909e26ee6d3c09454c537f30a3b9d90b13761e3d25cfab2d59f3632c`  
		Last Modified: Tue, 28 Apr 2026 00:47:02 GMT  
		Size: 10.6 MB (10596861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0629c423e21d26d5f8b3b2d657d166b5d58b08be7dc3fc7591e7c6b2e417f07`  
		Last Modified: Tue, 28 Apr 2026 00:46:54 GMT  
		Size: 28.8 KB (28791 bytes)  
		MIME: application/vnd.in-toto+json
