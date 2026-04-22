## `julia:trixie`

```console
$ docker pull julia@sha256:2932745b3c25739bbeda9e2c4f9f4206de820cb203ccff65c169b30e695b7dcb
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

### `julia:trixie` - unknown; unknown

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

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fd27fc5dbe5ab3d0371f309939073fb41f47c4fa39e205c3eabe118c9895b7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350584553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66877598217f939145c834aaf27f697b959ea0c1991b277a71a1477a236edefc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:21:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Apr 2026 01:21:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:21:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Apr 2026 01:21:07 GMT
ENV JULIA_VERSION=1.12.6
# Wed, 22 Apr 2026 01:21:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Apr 2026 01:21:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:21:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4902e5a1f8480c02eed3f4ae1f3455dfa6665a3afa6cf27f5401c59271c50dd`  
		Last Modified: Wed, 22 Apr 2026 01:21:54 GMT  
		Size: 6.2 MB (6154442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51c9360275a0084377e557692f646df27fecbdd05f27a658bb363cd2955fe51`  
		Last Modified: Wed, 22 Apr 2026 01:22:00 GMT  
		Size: 314.3 MB (314286133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69df51b8833276854800fab164483dd9479feda4f298d665eecd399e7f4cd60`  
		Last Modified: Wed, 22 Apr 2026 01:21:54 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:69c7f328b47e52eaa15b0c2192bd2c4b47552c87a6da1bec063cd16a9b69752e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344ff187430d5ba441fcd08133ab22a5c8e0e4cd759a94e11ccc8aaccde03cc4`

```dockerfile
```

-	Layers:
	-	`sha256:c1a9adcad1efbae9200d0166f4b7328783fd9acbf97d21c5d11999366d3c54ef`  
		Last Modified: Wed, 22 Apr 2026 01:21:54 GMT  
		Size: 2.2 MB (2240591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092d9da7a15e2c6f548ec3789f63c32453e9bec03534ea11924506632ba38f21`  
		Last Modified: Wed, 22 Apr 2026 01:21:54 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:e83a6047db06989ec5c2e480e12cc6bff090f476ac3b8d65cd93447cc34aab0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273102686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d957af4ad979f2af89445acce7ee111d257ceedb3d95a41118507e95da35c8fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 14 Apr 2026 00:26:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:26:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 14 Apr 2026 00:26:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:26:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 14 Apr 2026 00:26:28 GMT
ENV JULIA_VERSION=1.12.6
# Tue, 14 Apr 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 14 Apr 2026 00:26:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 00:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 00:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ebfc19e1898ac4681983a2a55411408641acc81fe89508c9f3c6a74824b83`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 9.3 MB (9317310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39ca7da2f31349a2134b397d24a71778320afd9a3b443023e601e75de47c801`  
		Last Modified: Tue, 14 Apr 2026 00:27:04 GMT  
		Size: 232.5 MB (232493753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95f0f29bba3334989a69c3b3d3756051705f8e8becd1a682515521da92f84fc`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b46ea295ca96230654e3c7632a569fb8d1ae474f01da0a0d9932a8ca11023bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869c40f34d4fd72ec99d77f210bb0265da4d2bd73da94e91ef876015968e19f3`

```dockerfile
```

-	Layers:
	-	`sha256:1b1c97d9bd4883bb34bc3cfa3f43b4ea7ecae479e22907568736791fa962c72c`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 2.2 MB (2237384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7863b5384e4649c0f8c7041ec500c95832e352aabcef3add78cf40f45038b0`  
		Last Modified: Tue, 14 Apr 2026 00:26:59 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json
