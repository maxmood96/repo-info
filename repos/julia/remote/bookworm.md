## `julia:bookworm`

```console
$ docker pull julia@sha256:ba759d544f2cd300007fcc834c33843d93aa7169fd2864717b032a1942be1f52
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

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:307e5b235be04c2d0817cf5f1c628ffaada5dcccbb8b637167de45daa135cc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323158758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8479d144aff1f4e40126ecf80623b7f0cfeb697cff04356daefaf1bdea8dd5a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e58055188d35803790ee04d3f452522402826a633a2dcb51ef786fbef142b5`  
		Last Modified: Tue, 12 Aug 2025 21:11:35 GMT  
		Size: 5.7 MB (5716148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0cfb149b0760003b05807215ab595f693bf3db39eb264165e60a6be1ae2049`  
		Last Modified: Tue, 12 Aug 2025 23:45:17 GMT  
		Size: 289.2 MB (289211984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c620eb37d7b4bef2e75a2b2598f8195b5ef70e676b57a9b353d0aefae2a7a2f0`  
		Last Modified: Tue, 12 Aug 2025 21:11:33 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f4f4cc9dafc4a79cb5c5979063d5ec8224b2812b3f2dd41ce259b0e891db5a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8d41fb45f7f483f8b8637d3d0fad1bc36d992f3f806086a93e660205cad25f`

```dockerfile
```

-	Layers:
	-	`sha256:b5cfcf57e70d6d7318f67db1d656d4409319c9a596973aba7423c30450844c2e`  
		Last Modified: Tue, 12 Aug 2025 23:02:34 GMT  
		Size: 2.6 MB (2566741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afad82169e4a31e2c1a2cd4bf52828909030dc572cdf8dcdcb0925f450c350b`  
		Last Modified: Tue, 12 Aug 2025 23:02:35 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:eaa61e62b6c3f10d54485405f55876dc54eb3a2c72b5a40e340a2307d9982065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338232079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf837e655daef180b161ccba1e9b9d86c9cb0b90d5b76c3682c06ed838c2f434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83861b6e67c998bbf64b5a54d4638f4c3566a6fb36b6f57b01adfecd5585320f`  
		Last Modified: Wed, 13 Aug 2025 06:19:50 GMT  
		Size: 5.6 MB (5560846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5a67f47dbcaef4afa48a93dfdad0db9ce579e61319b63e6d8dbf0863361153`  
		Last Modified: Wed, 13 Aug 2025 08:41:52 GMT  
		Size: 304.6 MB (304588860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a4e854ff9b731f47ae76db8031b794e237d70f2ac8ab23a894fcd3f073761b`  
		Last Modified: Wed, 13 Aug 2025 03:07:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:6a56e760241b423753cc2e5bcf1f43b383dd4913be98e3578b6f15801b2e0a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5437916c6b0107c33aff5477909eb6a3de28a52595789fc83193cb4efa5f84`

```dockerfile
```

-	Layers:
	-	`sha256:b54b99b542ad461aed8234726bc1c1b820624862ae22e5b50720fe788abd3843`  
		Last Modified: Wed, 13 Aug 2025 05:02:27 GMT  
		Size: 2.6 MB (2565846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d02ce937c6d32101c6a0be65425b3b221b3d753f2541426cf2b7e1d2365546`  
		Last Modified: Wed, 13 Aug 2025 05:02:28 GMT  
		Size: 17.3 KB (17348 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:aaad0159957c096da0e68d8b53c1fc5a04b63ea93f0159161b59d674603f85e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272780062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae30d6035a226eda1cd2f937fe966364463fabf473c8654a918d182ab73314e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddae20e2184c07139ca014cfb9fcce90900752044f668a68dab41ee12729eb`  
		Last Modified: Wed, 13 Aug 2025 03:24:18 GMT  
		Size: 5.9 MB (5877781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ac49b4f760741be5b831141e2d75ac3caecaf21da187d07ba82e41f5402f3`  
		Last Modified: Tue, 12 Aug 2025 21:11:01 GMT  
		Size: 237.7 MB (237689305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12026cf25f2afd8ff39ecae53c1d4cd38317122890834d226b3deadd399c4439`  
		Last Modified: Tue, 12 Aug 2025 21:18:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f1a9259dbf9099810be9667c20d980d9766738ca7196bd8e8fac7358c322dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93d18d802a23b8b0bb549ae10ac49970a3a2c5c33c8d8c69bfc035362309e6f`

```dockerfile
```

-	Layers:
	-	`sha256:b1cf3d58705f5dfc63a1877eba39fc24ad8fd9ed8acff9bef58dc37c52b3081f`  
		Last Modified: Tue, 12 Aug 2025 23:02:42 GMT  
		Size: 2.6 MB (2563868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66bf9a53249efec352b76865ec05dae4600e5978adc16fad15cedfe2bc6fea27`  
		Last Modified: Tue, 12 Aug 2025 23:02:43 GMT  
		Size: 18.3 KB (18344 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:e019d6b4532811b5f3b19440e01821cbf80160200b39fbb00d143ee67ffaa9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286926234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31c10e9d919c3ca1405cbbe4e6e5ff2c57f85ce4d263694d7d7477828d1dc20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f3260a55ddc3e81aef3b818409b8e38e7f09d8d1fcd50b9da9fae3518ef9f5`  
		Last Modified: Wed, 13 Aug 2025 04:56:54 GMT  
		Size: 6.3 MB (6256087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1b1082a1c73f357268048777ee7b52a997a5b9df7c031e09939ee225de72d3`  
		Last Modified: Wed, 13 Aug 2025 04:56:37 GMT  
		Size: 248.6 MB (248596354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bc93ab36bb9e123112ea184ca2e07b763aa19d35f1cd7b8daa880164d7fe08`  
		Last Modified: Wed, 13 Aug 2025 04:56:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d09b9919ea9af2a673ae25e3c2ec766cee8edf682765c9b8e377d322a2eadc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2587375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3b061676b9f97aaec9b1f5144d67c9ad88439ab12c9d1c3ba8ba8df383c8a2`

```dockerfile
```

-	Layers:
	-	`sha256:6c9daa969876e07f83fc06b41d8dff7dbfb52c29230aa00d02010450b28c01b5`  
		Last Modified: Wed, 13 Aug 2025 08:02:32 GMT  
		Size: 2.6 MB (2570099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e5ee1145556687de5f27362b4e29e5d0cf3e06f57e851ff8f4ed565c426040`  
		Last Modified: Wed, 13 Aug 2025 08:02:33 GMT  
		Size: 17.3 KB (17276 bytes)  
		MIME: application/vnd.in-toto+json
