## `julia:1-bookworm`

```console
$ docker pull julia@sha256:ec8ff1dac359ee0db6defa76ff576a214d9ada6508a818c1414fda08ca7731c5
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
$ docker pull julia@sha256:2478ee6b57b92b08c0ff272f771c5bc94763c653b9e352db1726c7bb437561da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327517238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2614bb389c3a3718ba745d66fa25023a009bf771167ecc1de7d172c8a1d25e22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:21:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:22:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:22:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:22:11 GMT
ENV JULIA_VERSION=1.12.6
# Thu, 11 Jun 2026 00:22:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fab864490163fcb4dfb919a78869bf73102564c59e1ebd653e8858773bad3c2`  
		Last Modified: Thu, 11 Jun 2026 00:22:56 GMT  
		Size: 5.7 MB (5721476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d9901bd68cda941070afec249d49ccb9777ceefb87fa955010ed9d2174e08d`  
		Last Modified: Thu, 11 Jun 2026 00:23:03 GMT  
		Size: 293.6 MB (293557768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6917117ff10647613cb99da3e141ea264ba611a7e8cbacd046edb50a279c21`  
		Last Modified: Thu, 11 Jun 2026 00:22:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1faf0ee0e9bf635ecab6b4b555fd513f63b6ee5070da1e8275681f027e076d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bdfe50d0d62ed874974ce858d86f0c631fd1785de881f5c59ba42ca2f7012b`

```dockerfile
```

-	Layers:
	-	`sha256:c9e2637ee689c192f2b642e8c24d108a1c9fe3bd96ec76b87a04e45ec46423eb`  
		Last Modified: Thu, 11 Jun 2026 00:22:56 GMT  
		Size: 2.6 MB (2567732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4510340d902d83b44180faaf005f8d787efe8cf66891bd9b6267f5c823cde694`  
		Last Modified: Thu, 11 Jun 2026 00:22:56 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5a2efa2869a0ff32d40e9e8d39cc2f0d0e37b3d650c8e4468d88eb98a4045d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347951801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7a870038099e8a70700fbe60fbd5be0f16e1dd2c409d0c91071a6c13e04a30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:22:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:22:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:22:59 GMT
ENV JULIA_VERSION=1.12.6
# Thu, 11 Jun 2026 00:22:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:22:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:22:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfee41b73251b7d2d7fb7950e20f3994e797d9cfe5df8f55a84c15b619c3214`  
		Last Modified: Thu, 11 Jun 2026 00:23:45 GMT  
		Size: 5.6 MB (5570462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2e693480b709d1724ea70b6be3d75b0a1982470c53731f7267e6744debdd74`  
		Last Modified: Thu, 11 Jun 2026 00:23:52 GMT  
		Size: 314.3 MB (314258662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55e5c5b73832d5f28a020245e28de7e6815f75f67bd3acd5f9f606c23b07dd6`  
		Last Modified: Thu, 11 Jun 2026 00:23:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:cd18a7b928567f0fb62052b8c97f0056a6b527df550f1877244ce4c780141572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a60b4dd6780d05aec382c7ed83a2ca939ecf905bac291dc8fcd6c521623be9`

```dockerfile
```

-	Layers:
	-	`sha256:bc41f6c7a1c8591f5186bd2c4ef8e71ae104046433c41ddd098b2140b75bec40`  
		Last Modified: Thu, 11 Jun 2026 00:23:46 GMT  
		Size: 2.6 MB (2568007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf652879f6635daa425e09f0decbf522fe905bab0c88f1b00359dbd12df044b`  
		Last Modified: Thu, 11 Jun 2026 00:23:45 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:5399ef8a76713c425bf60fe648acdb51f4bec86d3a56299bcab104b00b2ad743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267560142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5bdd7c8ed32339abc1a44b3123b3c8a32f120ce9a79770a1fa555dce326537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:17:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:17:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:17:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:17:41 GMT
ENV JULIA_VERSION=1.12.6
# Thu, 11 Jun 2026 00:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:17:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f38d43bae588245aae00aba7b515932c1f9e7356f5374da3de4a5eb0b7a1fc`  
		Last Modified: Thu, 11 Jun 2026 00:18:15 GMT  
		Size: 5.9 MB (5880050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c41b3264b1481a3bb0d9f66c1fa0b3f87791326f9df73065f1a5aba16fe0eed`  
		Last Modified: Thu, 11 Jun 2026 00:18:22 GMT  
		Size: 232.5 MB (232453961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658dfa11cf83f8e2996a280d66f7a21de8e5b1780ec2aeb643f977f5e55f7b8c`  
		Last Modified: Thu, 11 Jun 2026 00:18:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5fd93a13bbf4e8ad28e7fc868e5b467dd2f10e2d921ea3ad1f10e73d241c5e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1abc6fd3bb6ee904809a5b27bb886801077cb234bcbc5eddff5c36a7d615c07`

```dockerfile
```

-	Layers:
	-	`sha256:71acedc08da440f9cd1514fa60044724d199719ca6d6406ef5d12b343b9fb62e`  
		Last Modified: Thu, 11 Jun 2026 00:18:15 GMT  
		Size: 2.6 MB (2564879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df77dcffb715765392741e2fd0f39b0f4d7a4e23e3932e7b05cf583f8d950ba2`  
		Last Modified: Thu, 11 Jun 2026 00:18:14 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
