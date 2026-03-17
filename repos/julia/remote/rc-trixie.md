## `julia:rc-trixie`

```console
$ docker pull julia@sha256:6a7a969089216cb32bba1ea57f8ad241bf6728ecfdd1882bfbc87f81205a7433
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
$ docker pull julia@sha256:15a31d956f2749233e9a82a83821425871bce0576ac25dd2eaa8b701f36ce50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344834315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab477c0c7c7b9019ae5c4f1c6829de2fe6cafaccd1e55fe28f77c0525fd863cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:23:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:23:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:23:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:23:04 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Mon, 16 Mar 2026 22:23:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:23:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:23:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4487cd740fa14ae3f5825de92474f09361fce8c7cb3a5a283548eb09414cda`  
		Last Modified: Mon, 16 Mar 2026 22:22:26 GMT  
		Size: 6.2 MB (6247066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd76c52bdb2e2bcffe136372c7dccdc691937d8ce34c294dcbda495c1f0f7f6`  
		Last Modified: Mon, 16 Mar 2026 22:23:55 GMT  
		Size: 308.8 MB (308811376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856999d5c42dff2697a2309d135027497f29696845b84b3f2edddbd84082ee9d`  
		Last Modified: Mon, 16 Mar 2026 22:23:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2316ca54ea4fff412519466f365e40104846fd6256cbb556734a4316ed5b10f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1169badc0ff7aee56af2a9a03e5264b35576517afda367b5cbf9dbe9a4c3737`

```dockerfile
```

-	Layers:
	-	`sha256:a14b60dc09f504b991a9c3f9b73d6926660c42892c83085045c947b99bb9bf81`  
		Last Modified: Mon, 16 Mar 2026 22:23:49 GMT  
		Size: 2.2 MB (2240915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a4d2ace8c8cf46bdf1013d5165d71ce2149752a8c0396e0d9f6054a866993d`  
		Last Modified: Mon, 16 Mar 2026 22:23:49 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:fb5137923edc6e6d1a57deec127a6edb82c57aa173da09bd3f77e29054e6eff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369057670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b361b6dfce44f2eef4f06a5cdd0da7dfd0dbb2bbc415aed56d6eff5c83bc29d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:22:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:22:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:22:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:22:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:22:49 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Mon, 16 Mar 2026 22:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:22:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:22:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:22:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96375526b57ed728734f154de954fcd470ee1da9c5699f81724af31d932b97bb`  
		Last Modified: Mon, 16 Mar 2026 22:23:38 GMT  
		Size: 6.2 MB (6154454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec407e8e403a9b4bd18493435323317f63c7a4dd9da5965faef27d1ad918c756`  
		Last Modified: Mon, 16 Mar 2026 22:23:46 GMT  
		Size: 332.8 MB (332764432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2a0319d110e67a241d15757564920d5bf734db9791de68666e7ee22d33b0a`  
		Last Modified: Mon, 16 Mar 2026 22:23:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:0f9a99cbbbf2c5aa1dce6a52734ba621a03d4032b2cae4deacf3435a5ce7f82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c365759c91710937dbdc790e9525f2eb46d6583539bb2889fecd205ace716a`

```dockerfile
```

-	Layers:
	-	`sha256:67ef9fbfca74bbe4f8c102165def26e1b719e8924b0170151c3c90eb32b173f0`  
		Last Modified: Mon, 16 Mar 2026 22:23:38 GMT  
		Size: 2.2 MB (2241223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9e2dada137b884f084c0d9f1d3c496805c7cba36ea59f8a3a9d5a4c9bf8ce25`  
		Last Modified: Mon, 16 Mar 2026 22:23:37 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:bc08745f3be0dc7fb983829f367b3b5160fb2dd9eba5c91616785fd841a962a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280691189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bf25fa1625617ad4cd4c898a0287978b4c977a628abca518780cbe84fb05a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:15:52 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 16 Mar 2026 22:15:52 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:15:52 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 16 Mar 2026 22:15:52 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Mon, 16 Mar 2026 22:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 16 Mar 2026 22:15:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:15:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:15:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beed1117b19ca752f25921088a8713b15055d87e9f7abd62580f5004ede02a95`  
		Last Modified: Mon, 16 Mar 2026 22:16:26 GMT  
		Size: 6.4 MB (6433740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e44a4080233a24f0c4c4f90e7057c3525583974fab28d771f5bef7e049d555`  
		Last Modified: Mon, 16 Mar 2026 22:16:31 GMT  
		Size: 243.0 MB (242965948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f93dcf30f0f05cde2d5cf8d1f6403a9def0d62b620968197225585f60ec93b`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:122c08430cbd6fc276e57d1978ed1fc3d57de0bc218eca8c5fce95b29cf14405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69ed6f91b9df1a036e28beb988106d0136fe003810aca386225b51a30c2c46a`

```dockerfile
```

-	Layers:
	-	`sha256:c3d37e4ffaa41e6b981e6f8ed994bf093dc3544507dfa6d1bbfcc8cbbf6e8b4c`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 2.2 MB (2238050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2200b2bf3700667dee4ed461f5fc3a146f974b2c0b7248d6de5db91b6e960a07`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 17.1 KB (17145 bytes)  
		MIME: application/vnd.in-toto+json
