## `julia:trixie`

```console
$ docker pull julia@sha256:75a6de097ec10fff0ce6aed8fda54b0e5876f89527f981d30fcdf0b981231806
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:trixie` - linux; amd64

```console
$ docker pull julia@sha256:8a43c035d43c7629dc8631304543fbe0b5059dabc7e6fab1831666b69ddf13e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325260729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c796945987f46381a223b4b3f147bbb2a81ee38d2a6be58c6c2126bebe328921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cf7cb71f165e5fcbef025e187c585e15274f8bd86895c4a41684dcbbc67a11`  
		Last Modified: Mon, 08 Sep 2025 23:19:32 GMT  
		Size: 6.2 MB (6242735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3016f121915f685e22eecf61a4116a161418634165b60f917b09261b6127ff98`  
		Last Modified: Mon, 08 Sep 2025 23:19:50 GMT  
		Size: 289.2 MB (289244127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc70e11ea588702fd7de8646d68d3e5f86acedff1bb9afd7707613b81fa179f4`  
		Last Modified: Mon, 08 Sep 2025 21:35:06 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1ce398e92621ab24804246664f02ec817724850211d71885b9c0e7e19947e828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21eddda5362a0bfe3fcd6821c809adfc8739a7bf89a6a8d2898ed19ce8e6896`

```dockerfile
```

-	Layers:
	-	`sha256:df492084abdb1ac4db29f95ea77b84d5f764428274948be67b9b341dc20e7231`  
		Last Modified: Mon, 08 Sep 2025 23:02:28 GMT  
		Size: 2.2 MB (2240039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af37df0fa80434ab1bfa8da4b161bcb8256805a41e5656ffe314914ae9bbb35b`  
		Last Modified: Mon, 08 Sep 2025 23:02:29 GMT  
		Size: 18.4 KB (18372 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aef3d61fa8ee2e60985241383bf0245d9851cc7e27f5b13f912c9b1f7c26ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340905160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8134be7e8ae2d0e13468aa0fcc66a92ee5354d346305e0ba0daffd191feb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c718b1d20deebbfcfb9c6e8f26083fd96cbc856ddcf7ae8c49a7b885be56b5f9`  
		Last Modified: Mon, 08 Sep 2025 21:20:37 GMT  
		Size: 6.2 MB (6153088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dd3b126970e5ed898a0d6a9f177e2fec84323c9d95887b867b315392e66907`  
		Last Modified: Mon, 08 Sep 2025 21:20:43 GMT  
		Size: 304.6 MB (304615073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc8822324b3d4c6e25c53dad2c72185da44a1d21e34b857412fc755f89dc91`  
		Last Modified: Mon, 08 Sep 2025 22:04:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:c6a7cd259c802fbc94647e7853649b8ae516d2ccc3f6af68b67aad419da376ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cb2295f2dff21657a9e3bca9347bd890987e100cf175df546a246bee14b4a6`

```dockerfile
```

-	Layers:
	-	`sha256:b50d6420b23cb2a6a2ac5917e59ee7e36eca8080f399fc9563c37754ede451d0`  
		Last Modified: Mon, 08 Sep 2025 23:02:33 GMT  
		Size: 2.2 MB (2240371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac2dc51ac9a142a5a27d0400114b105564ca352a140b530ef91867b99bf6125`  
		Last Modified: Mon, 08 Sep 2025 23:02:34 GMT  
		Size: 18.5 KB (18539 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:f7df88ca7e3dfed586774a7d4e3ee802a722ef7272c055eea6919eca9af10d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275447779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901177a5999f0b5cc75c1a5d279a0eefe51e7c4bf3e3a78a6377f846a3c01fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9143bc0fc056ef4e07800af81bc06bccc5a215ae44b2d242ae1bc1ecf822a532`  
		Last Modified: Mon, 08 Sep 2025 21:13:39 GMT  
		Size: 6.4 MB (6427768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a7e8e290383c87806bd1ad1c98c48b8cf32fe08027ea55952585d120614b0c`  
		Last Modified: Mon, 08 Sep 2025 21:13:44 GMT  
		Size: 237.7 MB (237729861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b322453457c8561bbf296cd53942b268449a70284ef1e933a331be0d6f4403a`  
		Last Modified: Mon, 08 Sep 2025 21:31:00 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2909c70b7988db57be461b8df3ee700c4a473fcb748f5346a0e9fa0c99b85dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bb51a63ec2c51f631109a871455827c49a348b5ab4d7cae63a307bf6ce01c8`

```dockerfile
```

-	Layers:
	-	`sha256:0078204c6c0f388732fb338a55a824c6c6860ae29600fbc6cee628cde6d5546b`  
		Last Modified: Mon, 08 Sep 2025 23:02:39 GMT  
		Size: 2.2 MB (2237164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392153a7bbce6d318003d6456c7f6148d72ddb1e1e0b71aa7aac98d9103e6359`  
		Last Modified: Mon, 08 Sep 2025 23:02:40 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:6a7f5e2b5f9c43b8ea6023df4c46edaf14dbc6d3f40562545a63a2f32316c06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288908835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71bf74297b3f4a3318d9da6059185bf2628cc8f905687597f8de412cd4b462c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafa9b90e5eca4b29c8862f42898a74352cd1ae12381a78a307fc93033690fb8`  
		Last Modified: Mon, 08 Sep 2025 22:27:54 GMT  
		Size: 6.7 MB (6682195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee1c1a71e70c8719aad4d71226790fa42c42cd8647b4f3cdf9e479d5ebefb08`  
		Last Modified: Mon, 08 Sep 2025 22:28:16 GMT  
		Size: 248.6 MB (248631918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146d92fa4e6d41fd4e3cedb3bd316cb49ece146226eee02952fe71ca23d67966`  
		Last Modified: Mon, 08 Sep 2025 21:59:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:854b0d49003d247fa6e6826b335950732803c71f901c66b36c0dc83fd0cc9e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2d243dc768eb51115ac15d4c8f02f7256bf5becfaf4eefc10e29c744d33ede`

```dockerfile
```

-	Layers:
	-	`sha256:5a0b14672322521129557c0798f48c92ae9f850692a38ed66d7b08dfd4f84fcf`  
		Last Modified: Mon, 08 Sep 2025 23:02:46 GMT  
		Size: 2.2 MB (2243792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0001706be40b7cde1d1c988f7a8d8ebeb0741d9321c63c80000712b6664335fe`  
		Last Modified: Mon, 08 Sep 2025 23:02:47 GMT  
		Size: 18.4 KB (18442 bytes)  
		MIME: application/vnd.in-toto+json
