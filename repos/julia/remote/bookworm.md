## `julia:bookworm`

```console
$ docker pull julia@sha256:7fc50ff36010d7c9ed79b59fa178f85aa8c8fdcbaacd66bb3baef3c59d774a53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:b5ca2b103ebc40ffe890bbea39556978273b2bf6f56f1fd882d489a847f58348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327512581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b1c14ad069685331cae67f352324433ef972113a9c7f81e171ea52836faafb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 May 2026 23:04:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:04:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 May 2026 23:04:20 GMT
ENV JULIA_VERSION=1.12.6
# Tue, 19 May 2026 23:04:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 19 May 2026 23:04:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:04:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:04:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaaee9bf524d412f08b84fa223534c81acf875ed6eed9a93e66d63140741739`  
		Last Modified: Tue, 19 May 2026 23:05:01 GMT  
		Size: 5.7 MB (5720913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310203049db5cf8fdaf19ec7b31d5c9ccfc98035ecabbcb93dbef18b822da1e9`  
		Last Modified: Tue, 19 May 2026 23:05:07 GMT  
		Size: 293.6 MB (293557753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc85994170c144f68047a41fbc608253dc7fb90665d7ceb5992578a8052e9537`  
		Last Modified: Tue, 19 May 2026 23:05:01 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:fd978c5843602905b0d77f0b41d46d1739dc71603d5bd77b87d9ec0bce1dd0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c469f234f13dbf4040e7f4e52682b9b345fd1c59d4208f5ad158a452f6626e97`

```dockerfile
```

-	Layers:
	-	`sha256:ff28abdd341881632e3dd10385e1f8669f1eb5b0ae55a181efdac947400740cd`  
		Last Modified: Tue, 19 May 2026 23:05:02 GMT  
		Size: 2.6 MB (2567714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108c7710835d855f703da0c3709e1edb96ab5fc640f9f2fd7bfcd4757b2af5a4`  
		Last Modified: Tue, 19 May 2026 23:05:01 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1a94b8d24fca0a9ba986649a1fba03728d4323108e4843a659e6288c94b04ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347944112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03a2c20b28d5c672ac6f821cc09703c2f9fa941d1a053b7b32a051b9c23a1e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 May 2026 23:04:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:04:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 May 2026 23:04:14 GMT
ENV JULIA_VERSION=1.12.6
# Tue, 19 May 2026 23:04:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 19 May 2026 23:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:04:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb4a8e5491a7a5ab44193341ab1a81cb987d60c2f0e101e75755a9e5aef6287`  
		Last Modified: Tue, 19 May 2026 23:05:00 GMT  
		Size: 5.6 MB (5570014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24373602d6347368c53b7583afb21c4570715334a729ea28ad8b1329e1c92fe9`  
		Last Modified: Tue, 19 May 2026 23:05:08 GMT  
		Size: 314.3 MB (314258685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ceae0372f12ee106b60590af187795ccb0910d4d97f5b8c0ad81a4de342c6`  
		Last Modified: Tue, 19 May 2026 23:05:00 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:691e01b670351618db1f1614a613b1143f7398d6b565b50e88505b9b20960a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c983d6e5acc756b65642254f4dec66e0a4e6d7659cefaff6802370d63a5f7d6`

```dockerfile
```

-	Layers:
	-	`sha256:f09806ed6331efe46afe68a87320fd68d86584efdebab843acdd57421359ae53`  
		Last Modified: Tue, 19 May 2026 23:05:00 GMT  
		Size: 2.6 MB (2567989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc493e8c2d9d7375b3a5df7a928447e7696fe70432927924b3f1a6df572ca51b`  
		Last Modified: Tue, 19 May 2026 23:05:00 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:b175a07f8afa1a5e977752950ac7e83b9b3679770e31a171e59b1a1c61e3ac52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267552668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a10ce98ab22387f6af02dee99a68e827dd3fa704b7798efbf64283a1d6de252`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 May 2026 22:58:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 22:58:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 May 2026 22:58:48 GMT
ENV JULIA_VERSION=1.12.6
# Tue, 19 May 2026 22:58:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 19 May 2026 22:58:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 22:58:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 22:58:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883663569d2ca08d451ae31659282496f780bca4899394555bc916edf98ac785`  
		Last Modified: Tue, 19 May 2026 22:59:20 GMT  
		Size: 5.9 MB (5879691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902d6ed61afce9773f41e127e637c01f99de75be01dfc7793a781f705d6ae255`  
		Last Modified: Tue, 19 May 2026 22:59:25 GMT  
		Size: 232.5 MB (232454003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b708f8dd5c9cabe0f8e3b462e2abd927296ef5b1792d8db5cb86ab2f2ffaf9`  
		Last Modified: Tue, 19 May 2026 22:59:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f364a74fe515b444dcb707f14384cf253d0fdf3fd6ff99d1ca903cdff74bf279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8925a9f695b9aa55ef342f1eaaded471b2d332530c0d9239fe9a99562ebcc3`

```dockerfile
```

-	Layers:
	-	`sha256:5a813bc95277cf3827bdc83a00ee17d4785f84de268cf432655c78a1d1bbce00`  
		Last Modified: Tue, 19 May 2026 22:59:20 GMT  
		Size: 2.6 MB (2564861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad3e832d3e54ac7221ee55b2be4e134800fb340369009bc539685bdcf3aef7a7`  
		Last Modified: Tue, 19 May 2026 22:59:20 GMT  
		Size: 16.5 KB (16512 bytes)  
		MIME: application/vnd.in-toto+json
