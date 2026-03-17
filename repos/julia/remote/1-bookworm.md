## `julia:1-bookworm`

```console
$ docker pull julia@sha256:5268a49441bd60b6fe15bc86dd74c1697429f8163690473ec9ab59ef845da572
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:9ca0a1516419abfade0555a699eec3f36334bcb26c212e7d95880f23b767dbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325369748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9dd7b21a1c99279ffa6fb940543cc26c3ec15ed7240957e5ab5c4438f54bf3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:21:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:21:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:21:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:21:43 GMT
ENV JULIA_VERSION=1.12.5
# Mon, 16 Mar 2026 22:21:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:21:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:21:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:21:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb246dd8d84357e15edeba39a437991d6093b92a099a4f53d33110d7fd798881`  
		Last Modified: Mon, 16 Mar 2026 22:22:27 GMT  
		Size: 5.7 MB (5717932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b5269418350e0125da80cb014a54423d9a6998c363947367e9dbfe68d5dad`  
		Last Modified: Mon, 16 Mar 2026 22:22:33 GMT  
		Size: 291.4 MB (291415222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea5a4f5c8b10a3d6abcc8dcdda3650de03658d3c018e0b722bc90fde266f04`  
		Last Modified: Mon, 16 Mar 2026 22:22:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:ea3afe0eaf8e53b8a52a1edb36c967532e3044551441cf7eae9f68b5d0d44b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3af095911dbdc8046329b03a94387256e35f11e6e11c165cc74e0b31a01b1b`

```dockerfile
```

-	Layers:
	-	`sha256:be1dd355a48c7747e9ab3ed7f100195dc16f1a053d8945e7182f6afbe62d33de`  
		Last Modified: Mon, 16 Mar 2026 22:22:26 GMT  
		Size: 2.6 MB (2567696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff6c0f9d24b68dd97e1674995dd36c36ee5a60124529f4a437360631ac61902`  
		Last Modified: Mon, 16 Mar 2026 22:22:26 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c999ffc78ef911580ea84c05caa7f24cc0c65d7c82d77e00ab79bfab47281888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344905236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8b47b79cca78d470225468a21eb70e3ccbdc6ebe91c51afe3495f6c23b8d72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:21:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:42 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:21:42 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:21:42 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:21:42 GMT
ENV JULIA_VERSION=1.12.5
# Mon, 16 Mar 2026 22:21:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:21:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:21:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82466324d075cf18340998caa2811bd150aa8d8064c99adcd257dc0a24e07f5b`  
		Last Modified: Mon, 16 Mar 2026 22:22:28 GMT  
		Size: 5.6 MB (5567885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4370ed1e309a64daf43675e8d46d715be9f557d1ee92573a05cce4e47fbd60`  
		Last Modified: Mon, 16 Mar 2026 22:22:34 GMT  
		Size: 311.2 MB (311220916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b40bc3253991f9498ebfc01b1e5fd6efcfe14ba5d32cb54a24b05410bf0ad34`  
		Last Modified: Mon, 16 Mar 2026 22:22:27 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c3f42c6394d5f67d55e33fd2bf3a557c3fd8a474fe8d00ecd5d885bbe7577a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75e5ca54ffe8781a6e8e339d1f00896c14e96728fd10348c346d2a506e983d2`

```dockerfile
```

-	Layers:
	-	`sha256:c99157e7b5184d2446a0b778940cc95fe182a73fbddbfa503438002aeee62fea`  
		Last Modified: Mon, 16 Mar 2026 22:22:28 GMT  
		Size: 2.6 MB (2567971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae98b1a3c836125a6cfb0fe5c612ab0fa3d59956a90c89bd0fe8ebeaca0c5174`  
		Last Modified: Mon, 16 Mar 2026 22:22:28 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:8786e6e340c5354a2b554f0a689a45b8284766d7b125c90faa3c9f7de1331db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266282670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdeb69c8c5e69878164d56666c086591d4d8d503979f13507d81b7a2eff0aea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:17:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:18:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:18:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:18:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:18:03 GMT
ENV JULIA_VERSION=1.12.5
# Mon, 16 Mar 2026 22:18:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:18:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152e769e4b5958fd7b53c973bda9c266c0becc172a206e8c5511b3b2c43b9766`  
		Last Modified: Mon, 16 Mar 2026 22:18:37 GMT  
		Size: 5.9 MB (5878869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3dfa8e91fdfb3a809a950d5ff78dedefe9a3c497859d3ca46cf9b6a6ce8881`  
		Last Modified: Mon, 16 Mar 2026 22:18:42 GMT  
		Size: 231.2 MB (231181754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb6ef8be9ff6c570e717a30beaf4b337de8d8533fb68d524b4dd09151f1f4ad`  
		Last Modified: Mon, 16 Mar 2026 22:18:36 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1ec1d917508378d2b0052976438e7151126a602f7292e3a9d7044c9ec411977a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86037745be575bd96f4123b760ab5e7d6cf2d64147cb310c93c78f8f72667d9`

```dockerfile
```

-	Layers:
	-	`sha256:a8223eb1151aae7d7efd5657b0290c64bc000851f133bc15f08a4d7709d1d60d`  
		Last Modified: Mon, 16 Mar 2026 22:18:37 GMT  
		Size: 2.6 MB (2564843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96123a8822b3a7192ede9670d1daffbd95a0ae9de9413deec09acec97f51fe4c`  
		Last Modified: Mon, 16 Mar 2026 22:18:36 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
