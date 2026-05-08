## `julia:1-trixie`

```console
$ docker pull julia@sha256:d6b0db74a325f298e5f209f2cdbdd8b4a4f9211895abdb0422fda095bd557227
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
$ docker pull julia@sha256:1fe2de94c55ef259658fdf3fd572cfd97a27a97de4a0aaa804eecc9082fab2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329624456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f4e27ad227495b7be51cc9c82f03c1cd47cc91eb4c692a9b63dbd3ec963c73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Apr 2026 01:20:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:20:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Apr 2026 01:20:46 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 22 Apr 2026 01:20:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Apr 2026 01:20:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:20:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ce9ed6a2834a7febc7c6a6d0c4ad5fbfd4baf54d7160fb8160b6d7fdfe4c5a`  
		Last Modified: Wed, 22 Apr 2026 01:21:30 GMT  
		Size: 6.2 MB (6247034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6862e94e4620368ab3cea2ff4cf1c2c3a1c437ea50674f5920aeb8c9100d97`  
		Last Modified: Wed, 22 Apr 2026 01:21:36 GMT  
		Size: 293.6 MB (293596877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899ffa6136c895828457051d099f116d45238ca41225d537407212870c2d25db`  
		Last Modified: Wed, 22 Apr 2026 01:21:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2a6c2ca49639dc4f6a2ed8bd283f1b7a1e2218092177a3a597aa2693623f4e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c01566ec2bc40e1dc4e14223bbf0a32fcad1cafee7f12a11cb47dac1f6368f`

```dockerfile
```

-	Layers:
	-	`sha256:110e30a7729259d579190eb3809e909d9aecc1e9c97cac78ef4654acf800c286`  
		Last Modified: Wed, 22 Apr 2026 01:21:30 GMT  
		Size: 2.2 MB (2240259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a48d77222a6af400c0324b2156684a712fcd4713c47304efb1137cd0189276`  
		Last Modified: Wed, 22 Apr 2026 01:21:30 GMT  
		Size: 17.7 KB (17688 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4ca77a721c915f69b65bd25077aa1a89c9ba4646b1906ec88ffde28e3148cf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350584649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e17938264725df3908c1a18ab17a19f752e67d991eb0dc5e275ebad68954d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 May 2026 19:20:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:20:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 May 2026 19:20:07 GMT
ENV JULIA_VERSION=1.12.6
# Fri, 08 May 2026 19:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 May 2026 19:20:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:20:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:20:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf639e80263b13ae13bc4bbe328f590fec3e3659c582609f58a015df8c38fa6`  
		Last Modified: Fri, 08 May 2026 19:20:53 GMT  
		Size: 6.2 MB (6154445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0a6e458a2fe53b4ec8d2dcc03111931594e4adf7a5db0f0ee92aaf98d882f7`  
		Last Modified: Fri, 08 May 2026 19:20:59 GMT  
		Size: 314.3 MB (314286193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6218ff8d118ff5f8274b529edb2cac15752776996af7d2b58a48ed75e47b5190`  
		Last Modified: Fri, 08 May 2026 19:20:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ec9ace4c9f9812c1aafc64d8b1b8f7fba8abc9aaf9aa7af0ab45f398684c5f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a827a6f407d216aa958be9cdf1db8ed7ed1838a72fbf7c18e63dc6fb645205`

```dockerfile
```

-	Layers:
	-	`sha256:c55fb3b6754667b484c9e0e14ca14e554926a86ce083c41f07e7fa5ab75df25b`  
		Last Modified: Fri, 08 May 2026 19:20:53 GMT  
		Size: 2.2 MB (2240591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829a34621c91a235caed0462ec4e1832b63a93e111c51c6f167d8c6d4791a6ff`  
		Last Modified: Fri, 08 May 2026 19:20:53 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:04942c24c0cda0998c1c0be6a20881e05f3e3f43a16c72758be3cf090902a570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270223813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab354da10650c602020830044a1d15c68b544b113d1a25dfed32d015a143f348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Apr 2026 01:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Apr 2026 01:16:50 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 22 Apr 2026 01:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Apr 2026 01:16:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:16:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6cc86c2bc3398eba3c7b216fc52a22cdba31135e65f97bf30eb3df16d44fa`  
		Last Modified: Wed, 22 Apr 2026 01:17:21 GMT  
		Size: 6.4 MB (6433736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c752f6bc7f6e2b30226808f004f823ba1a81def8bf1663b626d4d2c06929c439`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 232.5 MB (232493381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212a487ef76e2f46f84d3ada157486d6a951387cc1044d00c239aadb90ec1da`  
		Last Modified: Wed, 22 Apr 2026 01:17:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:be5adb81b7823d93ee6f68b015f3d620a7e53fe0a601838f272ed04e9bce2508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24a04c8f80eb2cee63a02b63459e1a19d3ee385c7f4975ff0ce7d1d1eb7de7`

```dockerfile
```

-	Layers:
	-	`sha256:daf6943410a60ac1af38bd271269032284982821df27a747fa0095b07e6fee05`  
		Last Modified: Wed, 22 Apr 2026 01:17:21 GMT  
		Size: 2.2 MB (2237384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872b52598676aa887ed550e0a2a6019c07f7a44eca930ca47bc91f3545ac6dad`  
		Last Modified: Wed, 22 Apr 2026 01:17:21 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json
