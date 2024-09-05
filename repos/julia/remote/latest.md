## `julia:latest`

```console
$ docker pull julia@sha256:469701ddb6e43627ec86435729ac07d3fb6cafe62323f9f7543141ae5f12bf48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:76dc0a93f03468c5194af478abc60dbb6985cfdda0761d78d5ed0a2aaf36d8ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211247898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05324dfafc75c88ca76674e6bb4fdd125cae19778114524305aef6922d37f8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25e2794ce60a286233480f549a8fc2a23692758aae9ca22a67f374e64cecfb9`  
		Last Modified: Wed, 04 Sep 2024 23:10:20 GMT  
		Size: 5.7 MB (5712673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f0029234a9f3f9532602d87fe311b892dad827d02f4bb68576b27fa96609c`  
		Last Modified: Wed, 04 Sep 2024 23:10:22 GMT  
		Size: 176.4 MB (176408368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae0bb5cff6024d72408733971375d094833be291d72cf036fd8557850d23b53`  
		Last Modified: Wed, 04 Sep 2024 23:10:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:7d7b0cf9077a5381501de185074c321f9a4dac644c2749069733ad19b24eec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b661ea08a3a3c6a6f4bd4a05478af864e16ce494085196f8e2ce30c6b0957c6b`

```dockerfile
```

-	Layers:
	-	`sha256:1c0d034df7355e3859fb97a346046cc99b57437883e0b1c1bceff40eaacf8e9e`  
		Last Modified: Wed, 04 Sep 2024 23:10:20 GMT  
		Size: 2.4 MB (2436724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3ec84fda28b0ad2a095ccc10a57d5251471aa620566bb4322e914fa4be428e`  
		Last Modified: Wed, 04 Sep 2024 23:10:20 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e2055462abd9509e478bcdcbb01e1297bf092fce24fd4afa0694f208e620bbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211925401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebc1668d01a0eb3bfdb2b158689d1f04e48c17b713b30bfef8844d5bc2b4f21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
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
	-	`sha256:b9912cf5aa8f61abe4bff6ad5bcedb02daed3c9446cff7713bcf8c3562cfec21`  
		Last Modified: Thu, 05 Sep 2024 12:23:56 GMT  
		Size: 177.2 MB (177231297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a206780f850fcb763dd37a16cf146c5d6006e4af368771a131a665ffa05d0e8`  
		Last Modified: Thu, 05 Sep 2024 12:23:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:6c3867c42815ed4561e6ca07f9eb99589abe4f16718c034dd38e81998289ac54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920ce22704d26e54deb7f9b02924cdd626a2f0d40edffe4df66723be09db53cb`

```dockerfile
```

-	Layers:
	-	`sha256:7b6c0602fa82d5c75426343c515790dfb847610ceb9b3d9cfd2765e54c910214`  
		Last Modified: Thu, 05 Sep 2024 12:23:52 GMT  
		Size: 2.4 MB (2435930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52aa3f3b351611bb91e41c6f7b210fbf1248b3b0902bf5327dddd56a0385747f`  
		Last Modified: Thu, 05 Sep 2024 12:23:51 GMT  
		Size: 18.6 KB (18551 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:ebdac2860e2fa5a54db8683131c910cdc411c2d8299ea8fde90aa013e60d4793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193817060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a6229b6fc4c134614742b8fed541e99082df270b38f8a486845d859428fc81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da1f30fe92fd6979bfe08ebc525d23e7ef296afba4779d1d773bcdad3de1493`  
		Last Modified: Thu, 05 Sep 2024 00:07:57 GMT  
		Size: 5.9 MB (5870525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ef86916ded7a551e1e77baaae14d02989452992edd8932ae2f77fb9d085014`  
		Last Modified: Thu, 05 Sep 2024 00:08:01 GMT  
		Size: 157.8 MB (157801869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f855163b52927c407c08dcfbc06327944990568fd0db5032a6562c9d3a8d310c`  
		Last Modified: Thu, 05 Sep 2024 00:07:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:527c035d817b7dbf39fdba80d57eafbf9cb9ec3298f81da14217fd369d1c6c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2451939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3366bdc202bd3de566c084904ba9bf521e9d2bf77d5ae4936ee9d77c9fc1e69b`

```dockerfile
```

-	Layers:
	-	`sha256:3e290c2665b55365832d4af648bd5e311a3fa179a6653f1e6efeb4d55929078e`  
		Last Modified: Thu, 05 Sep 2024 00:07:57 GMT  
		Size: 2.4 MB (2433796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c280b5a3137cc86900218132a1baba80fb6f6d2aa5dded66e7118086f861fb12`  
		Last Modified: Thu, 05 Sep 2024 00:07:57 GMT  
		Size: 18.1 KB (18143 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:43b175aa16b348028f8a07b8a63de74a22e017b85ce0cfffb47fa2bf707498ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194508718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69593531145902938b333325eeb8f693d09c1a6529ca36443b06b69b796720a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70b3d4701b0d2614418e2b9751c16886e5d687e69b51c3e5127a60824147119`  
		Last Modified: Thu, 05 Sep 2024 00:34:49 GMT  
		Size: 6.2 MB (6247900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc6309de419466205f066cefac5a2970534e88bf28d0c6865b4a1fcc108b3ad`  
		Last Modified: Thu, 05 Sep 2024 00:38:45 GMT  
		Size: 155.1 MB (155138089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf74c80aff93bbdb57b18dd8a25564f30466d5e812cbda3928244d43c58b0f1e`  
		Last Modified: Thu, 05 Sep 2024 00:38:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:6acf883fd7aa9cac3737e0ddd0ffc2de2d2f4221f80483ffe916cc7285dc00cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd50698ec20cad44f697372853b3d6caf039883d84fe7d66ae9ad282db4a2cee`

```dockerfile
```

-	Layers:
	-	`sha256:752c64723784cd88bfb9ce0fb29d0180af1aa835730218a62c89cdfaf7848056`  
		Last Modified: Thu, 05 Sep 2024 00:38:42 GMT  
		Size: 2.4 MB (2440039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de0aa147b1cc3778ba54a2659121e68f4f8916c9f31fba5608cc3c28e9065ac`  
		Last Modified: Thu, 05 Sep 2024 00:38:41 GMT  
		Size: 18.3 KB (18258 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2655; amd64

```console
$ docker pull julia@sha256:35ff2d82eda048ca16d0d8eb20905a52db8f3531e5f5ede13186a2fb394cbdee
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330370334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5150180c61675eb08de51ad2ba1417ad6f4fd04da20972fd886fcff56226d07`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Wed, 28 Aug 2024 23:55:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 23:55:46 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 23:55:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 28 Aug 2024 23:55:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 28 Aug 2024 23:57:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 28 Aug 2024 23:57:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e86a373484a9226fb2951ac111cf61075374106381e25908fc926acbc6a056`  
		Last Modified: Wed, 28 Aug 2024 23:57:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25995c4cf169543f430445558d4c95aa6434766142bbb601ec43d1c537496a4`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66b8803d7228f9507e69ed2aba00848562367a5db6a1162e7a9f9a97dc4928f`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f7fc5b58fddfd1a3f9bcff4c4b6ad062847af85867a169074e877efd03e17f`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3412e707947fdf51a0772fd74c974e29ea85b079793fc9416f6b133f51585bd`  
		Last Modified: Wed, 28 Aug 2024 23:58:11 GMT  
		Size: 188.6 MB (188598911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85bd03d8438c88c9b546fbd749dcf5d9819ca8dec46c49e7408bb692db3e485`  
		Last Modified: Wed, 28 Aug 2024 23:57:48 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6189; amd64

```console
$ docker pull julia@sha256:d007df9135231c703058d8fb38ce8986162976b7292db8a4892cd9b1952952ab
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2433926176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8880f79a3d4ce83a1562605fdda3f727ad6276c3d01f2f0b03d3118b20a35ae1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 28 Aug 2024 23:55:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 28 Aug 2024 23:55:46 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 23:55:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 28 Aug 2024 23:55:48 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 28 Aug 2024 23:59:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 28 Aug 2024 23:59:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22b07d4ac7c21730fc02c65b87191af0bbd96758b7e3cbffa9fe02078313606`  
		Last Modified: Wed, 28 Aug 2024 23:59:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec83f52a10f1af30baa85b014fb89f22ab29253f203c144b5b5abdccf3769921`  
		Last Modified: Wed, 28 Aug 2024 23:59:04 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1e13657416b339455c575c0dc0307482fd20c232bbb0d58fb2658038c4504e`  
		Last Modified: Wed, 28 Aug 2024 23:59:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce1347ee812b4edfd510f18a100836966c6737474127af4395b4ef7bce9cc51`  
		Last Modified: Wed, 28 Aug 2024 23:59:04 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f929c7c33fe400b46e3b0ae469d1d08ee4ab4823e9fa79bf0bfdba390b19a45e`  
		Last Modified: Wed, 28 Aug 2024 23:59:27 GMT  
		Size: 188.7 MB (188716457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e126b67348756f33e0f1a03130439a47d775272bba9645c6afaa147896e071`  
		Last Modified: Wed, 28 Aug 2024 23:59:04 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
