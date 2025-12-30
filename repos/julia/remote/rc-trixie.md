## `julia:rc-trixie`

```console
$ docker pull julia@sha256:60d325de832920b82fc3a2b04b36234a2e51cf4adbc28e0bb713a4ff76498b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-trixie` - linux; amd64

```console
$ docker pull julia@sha256:37266186eebe148ae5ef3859f42dc48858df120a8a398261fd3a222ace4751b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342734086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7af534e16148c66d8897611b3d9f2dfd042cc809d9490ed19f3ba3d6318fc59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Dec 2025 23:21:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:21:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Dec 2025 23:21:37 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Mon, 29 Dec 2025 23:21:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782745e0bbabf49f29dab027f40791808349c5332272898260a0b94ef6d2fb13`  
		Last Modified: Mon, 29 Dec 2025 23:22:39 GMT  
		Size: 6.2 MB (6242871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b2538d53b4dbb775a64f2d8152e3fff32422876c146dd3cf2c18dffccf6fdf`  
		Last Modified: Mon, 29 Dec 2025 23:22:39 GMT  
		Size: 306.7 MB (306714308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9a70932a25f726924f84a96414d1436bc2711560bf299e24e3dcf284958a5`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ccad9a3c9e71b750faf5285a9a1543a09cad5d4cd01dcc557195476fa4c78758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e097401d848412a3a11f935b8c0cf1beeef797eb9b89e29ac874a18f3942c86d`

```dockerfile
```

-	Layers:
	-	`sha256:6f5a5be65850efec8cc5ded08b7e7159d9ad9fb04113cb05ee04f80022a38be9`  
		Last Modified: Tue, 30 Dec 2025 03:03:54 GMT  
		Size: 2.2 MB (2240783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12d454cd95e86b5d9639cebb344c6da0a5b16744ec4c49e0306153cae6c9f77`  
		Last Modified: Tue, 30 Dec 2025 03:03:55 GMT  
		Size: 17.2 KB (17205 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a3be761bc1b19231f905ba37b10c58a4c557ead4a676796f78cfcfcdce1e13ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366004549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20421995351728789247d072460083993ef7e95f0e7c0578b0e319e28e89eeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:22:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Dec 2025 23:22:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:22:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Dec 2025 23:22:13 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Mon, 29 Dec 2025 23:22:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Dec 2025 23:22:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:22:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a84c239e2a01e8799892a32383504d2ae8b307157be8b4ae61d1006201e9d82`  
		Last Modified: Mon, 29 Dec 2025 23:23:15 GMT  
		Size: 6.2 MB (6153446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a311316add4f0105a18bfe37b9c3bbaa7b688264d606808406866d9365018540`  
		Last Modified: Mon, 29 Dec 2025 23:23:23 GMT  
		Size: 329.7 MB (329712099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dcc89b50f7432b1df8e53cd787fac6efff66c49d5b3bb6f4bc39f2366fa810`  
		Last Modified: Mon, 29 Dec 2025 23:23:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:353e7c0fb96893a44c285daf31ac5a9872d272f95d813f33ad83f976cf6c5223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef31334de26d6e2254d8c97f345fc3bd3d604171824baea60e08c97b9fc14162`

```dockerfile
```

-	Layers:
	-	`sha256:504ec17b8f522227e4580be9233988a726f0c40c41c0634f9fb0b2f46bc49f39`  
		Last Modified: Tue, 30 Dec 2025 03:03:59 GMT  
		Size: 2.2 MB (2241091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d743dca2aa7380849b8f80be3c2255af3af9458d700f59eb7fa7997b686c432`  
		Last Modified: Tue, 30 Dec 2025 03:03:59 GMT  
		Size: 17.3 KB (17347 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:87cbbde75c684c5d2a524298a751792c4c0182c3fc00ac63d943d5e4e20fb86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280240818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958909dbe6008ba13f6434dd4fe2ac01f4b9de0aaf7af6447feaef01616af6c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:16:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Dec 2025 23:17:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:17:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Dec 2025 23:17:06 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Mon, 29 Dec 2025 23:17:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:17:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f67c9decc3583dfa06c4847c8eed2f112bfcafda91af03052b30e5861f6b7ab`  
		Last Modified: Mon, 29 Dec 2025 23:17:49 GMT  
		Size: 6.4 MB (6427678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf2d5b9c3e3eaf182171027f58fac8e983f82a04d64380e09ed3a9afc0d702`  
		Last Modified: Mon, 29 Dec 2025 23:19:08 GMT  
		Size: 242.5 MB (242519668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75158e739e61715eee6e2b048042812078eccbdd9f7b0e62b689c3497457ed3f`  
		Last Modified: Mon, 29 Dec 2025 23:17:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7465c5dfe6726e4a790475699d9c19407dfafe1444a396716e1c15a42e4d0fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4705c869e6baef01597be47983f1bda42a408fa44920c65fc7f092c66e259e9`

```dockerfile
```

-	Layers:
	-	`sha256:dc38d2ca5ed34ae509a2faacb6fe6db1ce0366372700bf023155e5e8f8bb6d1b`  
		Last Modified: Tue, 30 Dec 2025 03:04:03 GMT  
		Size: 2.2 MB (2237918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec416247cc57b2b314e0373180186543ad9d56b15b1844b172b3d55c47601c25`  
		Last Modified: Tue, 30 Dec 2025 03:04:04 GMT  
		Size: 17.2 KB (17161 bytes)  
		MIME: application/vnd.in-toto+json
