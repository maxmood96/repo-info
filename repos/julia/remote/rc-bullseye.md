## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:ce7fbd41bbdcc575e395ce0b7d3b72eb9f7f537998db64cac9504f17efe4feec
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

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:9d371117fa115d4917ebaa6f90395d142d74a98208a0eaeb0abfe12b31155de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290548040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a209a6d2a71e3c3a4932a52de1b27a4a8a7a234362a6bb829142f2494ae42cb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
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
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de507441433be8d1b778c813b378d75c2dc8dd1c84ba242c1845c677e967c10`  
		Last Modified: Thu, 26 Sep 2024 23:58:47 GMT  
		Size: 2.4 MB (2426565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9563738a4c835572d89b377cd687b92457528c884fa715809399b6a5d70096`  
		Last Modified: Thu, 26 Sep 2024 23:58:51 GMT  
		Size: 256.7 MB (256692425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ecc39e4388c5daeaa06da0e2f06635e67c55fd874e8718fd6e9671c1e7ef76`  
		Last Modified: Thu, 26 Sep 2024 23:58:47 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d9bd3552d9688c2419f4c2e8863e38cc213a4941df0fa24f641a55860d49a388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d47273c6f47b214a46ac2d23c1e51c8060f71f4284fe6bd6c1e7adff2b45d3a`

```dockerfile
```

-	Layers:
	-	`sha256:1114a986aaeb756948ff8c1a993438f68b844febdb89063e29129f61c2388ac4`  
		Last Modified: Thu, 26 Sep 2024 23:58:47 GMT  
		Size: 2.7 MB (2702858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:720c18c807dcc6e2c6a14bce0084cb8f8ccec6d202a988ae40ee5f17c0d0b167`  
		Last Modified: Thu, 26 Sep 2024 23:58:47 GMT  
		Size: 16.8 KB (16801 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e6ff1215e453ebea51e0ab9330fa95e535f1ae256201247fe9ea7eeee74d7b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.9 MB (285918965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce11e6e2b53b057ca16db33dfc9b1420a25ac9f72fe13d8f6e0248dff91a393`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
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
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa630b71e57d93c6c4a298a32f8abf58c36a28a92b39609f86ee56a5c299803`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 2.4 MB (2415117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820d4fa50588fdd9f70ddc85b2cdb4fb77e6938ae21ed0c34bbb8ad7db3f16b5`  
		Last Modified: Thu, 05 Sep 2024 12:22:48 GMT  
		Size: 253.4 MB (253429110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec59ded0e9682bb6b3c1a8bf8ab2dbd9371a8ee3506172e2c2c853693f697aa`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b08c03340f645cd23f7cef2e544576c8916a72a19baf4938d52e7fe006a0ed62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f402739348440a551f0e292ac8a605d414dfe1cf68c9160b9dc2878baf3141f1`

```dockerfile
```

-	Layers:
	-	`sha256:e3b4491894623dc9ff05affc4fc2f703b4ff2828f5b4b8f5c8c7bf8ddd333233`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 2.7 MB (2703095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7422b2ee823d968f6b8d4e9af7e7574bf8f0bf268f5af2fb4f1c4f246246b249`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:082203012270827e3e1bdbef45184e2fac21d1133c019113a0c52ac6721710a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269408900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ffca762174df50af85f73c84aa24f04b749a49a14c90f139d434354e85fd42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:56 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Wed, 04 Sep 2024 22:44:56 GMT
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
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c9366cce4f443461ea3509558fff3aead08cb47b35ec661a655611b8307985`  
		Last Modified: Thu, 26 Sep 2024 23:58:58 GMT  
		Size: 2.5 MB (2533063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5739090de53dc8f53cdd523e2514251f3ef26cd528a28a0645d6c091d52cf55`  
		Last Modified: Thu, 26 Sep 2024 23:59:03 GMT  
		Size: 234.5 MB (234462151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02226885fe82df49c0fe8aaf9df5e74665984c630100317747309648da9e09b`  
		Last Modified: Thu, 26 Sep 2024 23:58:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:95406cd0bb3e127c06dc83a2272596f249ac43ea69795e5a0c6209db6a768da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5800c1831be3ab7954939e6761102240d17887bb8c9f04b268043872ec51aba0`

```dockerfile
```

-	Layers:
	-	`sha256:11955bfaf00773b913b772f9fcd307a52a3af0e320e3635a180af2270311c138`  
		Last Modified: Thu, 26 Sep 2024 23:58:58 GMT  
		Size: 2.7 MB (2699961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c77f7462e085145161d0e68ace8c7250c2c5ee8422dd1b042cdd8c6ff869c4`  
		Last Modified: Thu, 26 Sep 2024 23:58:57 GMT  
		Size: 16.8 KB (16775 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:8326ce7a337af167755f2a1f4aba0a905ada04f0a7c7d85b10d02e42f01609a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281938259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311684e8df932918ff285bd478fd6c506976de08f05e53f6d18e33fcbaa43c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
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
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbb0c0469be47f8494a9cc686d3a871114819d6faf484d40a9aa54c23b8c5c`  
		Last Modified: Thu, 05 Sep 2024 00:36:57 GMT  
		Size: 2.6 MB (2629989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09625c2a2dae391bc1f387ba7da27f20d32e8ffd535b5af135a675626439ab8`  
		Last Modified: Thu, 05 Sep 2024 00:37:06 GMT  
		Size: 244.0 MB (244008622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a0182ad5d05c8ef8285defc1783794fab53c7843d0eb73dc91f5e37a9fc4f`  
		Last Modified: Thu, 05 Sep 2024 00:36:57 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1c720488fd2a7decacc28646f4eeb990b45d101993422355d2d7cb8661b48e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2724069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b335aefc249ba2bf92013cde05af33105f4205ff9bd9a3b9abb54b6c34596b4e`

```dockerfile
```

-	Layers:
	-	`sha256:bf06a3e009ddb331eaffcc4ee81d9b046881bd9c2253e07d155977376ef4a48e`  
		Last Modified: Thu, 05 Sep 2024 00:36:58 GMT  
		Size: 2.7 MB (2707234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc30210a4c154526eba6fe99700f77fb9ffc444a5cd72b12fdbe38e7d09b2b7`  
		Last Modified: Thu, 05 Sep 2024 00:36:57 GMT  
		Size: 16.8 KB (16835 bytes)  
		MIME: application/vnd.in-toto+json
