## `julia:latest`

```console
$ docker pull julia@sha256:584cb02c203791e0abdf7e8c060b6e33334c91c1fae493c85fde188eb1b39015
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:a86b651161c1722fac781b2d6bdc10f50e8d7bc7cd8c5cd70c7cdff5e4c7421c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325260309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a05d31d1f77b9ca31da0fc15e1806c8fa8f5bf652c91565abce69fd21d6443c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.11.6
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad65136d5342542722e2cc2a8bc8d13f0fbe029c5a7e9db78aa762a09d2c675b`  
		Last Modified: Tue, 12 Aug 2025 22:26:36 GMT  
		Size: 6.2 MB (6242669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4b83a55842580a3d07f4d76f220a6c082e88f7ab999c856e1ba16d539e382a`  
		Last Modified: Tue, 12 Aug 2025 23:21:39 GMT  
		Size: 289.2 MB (289243982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a681ef9a9509f08a3432b7d27148959ff124c1a2b16594171990a17150e5c3`  
		Last Modified: Tue, 12 Aug 2025 22:26:34 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:52cc0e57bc7a4cb42ccf746b7b77ea76e4102057778108d8ca55ed8cb42969b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fbc796de08765ca032cb9ec157b00ffc94fd2d01bd9ccde20b5e1dc249cb63`

```dockerfile
```

-	Layers:
	-	`sha256:587c63675271365885adc325605e183056d9585a89b0586369e5342f1c62ff8b`  
		Last Modified: Tue, 12 Aug 2025 23:02:26 GMT  
		Size: 2.2 MB (2239191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cf9413ec2b5f166e800c256e03795ba5b69e9cb9f4fcb0474e9227a7541e03`  
		Last Modified: Tue, 12 Aug 2025 23:02:27 GMT  
		Size: 18.4 KB (18372 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:668962478499106a93ca340beb6d6769ab762efcfe68be3d248aa2ad56792782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340904380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729190dc74a7bc279ddc0d810c260de52993a91608649636ed4d4859e57dedeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.11.6
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce42c59c1725bf475c3d149ef8a99ad51b1eb986244ea212d5e0386c9670d162`  
		Last Modified: Wed, 13 Aug 2025 03:02:53 GMT  
		Size: 6.2 MB (6152974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11be43e00719d557902ad1c82690b187961301cb858230c6e6be48cfdf01ef0`  
		Last Modified: Wed, 13 Aug 2025 05:27:58 GMT  
		Size: 304.6 MB (304614991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2551fd1bee3ffdefbb796e2373836671b60359f4fb8d8ba167c1d9d0754603af`  
		Last Modified: Wed, 13 Aug 2025 03:06:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:de8f92642dcf7538f317ed700a59166c0d5a8c55732106d664f111e39739a49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915b7521f67553f7e202e42b6ef72e431103f3005657cdc71e14fd1a3a6ef833`

```dockerfile
```

-	Layers:
	-	`sha256:c47b3f4b34fda2626e5f7649976420261d94624f3ff3c47d4ecaff55fababd8e`  
		Last Modified: Wed, 13 Aug 2025 05:02:20 GMT  
		Size: 2.2 MB (2239523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbf352b76e453c8079589c7783a62983720beda57b19dc57d90829045def6f2`  
		Last Modified: Wed, 13 Aug 2025 05:02:21 GMT  
		Size: 18.5 KB (18539 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:4bcdb08c480a5c793831f0d15198ff636e0539cae7e1900df70f3d0f925afe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275447305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4dfb8a4d0c10e1a742c6895f9787756b9ff9ae242bf82dc0d84b0c5c5a3b4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.11.6
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b959fceb40838bea3404f259ca9cf338009ef9b78f66cb0247a0893b661dab`  
		Last Modified: Tue, 12 Aug 2025 22:26:17 GMT  
		Size: 6.4 MB (6427734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3b2dfc6219d5963369f91b7104862d07590fdf33f80e252b148f5965fe4987`  
		Last Modified: Wed, 13 Aug 2025 00:57:16 GMT  
		Size: 237.7 MB (237729820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b9297a27d14787de33a2a04c2f5fd100d4e2a05f0db31c88a525bc4ef3ce0f`  
		Last Modified: Tue, 12 Aug 2025 22:26:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:60066268aae620311682d1b5974a643d8350b513cac87cf155902313a28e1297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8feee93a9e3e91680b7d163b9e5a37b271e097709054742453f0639bafef76`

```dockerfile
```

-	Layers:
	-	`sha256:886a2de10d49922a9493cff4905f1e3fa0b6bd070777d60e953935aadc8383bc`  
		Last Modified: Tue, 12 Aug 2025 23:02:35 GMT  
		Size: 2.2 MB (2236316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3b55a07882238a01f0a7eb3f47135ea2c0c4d5f0f8c55f34f6ca9c6c8835a5`  
		Last Modified: Tue, 12 Aug 2025 23:02:36 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:d37f8d64a2fef05566fdb5d54d700e5f3efbf9a75be6ec83618a481ad7817130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288908604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677d46a279e80c196806666049fc8391835859984b1b674fdeaba556d98fa475`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.11.6
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929e23aaf4ae5afe65d85efce1f6ecfba3f281ae60a557bb5e4a494cb9128162`  
		Last Modified: Wed, 13 Aug 2025 04:54:30 GMT  
		Size: 6.7 MB (6682187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a37c28ec6776cf3f4113305f694b596e979ef9cf9e3d98d2f75e00e3309d5`  
		Last Modified: Wed, 13 Aug 2025 09:08:37 GMT  
		Size: 248.6 MB (248631834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4963af2a627a89e9c14280ffb677d5aee87b86ef055b1742ded8e2b3c26c2`  
		Last Modified: Wed, 13 Aug 2025 04:54:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:3c17e20bb70d5aedc7e94af039f373363979a69f91670a3a2d7f4e0fbb340828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2261386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a439a63f9af4389ff5115b417ba424f8481f6d21d3a95c03175917320d84447a`

```dockerfile
```

-	Layers:
	-	`sha256:db20fcd53a151500e2039ee2ba3824551460de313e712fdaf4f23ef2af4cfc46`  
		Last Modified: Wed, 13 Aug 2025 08:02:28 GMT  
		Size: 2.2 MB (2242944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:864824c081825910a1e9f1ffbf504e72a62e133b3801f83a30ce97a9696654e1`  
		Last Modified: Wed, 13 Aug 2025 08:02:28 GMT  
		Size: 18.4 KB (18442 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.4946; amd64

```console
$ docker pull julia@sha256:a6ca77b846485402d9950608eb819fde3cfda919bbc6f54207182abd058303e5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3784792637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3476c17ec709837053fee107219021712ea6e966861e14786e39e0be7f59738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:13 GMT
ENV JULIA_VERSION=1.11.6
# Tue, 12 Aug 2025 20:27:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Tue, 12 Aug 2025 20:27:14 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Tue, 12 Aug 2025 20:28:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:28:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1042898b3767cfa18658c36d43106dfd885fd235a9a37b20d94db5b83621d5eb`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c36cc967029541dde2878411b74bacd9137a1726cb9723e89f7bc39c214146`  
		Last Modified: Tue, 12 Aug 2025 20:32:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db27e15a646db31132da1d269e94474027004b1e464dd96add2c12426f4cfb`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a491dcb2c710748d811db63bed2f7b0d3903b70db7cfce4505630047daee9074`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917425fa28a9788603f41520ba1e89b12fb63caa8301d5a060250ccc23385c5a`  
		Last Modified: Tue, 12 Aug 2025 23:03:54 GMT  
		Size: 286.0 MB (285955536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafd846427380492feeb94da22ba7c6739f4c2b1b95739af0808407d74bbbf9b`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4052; amd64

```console
$ docker pull julia@sha256:625447d3dde2bd9c7972879d208c9a0f1304e474077c34ccb074cf3c263abc31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567555274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7473c348a9a50005201b43a4097f500923821d90cd8da9dd6ffa74ad9b9cf5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:31:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:31:53 GMT
ENV JULIA_VERSION=1.11.6
# Tue, 12 Aug 2025 20:31:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Tue, 12 Aug 2025 20:31:55 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Tue, 12 Aug 2025 20:33:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:33:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8663c4d2d36718aae1a419811e3600ed879d9244dc2e62a0de02522fc61245`  
		Last Modified: Tue, 12 Aug 2025 20:35:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcaca73cdc24156b5bf4135eb5726487883d8e47fb96541f9e68c05d0df559b`  
		Last Modified: Tue, 12 Aug 2025 20:35:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca570c3f6615c5bd81b96869e558a33852ed19e96d5b9d70a12b218b739cbc6`  
		Last Modified: Tue, 12 Aug 2025 20:35:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71971d011d5acccae7591a17d16a43c9c9e1c1b75eacf47b43ddb4ba0c8d8a58`  
		Last Modified: Tue, 12 Aug 2025 20:35:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368098632db31528abe917b1e3b08f8d7e01930b928be89059c13df00977b956`  
		Last Modified: Tue, 12 Aug 2025 23:04:43 GMT  
		Size: 285.9 MB (285856859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9f044d4f7b2ed5beebbd8ef7693d2c740455ab29f250364880b8808e57cfc5`  
		Last Modified: Tue, 12 Aug 2025 20:35:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
