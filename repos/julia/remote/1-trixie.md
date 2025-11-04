## `julia:1-trixie`

```console
$ docker pull julia@sha256:ac48e8257c839954341858486babc1e1ec1ec61c137577dba475a4de1bcf257c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-trixie` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 19:54:03 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json
