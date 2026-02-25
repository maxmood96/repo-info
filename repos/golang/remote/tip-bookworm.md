## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:823777d4b6c34507f4e47b104dcd4e1bda1666db47d14eca7bae4a1a3ea14688
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:6786b4557aaf478221023340773d9cf02ac62e0f015d57cf2a9619606ba5810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322932031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4215c750573053537fed8f5ca830de2238fbb326f394c033a05089cd6070be9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:17:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:19:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:19:32 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:19:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:19:32 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:19:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:19:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ead324cc053655a27bd7c2c7a2d0d0c15da81263d5bfd174f722c02f783c6`  
		Last Modified: Tue, 24 Feb 2026 21:20:00 GMT  
		Size: 92.4 MB (92444836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495feeee1b60c984a8277e0860f99ef7f9650e71ef87f6e01f020f04c712c1e`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 93.6 MB (93563958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b0cd87b6c91f70e99b8337370a36fad0f8c86cb84cacebbc5418e97e7f394`  
		Last Modified: Tue, 24 Feb 2026 21:19:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2eb1cf9a4fe183c6d541e4435839be12d67ca47edc087019c65976ae2f708e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b79cb356ee6d0d23230a5050040403e5dd836a7d1ac5efe737d26135bc44e6`

```dockerfile
```

-	Layers:
	-	`sha256:71faed9daae169079b6b5b908a4d43f6f1b764fa3a70a1e09c704bf00f32d8e1`  
		Last Modified: Tue, 24 Feb 2026 21:19:59 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b958c1d486f88dbe3e8ca73b5ca7b0ca02e198ec0ebd4299d7779dc17e5ce23`  
		Last Modified: Tue, 24 Feb 2026 21:19:58 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:4e85ce2f5245ee7f91088eda008edaf9d829a295842d819636121f3d63561ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281766938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07b12f518c6a413cdb93d5ba565170fc9182bae7635132a9e4c24b544f48f2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:22:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:25:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 23:25:01 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 23:25:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:25:01 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 23:25:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 23:25:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742857c89c3fff9f983a1595594994ae63f49f2e0dd92faaa9d5886d69aedc6`  
		Last Modified: Tue, 24 Feb 2026 21:34:25 GMT  
		Size: 59.7 MB (59651871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bab981a5dd9d6d4a6461416ecc867084bb01868c36c0bef9b4fcd0219a8ab7`  
		Last Modified: Tue, 24 Feb 2026 23:25:28 GMT  
		Size: 66.3 MB (66310521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccb983b4dd6150f64bcdff1ff9f7bd363663b337fb9965a8a864ee527592603`  
		Last Modified: Tue, 24 Feb 2026 20:17:32 GMT  
		Size: 89.7 MB (89654487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068afe7429d15d6541da1c1a6af777d6fbc9058bcfedfd06fd50d4b5055328ff`  
		Last Modified: Tue, 24 Feb 2026 23:25:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:49b51012604777db68010689f4350c4e9810240436f6c4aaa57d028b729239c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72facf9c932294b05183a97b7677cda21d846c6997cf244cde0f1b5f1b1d5bc7`

```dockerfile
```

-	Layers:
	-	`sha256:463e9a6705d9c5ce34c62efefd5488e4e678cfddd0b5faa7225224f66ad10300`  
		Last Modified: Tue, 24 Feb 2026 23:25:27 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5173741f594686856c7eeda98cc693b01f359f26cf196ff419f785ca93ab2d1`  
		Last Modified: Tue, 24 Feb 2026 23:25:26 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2612c28ea277bc9e9177cd6f5ff07fc80702d47b6129bb12566127b34d9e5ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311709818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fd41617b33759aea25403926d82f4eb669fe4f574fc13d078f26ece336b2f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:21:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 22:21:03 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 22:21:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:21:03 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 22:21:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 22:21:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698d3f24b055831fadba9a7980efc7f96b3d06c0b2517a92b2649176b26faf1a`  
		Last Modified: Tue, 24 Feb 2026 22:21:31 GMT  
		Size: 86.5 MB (86525459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c991311643d5ba1266ad32d242c21d958ba93238b33b79d32fc0b23bd2b25b23`  
		Last Modified: Tue, 24 Feb 2026 19:30:15 GMT  
		Size: 88.7 MB (88726849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7868cb0f155d1446984fab5a4a2a79396aefe77378dc192f8d9a25533e7f9363`  
		Last Modified: Tue, 24 Feb 2026 22:21:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5f527576c0c0bd2c510e8a95d30ddf437b96f94fce07cb45c074f1a0fcdb1327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9251efe92bbab25dfc95c8a736f9e97ca18b811839e9041cbccfcc688f5d0a73`

```dockerfile
```

-	Layers:
	-	`sha256:4bca029cedad2bbfe5c29fb5620f73691680148c98e03e35065ba5ab9feba40b`  
		Last Modified: Tue, 24 Feb 2026 22:21:28 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cbae453eda47030057cdb88eeb4d428376d5c66fb88b31bfa3a695106cd8eec`  
		Last Modified: Tue, 24 Feb 2026 22:21:27 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:9aeb668af244f03d37e0f9d62e58dcca03e2a7596ea42a6b1ac5b89da0d2c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321910301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91370cdfd7095a325613ac71e9f0345e503258593b8a117b2bf02595e896df8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:15:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 21:15:31 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 21:15:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:15:31 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 21:15:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 21:15:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383bd8d2ca9c40d67394c0121b8fdb7d7c8f44082342e21f4188fc611c88e9a6`  
		Last Modified: Tue, 24 Feb 2026 19:56:53 GMT  
		Size: 66.2 MB (66234334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0eef27a00b9b7db3948f213e46e37a1218941e612ff12da04f2f04381e2cf5`  
		Last Modified: Tue, 24 Feb 2026 21:15:57 GMT  
		Size: 89.9 MB (89871402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70dcda3c127f8506d59d712159bc64c0b0ee6293dc7af8e7cd42a7bdd642799`  
		Last Modified: Tue, 24 Feb 2026 19:27:40 GMT  
		Size: 91.5 MB (91454447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7595e9a9c0b3b2239280a002f6a76f48d259931ed03e5fb84c1382bcacf8f77f`  
		Last Modified: Tue, 24 Feb 2026 21:15:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:31528947ad120b6ec105c2ed26fe93e17277b7e7fb5beba673548ac1d8c9bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda8383e5a34e2f325bbcdc2d4e42aea01385d7a9a2f134db7486bc5d32274c6`

```dockerfile
```

-	Layers:
	-	`sha256:2c80b7e1ed51984d177257fa901e04d5a066fd43a70726a8f45fb4020d0b1da2`  
		Last Modified: Tue, 24 Feb 2026 21:15:55 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c7f4aa57315a97e711f9f26e1f4ebf399778123b8b523188eee2fb5218b94b`  
		Last Modified: Tue, 24 Feb 2026 21:15:54 GMT  
		Size: 28.4 KB (28352 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:0f6d011850d7b09e1fbaf4c52014ba9f3da6385e29f71f90d5994738a0c4fa07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293051661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f28e35e1e432b795b11aaf1346f1ab97df08cfc330afccc4fef24f32c04602`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 22:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:42:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:42:31 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:42:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:42:31 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:42:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:42:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164c80380b0dcd60ea92fbd5645d9478bdfb6a0b5dfaabf0daa2a974ecfb949`  
		Last Modified: Tue, 03 Feb 2026 22:20:18 GMT  
		Size: 70.0 MB (70021714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683fafcacb39fc79aadc4581443cba2d39082186a6bc47cb84dda47eda5579c`  
		Last Modified: Tue, 17 Feb 2026 19:44:42 GMT  
		Size: 87.3 MB (87341025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba2dd0119344cbd7219f3e88527214a655faf1d6fa189f73dece05d540f5a5e`  
		Last Modified: Tue, 17 Feb 2026 19:44:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:06ef5d481226395cdd914a908a28ddc40871beb58d717cbadb7d9b2bb5071c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac97286dd83e0da56d4cd5cc37a1fdeaba3c15fa56fd86d9e5e70cab7a1335`

```dockerfile
```

-	Layers:
	-	`sha256:721ff67e0c19ec054bcb3fd26ef91e54b835efb21860e5831b24eb20c32feb88`  
		Last Modified: Tue, 17 Feb 2026 19:44:33 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:cf7e50c7fddf1e7cc634079d1d7369f94c5c00e430c68a64bf1a2b7852f0c06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328505616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c640560dce4d90503fa25d1dbefc36d1575a0cec7716b83ceb48150672dae654`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 10:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:40:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:40:43 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:40:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:40:43 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:40:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:40:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c21a9818f8ca2f73ccd29b595b5a2bc7818b3057c3895ec555bee901eb365`  
		Last Modified: Tue, 03 Feb 2026 10:36:21 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf9d9076f39b8e2c0aced7f1f28dac543d58a8aafe215df11bf80a17810efe`  
		Last Modified: Mon, 09 Feb 2026 20:28:08 GMT  
		Size: 90.5 MB (90451427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fde41aed2421b1bfa6ecab656c0c906edcbf89b7187c466f56a4a89af6490b6`  
		Last Modified: Tue, 17 Feb 2026 19:42:01 GMT  
		Size: 90.2 MB (90209384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afc5d000dbc50de69bf164f01bd763715c68520fbcf0f5f26026374bdb138e`  
		Last Modified: Tue, 17 Feb 2026 19:41:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:470689f73ef8b1ead1ad33dfca00cf04322e0e48a4b7aeaf1d1086bfcda10f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062aecd0f3e8b775e60d443c3b761611850d0301c85ddd0e0c719e812b44241d`

```dockerfile
```

-	Layers:
	-	`sha256:b099be3ae09401dfc19a83831307a6bd6759699fc8cc9097c6a7c582abea4266`  
		Last Modified: Tue, 17 Feb 2026 19:41:58 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6f4435387372f3d721559785c9f695a7bcf72b47c1ed6eb152d97fa531c327`  
		Last Modified: Tue, 17 Feb 2026 19:41:58 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:b960fd8879d343f260ba9f6a6ed272ef646f677f752d21040fe1a2a5d704724c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296465346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7fa9b9ec733968d659e1bd69c28c81248f60cbba3290b465e15f617233cab9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:29:49 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Feb 2026 19:29:49 GMT
ENV GOPATH=/go
# Tue, 17 Feb 2026 19:29:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:49 GMT
COPY /target/ / # buildkit
# Tue, 17 Feb 2026 19:29:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Feb 2026 19:29:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be60f9687e53e1d931599c2c97d67403bb6a6a87fba5a8672d8f14c72b51e5e`  
		Last Modified: Mon, 09 Feb 2026 20:00:52 GMT  
		Size: 69.0 MB (69045163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6b6bbd9c00c665dfd4909e8016410533856709507819e5042a938a46f4e345`  
		Last Modified: Tue, 17 Feb 2026 19:30:38 GMT  
		Size: 92.7 MB (92746731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfb014a138b3fdeb3157d255189d7fc0539604ba98071d8d7d1fbd3dc756e04`  
		Last Modified: Tue, 17 Feb 2026 19:31:09 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0ff47848e04481b53a0b4d800af15ce6d341af4b87b84c60018927203e12692f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a41b547eaeca6f90057f360d34e3f11968d137375c629111f79aa7d27827e68`

```dockerfile
```

-	Layers:
	-	`sha256:f82141a7ba996c96c7a8392590f505c614898692591b5268e69bbfd4240a3164`  
		Last Modified: Tue, 17 Feb 2026 19:31:09 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83d20da944716d7f3c2b24ae73d97b5b68f843bb087e25def330d418c6683ae`  
		Last Modified: Tue, 17 Feb 2026 19:31:09 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
