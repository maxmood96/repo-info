## `julia:rc`

```console
$ docker pull julia@sha256:2e8f32d92e5f668b56ecd186c4950ebf48548eb0d2528ac72065fb10c034c44f
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
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:984e02521046440c34b74a87bae3fdaa2aa66f8fb417afda6247483b371a953a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290028345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8db115f7fa643333166c6f51b5508943fd72a30c88840c9f061cf182cbd8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2359b8f05100439523ae7537757e545d1043aed1fa1ca0f7571fb5e1062ec934`  
		Last Modified: Wed, 04 Sep 2024 23:10:36 GMT  
		Size: 5.7 MB (5712645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4444381f0e929a1791d376893d979e482592dd9fefe8846c512e83d6c20e5`  
		Last Modified: Wed, 04 Sep 2024 23:10:40 GMT  
		Size: 255.2 MB (255188843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1accaf488e2e8ba55cd914aa6357299c54c73e108a72c7d424f17ba47461ef56`  
		Last Modified: Wed, 04 Sep 2024 23:10:36 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:0595f9354f0e6f301df9d68cf0effc509e0c45b805ac2b288f3a44069d3f35a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5af87addee8808960fb8579b5edf888ea688050f50c67ce8c1c806c5767835`

```dockerfile
```

-	Layers:
	-	`sha256:5700f19be56ef02e4ec238e9f3e336164d3aea9f0a28a92a271abb462ffc02d2`  
		Last Modified: Wed, 04 Sep 2024 23:10:36 GMT  
		Size: 2.4 MB (2435044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2e088943e3d17fd9bb238e5bd7c0a66c5b8fcd67b57613b2c23f4bd1bfd3dd`  
		Last Modified: Wed, 04 Sep 2024 23:10:36 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a0e5204514587074d161c40ee909e259d7bba4609c32b960044e9b8408faf377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288123533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0968b80ac2161ca9a6d3dcf77ebcaf89f003d0778e7d5fd4517c35885eaf5b31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eadd28d9232aec1a98082e8b5fbaf4ce4cb0daa4e2acf3ab3e60d47db0acd47`  
		Last Modified: Thu, 05 Sep 2024 12:21:19 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5cb968d67de57282a69b0c7e3830ecc58b067168d1cb1f3e98e97062793865`  
		Last Modified: Thu, 05 Sep 2024 12:21:24 GMT  
		Size: 253.4 MB (253429426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75acb9aedb25408bbeb6b704db9f2dab622a3361d9d8ae654e3a47895d0136f`  
		Last Modified: Thu, 05 Sep 2024 12:21:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:3f73466585df5433b8054853d40aba4e711fa3beb02e936fdba1a632fbae9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9671ab646aa5e4799d986bdc497b42a496efe999ae752150dce7461be716f2`

```dockerfile
```

-	Layers:
	-	`sha256:9fa5f47032f0390a0f18a6c4f4a900085b1ebb48293ff1d72d9e9019f497464c`  
		Last Modified: Thu, 05 Sep 2024 12:21:19 GMT  
		Size: 2.4 MB (2435342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721ccac19b67fb880ebb0c1cd312a627436a23a079df7b5b0d5d5b8610b5b605`  
		Last Modified: Thu, 05 Sep 2024 12:21:18 GMT  
		Size: 18.0 KB (18024 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:923787456a144342402d59c9b028c32b98e935bb4e9dfd71dc01abd259dcc45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (270001676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b0542ed631723651e5000cfd8049bca38f80214accc104aa0c0d96b7a3cfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36da03f12f454b39c2b1cc23d0eccb55af1c15931e9d38d04c07aafa82af1b30`  
		Last Modified: Thu, 05 Sep 2024 00:08:11 GMT  
		Size: 5.9 MB (5870531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e144f7d35b0c0a71f8783bf7f9ac1a53a0195c13de360ee4371aa4406def6d9`  
		Last Modified: Thu, 05 Sep 2024 00:08:17 GMT  
		Size: 234.0 MB (233986482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46606142f2f7324d716128921aa1d3a8df1d998b6a6f83502ffa339cf4af829e`  
		Last Modified: Thu, 05 Sep 2024 00:08:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:11fef755df3904fb545ca30ac014e886ea54ff18d86c6a837d1cf03c4ffe8c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947edf678e76e2dddbbd5eba3bc8e2724b331dabe4ac7ac28297b0a1148c9272`

```dockerfile
```

-	Layers:
	-	`sha256:bfa6d99ff5da990465570e9c1e0173ecda252a0c752899071300caae14936f0d`  
		Last Modified: Thu, 05 Sep 2024 00:08:11 GMT  
		Size: 2.4 MB (2432126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e7b57ea77af207b09887492a7ae39287fbe5e83f6ba0ca38e74366b867a8d9`  
		Last Modified: Thu, 05 Sep 2024 00:08:11 GMT  
		Size: 17.6 KB (17650 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; ppc64le

```console
$ docker pull julia@sha256:0b35e7859351f10c04253439c2bfc42807bab8ec327eefe068233e0c56e35b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283380062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32cac01db8a2e88e550b5b161931b3b382a16a793198eb8643c0dd57fcd74cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70b3d4701b0d2614418e2b9751c16886e5d687e69b51c3e5127a60824147119`  
		Last Modified: Thu, 05 Sep 2024 00:34:49 GMT  
		Size: 6.2 MB (6247900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f0b4717eca89e7ad9a8ed876836ac5c96d12857135e535786e7323b739a2dc`  
		Last Modified: Thu, 05 Sep 2024 00:34:55 GMT  
		Size: 244.0 MB (244009430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8303c1bfe7e056c3d96223eaf74287b260583fcc059996a19c65d08c8d21d51a`  
		Last Modified: Thu, 05 Sep 2024 00:34:48 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:b5983532d3dcf9d04651e408787af98fe9ad48c515625882b526b2d2fcb47c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78806d8c12d82eba77826158eb8339d4a58400659397333685b4fd85b08c912`

```dockerfile
```

-	Layers:
	-	`sha256:7e3d3bedd820c6554611ac95f984c994d2349425878b9a6a3b14078be2888a08`  
		Last Modified: Thu, 05 Sep 2024 00:34:49 GMT  
		Size: 2.4 MB (2439463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c0f1df436dd8d6b55ad18ebbecbeabc95522ff1478fd8245502d78da1cb7c7`  
		Last Modified: Thu, 05 Sep 2024 00:34:49 GMT  
		Size: 17.7 KB (17743 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.20348.2655; amd64

```console
$ docker pull julia@sha256:e0d4f45b321751c09c6c88c51f09e70583b6de82ea3f532909984c377554d15a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2393920065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82309e195a465d7f44b29ced1b57fc0fbef25db259e8b0a8da42af49d2909d9b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 27 Aug 2024 20:04:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 Aug 2024 20:04:40 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 20:04:41 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc3-win64.exe
# Tue, 27 Aug 2024 20:04:42 GMT
ENV JULIA_SHA256=c8cf68a67216205306760cf5c0adbbaa281a859a61483409e9320b0e8c8ce605
# Tue, 27 Aug 2024 20:05:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 27 Aug 2024 20:05:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1ec36eed7919deb97704658849dfc031f34d2369f05b10e9b9d3b63dd89dc0`  
		Last Modified: Tue, 27 Aug 2024 20:06:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e88df49064c34265f709d07ffae1b96143fd8f6e00f6916386785b838155ad`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd37384f48b942098e55f5d2fcb3232783393a4bdd92eddfee327fd6ec8bf11`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e730dad64bf037b7a7f0a3ae8692c551860ccb8b971e7cadff3204eb3fc50b`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b37702a0f31e4e1096e8f384cff63773ea93abbfbffc2c3dbfdc2a44e1bb71`  
		Last Modified: Tue, 27 Aug 2024 20:06:31 GMT  
		Size: 252.1 MB (252148644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee05a32a382dbae44aec3a5d8a883f81403eba80e9396c99cdf9f834fa75d2a1`  
		Last Modified: Tue, 27 Aug 2024 20:05:59 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.6189; amd64

```console
$ docker pull julia@sha256:e87f65e4ae843949fdb7b111836aa61baa9be549855b5547b89f0f6b6b96df80
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2497474476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bdbbfce3254360fb6216ee173a0d386973e6452a5ffa9546aacfaa06549c97`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 27 Aug 2024 19:56:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 Aug 2024 19:56:03 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 19:56:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc3-win64.exe
# Tue, 27 Aug 2024 19:56:04 GMT
ENV JULIA_SHA256=c8cf68a67216205306760cf5c0adbbaa281a859a61483409e9320b0e8c8ce605
# Tue, 27 Aug 2024 19:58:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 27 Aug 2024 19:58:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e41993097840a6f84ef1f126e6db081e1a8ad55f7f89d4b157382cde7a180fc`  
		Last Modified: Tue, 27 Aug 2024 19:58:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0115fd5fa2c2d05059d08ecaabb6269d74d6d2c4b5860f85c7c8e5481f29be6`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c12cc15a7f0bb45833f020c942e01d783cee0547462f94ad360e05e96e79c2b`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5d1e2c8d818160dd29c0e37dabc52855165e6d35c6732f5a686adefaeda787`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76898a9dd96fe3582db7c090ba6f3eadd4f8198f89a681311600dc65a6cdfd60`  
		Last Modified: Tue, 27 Aug 2024 19:59:20 GMT  
		Size: 252.3 MB (252264784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c691d0511554e576cfad409beeff1511f20ad67e774025923ff6b2d3752c46e2`  
		Last Modified: Tue, 27 Aug 2024 19:58:50 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
