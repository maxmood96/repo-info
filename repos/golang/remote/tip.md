## `golang:tip`

```console
$ docker pull golang@sha256:e9bb60f533d0cc459a348f89e1d373fd7b8f01afc09dcf5ffc4bd6f1e906018b
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
$ docker pull golang@sha256:5ff212d5f15fa88aec6f1d5ff5025a80b1c3ba88110882388fb48cf13bdaba0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358480764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cde1c312053dfe45acfca882347291d697b774a63fc97e51bf3e171b2ab6fb5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 08:41:29 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940879ec2f8965980bfcf5c76f0245af842a19359fc91b29d9bda2bc8d5af574`  
		Last Modified: Sat, 15 Feb 2025 03:39:47 GMT  
		Size: 92.3 MB (92331738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f767e601eda3139d3a2c86388748ee052ac66ea4515fdb8e54673dc9e44217`  
		Last Modified: Sat, 15 Feb 2025 03:10:47 GMT  
		Size: 129.2 MB (129216535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d752ceed08f98297e8af393ceb30c5caeeca97937313814223652014719e84`  
		Last Modified: Sat, 15 Feb 2025 03:39:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:5e40735fea1779f34515d0717be563a39bfa86ced7c4d8479adeb4cd3a992f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10304520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b77a8fb22fc3137a5ade5f0434f1f150c4507c4641c360c8f89c4d0a0b42a`

```dockerfile
```

-	Layers:
	-	`sha256:1403682283494c8c2e35b911988528820d757ab78ac931f19d04cec7b16d74f9`  
		Last Modified: Sat, 15 Feb 2025 03:23:21 GMT  
		Size: 10.3 MB (10276857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4290886c04423f828a9587c0a9aed8b26ac1bb16b23ea8dae9d3e0bc98eafb4`  
		Last Modified: Sat, 15 Feb 2025 03:23:21 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:7f4d1f99da390e69e29a15fd157bcd46192c3dfedc1c5064b21fdc17a3bc7c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314483609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940fb4bbf75efcd9f03ff6218a6e9a9e7cff065f58203f2232539f064b346955`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Wed, 05 Feb 2025 04:00:39 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495fc29bc2ed109c3df977c363822d9e02d7dfbd66c67a0ed2643726ec489e4b`  
		Last Modified: Wed, 05 Feb 2025 03:31:27 GMT  
		Size: 66.2 MB (66183449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bce9909702d68cbcaa8d6736165483e5a988ace20a7429491fd9459c92058c4`  
		Last Modified: Sat, 15 Feb 2025 13:09:03 GMT  
		Size: 122.5 MB (122516719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fdf8e1711a1f06741509a854b457e18a7d5372d384b874e12856f875935c54`  
		Last Modified: Sat, 15 Feb 2025 12:31:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:37dd1523b33b9241c751e60d509a92eb996bdabe569caec281d760bcdb302a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8bf2c74fba1dfdfead290012776d18c7e6091895f2db4b0f7fd40d00d36c6e`

```dockerfile
```

-	Layers:
	-	`sha256:fab97b5afa9c4df3202a35d3c2d67fdfa836ae3cda538f52f74bec11b4214b71`  
		Last Modified: Sat, 15 Feb 2025 15:23:21 GMT  
		Size: 10.1 MB (10085179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94e9342144e201140bde526843c4832b7f26b2cada82cd450667001cec1419cf`  
		Last Modified: Sat, 15 Feb 2025 15:23:21 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7db7558a51fe606515c265dc8c6ccc2d6a852f70f1bec33f864c814542181b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345500051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c1b51d198816029e76e8a027defe5260e25d10d40c40f15c262edb574a2ef9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Wed, 05 Feb 2025 02:21:14 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac3f7121b9240f61d416dba8be2c96da4ffe9fe1f25831725071946bb7fc54f`  
		Last Modified: Wed, 05 Feb 2025 02:18:50 GMT  
		Size: 86.4 MB (86378491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905748308911592ab8dd35e81623d80a35a86c1f573f4146926a93bafbba078d`  
		Last Modified: Sat, 15 Feb 2025 09:11:49 GMT  
		Size: 122.9 MB (122858916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6b72d8784a6a7316138b68041826e2cf7964c7144b8e3173fa5106e130065d`  
		Last Modified: Sat, 15 Feb 2025 10:18:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:aa12c4eac423a5da6dafa86cdf63cd77cd9b561f67a6986ae2fa580fc27d5552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15854a447f3933c0782014c70e71737bde7e9137005129c55421cad05ee2cf98`

```dockerfile
```

-	Layers:
	-	`sha256:8a83681e4a92972c2220317e216b9e01a67f6102bdb56e92e1ef16a2471d22b3`  
		Last Modified: Sat, 15 Feb 2025 09:23:21 GMT  
		Size: 10.3 MB (10304704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:114c5e65f24ea41a4aa7745ed9c12eb2a729d19fce66844ce32f5a42dfcce44a`  
		Last Modified: Sat, 15 Feb 2025 09:23:21 GMT  
		Size: 27.8 KB (27822 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:031143276d496e0e295f7491cb572d6b2f324d9edda39b50cdfd9722a08862ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.2 MB (356211065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f6bfedaeda7cd47f8bb558a5a3726a808b4b575e12d4f24ff36e0fb648a9bb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 10:18:57 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 09:42:09 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670168f142dd09e49c51e3eb6f4e90e3e85198f357aa8ce88f9d74ab8ed54cb`  
		Last Modified: Sat, 15 Feb 2025 03:48:02 GMT  
		Size: 89.7 MB (89744368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2ede4bc0ff1c223f32b8ba810862b4e27669e273d5c1e6c5993b5698ec335`  
		Last Modified: Sat, 15 Feb 2025 03:10:29 GMT  
		Size: 125.9 MB (125872820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b104d433eae0d4b75cfb1bfe3daf6d336b5c227faf4f40b366f08653ed00da`  
		Last Modified: Sat, 15 Feb 2025 03:47:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:9b694f6fd3d58e5ce8266f16be484011b78eb76da7797a964b03a994af2951d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb66e317cbff415bad491d5e83b8559749a753469e9daae9bf2aa5e6162d8eb`

```dockerfile
```

-	Layers:
	-	`sha256:19aa4f99bb6f78f02ac1a7222de8206c5dc695fe6294816cd692d5d31cfa170c`  
		Last Modified: Sat, 15 Feb 2025 03:23:26 GMT  
		Size: 10.3 MB (10256928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715167e385f6fd1d9d4d23d739925b20751a1ccb59f0303c73d05a2b932a29d1`  
		Last Modified: Sat, 15 Feb 2025 03:23:26 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:ae983c30b901f8601c8f701550da876fad4b1673d73dc66e072994ee5e922d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324820830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b942f1f7512bda7ac634a313bf222620cbb6aa77d736035c2cac19053b6a49`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 06:00:54 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7faf65582b7e0fbb4eea14df7537078630b3bff0936e1fc964a494519326b5b`  
		Last Modified: Wed, 05 Feb 2025 04:01:51 GMT  
		Size: 23.7 MB (23652224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12393adfa37a97fbcfa8d29955e04828c6bd657b4d83082cf837413910af04a1`  
		Last Modified: Wed, 05 Feb 2025 10:04:59 GMT  
		Size: 63.3 MB (63306362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad120905a0f60eab99f4ab665554fe053a33e4959cc10d9453a31e032d47eea`  
		Last Modified: Wed, 05 Feb 2025 09:31:55 GMT  
		Size: 69.9 MB (69897902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3349bc8e4fca6174184ff162599f31cd5026fc2feffaeef6cc5e37bcc29536`  
		Last Modified: Sat, 15 Feb 2025 02:52:11 GMT  
		Size: 119.2 MB (119206384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12e8cee6ec09785473e5868f67310315a1989c5fffad7285345f5f894aee0a6`  
		Last Modified: Sat, 15 Feb 2025 03:23:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:82b444ce79e4a4c3f79db7ebf3564fb1df05efd048ac3d4195e70164eb475ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3747a3d7ab5edd53077ddd2d227923c0b47fa9856d51fe1c38126c3719d86f`

```dockerfile
```

-	Layers:
	-	`sha256:aea47e0b13ccddd41c90c95482ce7c817cea27946cc22c2d60bcf1b6bc5afb8f`  
		Last Modified: Sat, 15 Feb 2025 03:23:30 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:53903b35c52fbfb139928e13669d77a8299fcffc680cecee0cae46a4f02af712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362572747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1941ae5d7410c9112a02228de113062022cda8674b107c93d3d82c73e753e8e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Wed, 05 Feb 2025 00:47:58 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 18:00:23 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625fd5449702b0d8fa61c0c059218a9f27e0ee625784b4c5b5b74adb48030d7`  
		Last Modified: Wed, 05 Feb 2025 00:31:34 GMT  
		Size: 90.3 MB (90319530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f05ebd2cfc5d58a8a74d541592f939ce44409deeab829fb1fdead8865b10f81`  
		Last Modified: Sat, 15 Feb 2025 06:09:44 GMT  
		Size: 124.4 MB (124379795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd2834a300efc29f6a5c07befeba430e521fb281d19e7a961c7b820d418356`  
		Last Modified: Sat, 15 Feb 2025 11:27:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b24c1364922006b30c44e9e111e3e8c8358cb9acfcc65aacd77b441e597c2eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a66f051a7d5fafd2e2e2b76a1c746a2f14b2c89b20dc12f6392cf1c4b993e92`

```dockerfile
```

-	Layers:
	-	`sha256:905530ca934f722cedb903ecb6338822854cb1f59b1e74d48a021b349020a823`  
		Last Modified: Sat, 15 Feb 2025 06:23:22 GMT  
		Size: 10.2 MB (10249556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6115482bc4d0bc817273eb6338becdf6af0cb1232e3ad03c3c9ea805e1f98c44`  
		Last Modified: Sat, 15 Feb 2025 06:23:23 GMT  
		Size: 27.7 KB (27720 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:c6878c6b8793672b831317c8b22d3a6300e5c44ba3f4f1124326cec453190dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330276178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed508939ea93c9e7c903873cf4360ae7df4efb704416c6125a22d80d9418f4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 05:09:29 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Wed, 05 Feb 2025 01:13:32 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Wed, 05 Feb 2025 00:15:03 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622f31351dd9f8a683608361b61d9b52cab45259b4b66a1cbdd57f5fb617cfcc`  
		Last Modified: Wed, 05 Feb 2025 07:02:31 GMT  
		Size: 68.9 MB (68907533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f67487422a2fca86e0ab6fdcaa52aa1779b4a197c62c15e515f5ca0841f8f9a`  
		Last Modified: Sat, 15 Feb 2025 08:10:19 GMT  
		Size: 126.7 MB (126679962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e54a28605d3b15e8f45b6afc44f97fe2ef180646232241343decedf77160589`  
		Last Modified: Sat, 15 Feb 2025 11:27:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:8772b58f65cae6cfd4987514c90a9a7d96e87f914d0492b2e0fa55fab498fe1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10140500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719295cd5432d7f353c6c159978dc0e8ad39c31d64aa7e0cbc7ed75290fc7209`

```dockerfile
```

-	Layers:
	-	`sha256:b47d10861d54dff08cfef361c7f5a508b164201da2cd5ecf0906f1f111cb0c37`  
		Last Modified: Sat, 15 Feb 2025 09:23:36 GMT  
		Size: 10.1 MB (10112837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ca49daf43caaaa66d4c69308577595135be057c781a93d55964844d12f3767`  
		Last Modified: Sat, 15 Feb 2025 09:23:36 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
