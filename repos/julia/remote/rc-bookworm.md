## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:9c37ed0f0f5a50db8ccf1c26b323262fe8c341a7bf8cce12e3ee06a48232e43f
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

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:b29c2c7de3317786ec5f96ad3a18a08239c4bde57326ab751a91ff03369232c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291532202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814c4dbd22f26d33d99529333c1c18d35f8f36099a0412355e667ae5e9ff985f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 26 Sep 2024 05:59:16 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 26 Sep 2024 05:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc4-linux-x86_64.tar.gz'; 			sha256='fdbd1aae595bd90f20b01cffe7ec34afcd25568b6351888065c934923ecfa042'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc4-linux-aarch64.tar.gz'; 			sha256='bc87e519a7f4d1633ca38db2b6bafd58f7025601202291a8ab6dd680101ad44f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc4-linux-i686.tar.gz'; 			sha256='dbcb66e774c71daf53d8b2582d30352c8696f05907e82b64a49754f718447196'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc4-linux-ppc64le.tar.gz'; 			sha256='06892cc4172e4e7a62051e68acd1a664da5e8e0cdd5f4902c5cad679ac27890d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b36249088c8cc5ec53f02e1abac490065d8b604fe779e22a6946178e50fc660`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 5.7 MB (5712617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fe9a286915af9f12228c32c915c92c853edd95c246a39d569697e15e7d58f6`  
		Last Modified: Fri, 27 Sep 2024 06:02:50 GMT  
		Size: 256.7 MB (256692943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e51a5972ef04068cc0eaa2bbfbf088a0a10aca7d99277e84efc1507c93b7bbe`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7ae1818acdba29fde436bb2095b83308d37636ab23dce231cabf226fe6a456a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0154ed52338f5a8e1607530bb92e161925267813b9c4da8f10ebe1645810fd0`

```dockerfile
```

-	Layers:
	-	`sha256:b962abfd1495987b9b2facefc09b5ea91237fae74b75cad0a071f81db85ea777`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 2.4 MB (2435057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdb7dac4f9c5c488da2231e1017a9dbccf0073df2be651b691b365ffea87c82`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

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

### `julia:rc-bookworm` - unknown; unknown

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

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:29ac853b7a06f49199004c5c8fd8bb554adb41ca0c7624c0e26bf3aa77d1b5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270475703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8abd705e439ab7fef7ed7d93166eb93b6d65fa1db84da0d09c85cc2675f1162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 26 Sep 2024 05:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc4-linux-x86_64.tar.gz'; 			sha256='fdbd1aae595bd90f20b01cffe7ec34afcd25568b6351888065c934923ecfa042'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc4-linux-aarch64.tar.gz'; 			sha256='bc87e519a7f4d1633ca38db2b6bafd58f7025601202291a8ab6dd680101ad44f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc4-linux-i686.tar.gz'; 			sha256='dbcb66e774c71daf53d8b2582d30352c8696f05907e82b64a49754f718447196'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc4-linux-ppc64le.tar.gz'; 			sha256='06892cc4172e4e7a62051e68acd1a664da5e8e0cdd5f4902c5cad679ac27890d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310098518356653915c2026e19bf6ca19b8bf02ae691a3ad6895e00e9c6c6173`  
		Last Modified: Thu, 26 Sep 2024 23:58:45 GMT  
		Size: 5.9 MB (5870396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a9e91f0adecca9fe83a4e7f01503fa120b621ba884ddb7a5977120eff65493`  
		Last Modified: Thu, 26 Sep 2024 23:58:50 GMT  
		Size: 234.5 MB (234460640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21088ab064846e566d5d2f8a7e4e38137298cf7716707e8f0afa65a206db3ed`  
		Last Modified: Thu, 26 Sep 2024 23:58:45 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:03975cb933513a81e24870f97e4428955019871b38444867074b50d56a2cba47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f93ef96e5c14fe56ddae86491f4e780ac18d22e820f1f32cc796dd971fea2ff`

```dockerfile
```

-	Layers:
	-	`sha256:1907d58500872e8b202ad06c1a09ccadac7870ffcfe3d24e7c360e39ac9642b3`  
		Last Modified: Thu, 26 Sep 2024 23:58:45 GMT  
		Size: 2.4 MB (2432139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7a5a60f17cea8e8089fa732270cc15a6aec51db1e5cca36683d64d903218d55`  
		Last Modified: Thu, 26 Sep 2024 23:58:45 GMT  
		Size: 17.6 KB (17650 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:d35c60192965064d94023a2029824dccd13efa56e34af401be1b176597f2a3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283883432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49dcbeb2bfc224549fb5c6fd496d7f16358a125c20006ebbb1e73bb67466b3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 26 Sep 2024 05:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 26 Sep 2024 05:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc4
# Thu, 26 Sep 2024 05:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc4-linux-x86_64.tar.gz'; 			sha256='fdbd1aae595bd90f20b01cffe7ec34afcd25568b6351888065c934923ecfa042'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc4-linux-aarch64.tar.gz'; 			sha256='bc87e519a7f4d1633ca38db2b6bafd58f7025601202291a8ab6dd680101ad44f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc4-linux-i686.tar.gz'; 			sha256='dbcb66e774c71daf53d8b2582d30352c8696f05907e82b64a49754f718447196'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc4-linux-ppc64le.tar.gz'; 			sha256='06892cc4172e4e7a62051e68acd1a664da5e8e0cdd5f4902c5cad679ac27890d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 05:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 05:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d424b429b246dcc7c2c35da69e78023b09bce5be5133a9d35a34655a959e19c`  
		Last Modified: Fri, 27 Sep 2024 01:18:59 GMT  
		Size: 6.2 MB (6247878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5cafd82d33a1aadc2e8545c98f7c94cd152e606ccd05047a480cd892f4e4ba`  
		Last Modified: Fri, 27 Sep 2024 01:19:05 GMT  
		Size: 244.5 MB (244512821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6ad90c209e26bc493ebbef999a62589b61444304ec010796fd8904568f46c`  
		Last Modified: Fri, 27 Sep 2024 01:18:58 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:00cab981688e0fdc18f372cc6bce23080fa1c8a57a210b77ba026449c2dba32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fce562431ed048de5d5420f66874178acd5198f2ffb7473989033bffc17fe6`

```dockerfile
```

-	Layers:
	-	`sha256:94934dcd55d360f5c762ca73f51812fb86653f72df5b2ceaadbac09a9e84d107`  
		Last Modified: Fri, 27 Sep 2024 01:18:59 GMT  
		Size: 2.4 MB (2439476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b11af87de74f7ca4824600a9386cd86f96cf6192dcf340b9d9a8e833a622da7`  
		Last Modified: Fri, 27 Sep 2024 01:18:58 GMT  
		Size: 17.7 KB (17742 bytes)  
		MIME: application/vnd.in-toto+json
