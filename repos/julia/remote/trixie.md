## `julia:trixie`

```console
$ docker pull julia@sha256:c6f8f47eb641cb088e772d193a46aa2fa59f53462bbb5acbc4df9dfb455218b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:trixie` - linux; amd64

```console
$ docker pull julia@sha256:6798f3379146d108c2d384bae9d70c1a474d2e70bc515b2784eec2abeacd015b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329631092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f820ed914df5ca8432baeebc2b5c92b8b6a1d8f135aa0c2564262c60a685a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:20:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:20:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:20:38 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 24 Jun 2026 01:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:20:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4326bf71ecaf6c8bcff0ea0a455d1572bf105249f4fc15b47a2956cd5aa359c`  
		Last Modified: Wed, 24 Jun 2026 01:21:22 GMT  
		Size: 6.2 MB (6248430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71541e7da5c5f38c0a05057e5062ee94fa8ae805a33916194053de9e5ccd9538`  
		Last Modified: Wed, 24 Jun 2026 01:21:27 GMT  
		Size: 293.6 MB (293596876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b83f76b6d2dcfd053e0f7ab0b549cf3d0df43ac34cd01d12739bfc11c1e3b9b`  
		Last Modified: Wed, 24 Jun 2026 01:21:21 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ac923af9187e94577ef6bb2cdf4ca017b3a20f8a07d93cafdf5f34f358af8515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5cdd7da3cb5ed9d051836dd845cb415d7a91e0799870944e9ea1c213f29edc`

```dockerfile
```

-	Layers:
	-	`sha256:c5e2a1ab1dd4cec053d9d39f3d2ed9c4a9968a8c8c9c636055f9415b429d6e47`  
		Last Modified: Wed, 24 Jun 2026 01:21:21 GMT  
		Size: 2.2 MB (2240427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4cda070f2f6e72da86693eb087963f8cead47ca6c84328fc1ee5e2923c1c0eb`  
		Last Modified: Wed, 24 Jun 2026 01:21:21 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7ed4116ef9869286fe9c30adf41d61eb0f264788b9e23f68717103f4d281b51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350590629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbeee83cfc71f6807ab7dd07ebde5a02da3e44a6140280c67349248393a3180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:20:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:20:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:20:59 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 24 Jun 2026 01:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:20:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48205b84ecdbd9e90531fe22a801d51228023244090bd63f2a1984a0bdd044b`  
		Last Modified: Wed, 24 Jun 2026 01:21:45 GMT  
		Size: 6.2 MB (6155459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5d34fd599b9242ad3a0a28272f315849ac3bfcb67d44b35e32eb8fa2c125c`  
		Last Modified: Wed, 24 Jun 2026 01:21:53 GMT  
		Size: 314.3 MB (314286249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad42b878adb4595afbc7cfce9750c7538947f73004515e499794225d0dc9d97`  
		Last Modified: Wed, 24 Jun 2026 01:21:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:e426bba9a7784826e592eaf7b21d2a21fc34298d12d72d3026c1d5d69c56ac29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983befd3bdfa3b8e67055a6c3a134e89b5dacee7fc43478f041e8d640b5c2a08`

```dockerfile
```

-	Layers:
	-	`sha256:997b511c773622417268948dd9d2cdc2ae4090244a791fc8b9ef3fe62250c84e`  
		Last Modified: Wed, 24 Jun 2026 01:21:45 GMT  
		Size: 2.2 MB (2240751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c355eb9d606f46f0afc4e35fbcfcee019f57b6caa63558cade67099b8e4fd70`  
		Last Modified: Wed, 24 Jun 2026 01:21:45 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:80d15663daab41c73ee44cfcb80dff1110e38202f31c58c6c3a11f300c5cb3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270231037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bca15e13bd3183f232b46b9dddb4fc3dd14a25d0f6de815ce501e3182c770c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:16:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:16:53 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:16:53 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:16:53 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:16:53 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 24 Jun 2026 01:16:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:16:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:16:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:16:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54562366ba44552c87c62705b471653daa730799c7cd09d914cd7ec0329389a`  
		Last Modified: Wed, 24 Jun 2026 01:17:26 GMT  
		Size: 6.4 MB (6435886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3828d3b182c587d7b6fef2acb72939b5ea29fe35f867ba3da542d951da9232dc`  
		Last Modified: Wed, 24 Jun 2026 01:17:31 GMT  
		Size: 232.5 MB (232493567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6236e243722d3f06024429f303f84c89b6e2927115f675b8ab93649902b766`  
		Last Modified: Wed, 24 Jun 2026 01:17:26 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:df7600cde61a72a4baa9e70049f77b38e2941348fd557c04862a4b94be40e573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f143940ebf0de7d31891276022d60183944b6216326102eaba314a58457c20`

```dockerfile
```

-	Layers:
	-	`sha256:96b6232e6783c7e8ad1c0e51d8b48592d2f6d68748f79ed6d1f8edc2408c1be3`  
		Last Modified: Wed, 24 Jun 2026 01:17:26 GMT  
		Size: 2.2 MB (2237552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5284da5cfa7bf4d73cb40115c4b0eeb8a9a9c41f722a61c22df0ad2a48fdab`  
		Last Modified: Wed, 24 Jun 2026 01:17:25 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json
