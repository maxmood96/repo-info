## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:92d2112dbb40916655ce75256ee99f93544c9838820bfbeda9f01637b566ac67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:645edf1ffb9ea2d768853d31b53b8b3cef5934e01972ac097cbd26679cc951de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326867929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd44780b3788b3882bab9e78bc19ee193bf87a4d2e7d3c71ebc39b1faab2355c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 25 Apr 2025 23:13:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 25 Apr 2025 23:13:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta2-linux-x86_64.tar.gz'; 			sha256='b7466702ec9ceaaf0565acac7df7c26316a9af3dbb048d01797e71e4dbaaa924'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta2-linux-aarch64.tar.gz'; 			sha256='46c3f128f12fef5b22133b540a9fedbbefb412b23f7b49f1cf278174a2959dd3'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta2-linux-i686.tar.gz'; 			sha256='fddddc7bce50adae38b45fbeb9b05ea2c8062cc20d6dd50d5879c0818cf01c0b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 23:13:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf621d62f34f15facbcad0fec9bf9c674293f36b41c8a390813355e6b40af4`  
		Last Modified: Mon, 28 Apr 2025 21:43:23 GMT  
		Size: 2.4 MB (2426584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167dc74dab8e498afd18e0757be02c51704e9f9b6906c05c8cf27045db993802`  
		Last Modified: Mon, 28 Apr 2025 21:43:28 GMT  
		Size: 294.2 MB (294186370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9de130c46487886b44cfe79b99821a24c07342735c22f16970167b56fbcb246`  
		Last Modified: Mon, 28 Apr 2025 21:43:23 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:08f0ba0d0dba643563ee6edecd8561572104fbecb2f7c8225414a1e23264ca1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21a9a926d9d80833f3a4bc34d0281804b2ded5f868b35764375e1778c15f61f`

```dockerfile
```

-	Layers:
	-	`sha256:71382a091bc8843215bbdf24618f72938f6b5e6ea9d8cd01fb6ab66db4ebcd0a`  
		Last Modified: Mon, 28 Apr 2025 21:43:23 GMT  
		Size: 2.7 MB (2714234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60f96cb3022b7a5e83e9f2dd1760f09c9c01636055577d3fe3120bca01eb6f2`  
		Last Modified: Mon, 28 Apr 2025 21:43:23 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ade3f3d6419d8249ec895c36ff220ee0d48ef10bdf074b0cc6fe13373962e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346372523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13de7df418ad81bebfd5a4d9d58f6ffbe1459755befd410afee6f23adf4db50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 25 Apr 2025 23:13:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta2-linux-x86_64.tar.gz'; 			sha256='b7466702ec9ceaaf0565acac7df7c26316a9af3dbb048d01797e71e4dbaaa924'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta2-linux-aarch64.tar.gz'; 			sha256='46c3f128f12fef5b22133b540a9fedbbefb412b23f7b49f1cf278174a2959dd3'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta2-linux-i686.tar.gz'; 			sha256='fddddc7bce50adae38b45fbeb9b05ea2c8062cc20d6dd50d5879c0818cf01c0b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 23:13:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b76e6f5654c4c2761bc17aaee3994e1d869fe6fda5ecbf1100e5c5192a156c`  
		Last Modified: Tue, 15 Apr 2025 21:55:44 GMT  
		Size: 2.4 MB (2415194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1266a41d0fa257c10cd65206af366de7fe21e7d755d8ea151ecc75097d900866`  
		Last Modified: Mon, 28 Apr 2025 18:22:22 GMT  
		Size: 315.2 MB (315207459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fccd5eaf9d9c1fdc137aba2104885028fb802cc1bcedb6dd7e5ef0c9586b924`  
		Last Modified: Mon, 28 Apr 2025 18:22:15 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:db293bab61822d6246d1694d37330ded763196996ac7aafbd0a3ec851477bb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8de72d9814855d20def8937644e55e9e2f40a5741726af7610185f0338641`

```dockerfile
```

-	Layers:
	-	`sha256:c4e098cfa5d49f1579189799895a13a183b407a6c9c27ca366d76872ef4cd4f9`  
		Last Modified: Mon, 28 Apr 2025 18:22:15 GMT  
		Size: 2.7 MB (2714431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:400b599777be39163b6a125c0b29de1caf31480802a13eabad5853463b76e99a`  
		Last Modified: Mon, 28 Apr 2025 18:22:15 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:25fffe61a6772379c39d1106ab09144ee8c07de4eb2965a47e0d13cf8b931bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269746482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbec5812319a177f7151fb13271f97f6719779a6a6ec5063410fe503de40e3f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 25 Apr 2025 23:13:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 25 Apr 2025 23:13:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 25 Apr 2025 23:13:55 GMT
ENV JULIA_VERSION=1.12.0-beta2
# Fri, 25 Apr 2025 23:13:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta2-linux-x86_64.tar.gz'; 			sha256='b7466702ec9ceaaf0565acac7df7c26316a9af3dbb048d01797e71e4dbaaa924'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta2-linux-aarch64.tar.gz'; 			sha256='46c3f128f12fef5b22133b540a9fedbbefb412b23f7b49f1cf278174a2959dd3'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta2-linux-i686.tar.gz'; 			sha256='fddddc7bce50adae38b45fbeb9b05ea2c8062cc20d6dd50d5879c0818cf01c0b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 23:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 23:13:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37025fe1c66d58feeeb0688db83b0802160f67fde9503b9f0fc8f49d35781606`  
		Last Modified: Mon, 28 Apr 2025 21:43:16 GMT  
		Size: 2.5 MB (2533008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeba38af44fedb915234f68ebea2174f094f84dbb4ab938f694db0f11889e5c6`  
		Last Modified: Mon, 28 Apr 2025 21:43:23 GMT  
		Size: 236.0 MB (236025214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4839110f23c1c4e734d101d6f88e15eedd561d80e9eccb6c45fbf0080750da`  
		Last Modified: Mon, 28 Apr 2025 21:43:16 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e29e4dec456c37808570f0c3f09b4c8a8f2cfff1e055953ba3507bc5746dab0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5b12bc8d191588005424b3f5fd52f5d7c95b54007b487fa8b58ba4cb1aea07`

```dockerfile
```

-	Layers:
	-	`sha256:5feccb5b05abf1b98f18e95b9de07e01299a5bb44a88367c8557836cab32ab74`  
		Last Modified: Mon, 28 Apr 2025 21:43:16 GMT  
		Size: 2.7 MB (2711338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f851168891c9a2e40cb3ca03a2d25b6ea67cec3d03e9cb4393fe5a2e0e32ef27`  
		Last Modified: Mon, 28 Apr 2025 21:43:16 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json
