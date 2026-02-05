## `julia:rc-trixie`

```console
$ docker pull julia@sha256:50d61a51a8360d5456401353362a7c1578026d1803fdc8c23d970bd30456009f
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
$ docker pull julia@sha256:35ec98e237df82ba9c487d83b3b0657d8b0bc47292dbc2b16c8a662c461bdaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344834012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5af2a53f75a8a28ae2e57848263d1d6dc270a58c66ed63994c99b272decfc45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 17:43:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:44:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Feb 2026 17:44:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:44:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Feb 2026 17:44:05 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Thu, 05 Feb 2026 17:44:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Feb 2026 17:44:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 17:44:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:44:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cb796f00bc0e15257ae20cd14ff4ecf03b74ab04df8f05f5a2d0cf0f3b7ca5`  
		Last Modified: Thu, 05 Feb 2026 17:44:50 GMT  
		Size: 6.2 MB (6243704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3287f962545bb1e2d5b5600127af84ec5b518abcf58dcf147bdc2eb0bd841422`  
		Last Modified: Thu, 05 Feb 2026 17:44:56 GMT  
		Size: 308.8 MB (308811343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87ddf9408c4ae87c056f5a5c11e8d1a4e649d28bcd4ef8fab2f0e5f1372cf33`  
		Last Modified: Thu, 05 Feb 2026 17:44:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:e9802dbb27460be24a25309a1f8e18fce2816603cef1a2edadb665fea3a25571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70bcbf1b6355b0c33c0eeb3459211c76fb1c826da924055977dd6d7e0efd6e1`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8a715fa38623b2fb3e1962218ed9037b6fdd55fc47c43aba5fb5fd332e386`  
		Last Modified: Thu, 05 Feb 2026 17:44:50 GMT  
		Size: 2.2 MB (2240877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3afd9eae9ad8a9848d4f188f02cc5593228c9365472257df267a6961a97f39`  
		Last Modified: Thu, 05 Feb 2026 17:44:50 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3b22eb65535fe16b9ec91e33465e0840e42e921ec9009feb04d47f07c8fae90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369055693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fab4bdcf383ccc2ad77a77131e545446bbf499df2188bc5b5f959caf8398e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 17:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:44:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Feb 2026 17:44:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:44:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Feb 2026 17:44:02 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Thu, 05 Feb 2026 17:44:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Feb 2026 17:44:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 17:44:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:44:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac419fa61bc5225efec588c870db679e5750e3ce638b6cd40973ebca6b6807ba`  
		Last Modified: Thu, 05 Feb 2026 17:44:50 GMT  
		Size: 6.2 MB (6150971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af28520adc84dcc2438af01310ad14ec506e360ec6f20338cb5bac6411e0565d`  
		Last Modified: Thu, 05 Feb 2026 17:44:57 GMT  
		Size: 332.8 MB (332764286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71103492074bdf38e029ecbe1164816c936674b930d3429f43b43ac6a1a0b856`  
		Last Modified: Thu, 05 Feb 2026 17:44:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:4c7a98f8ad758c862661bd94fe423a063eb1fdea91a695f575fb97d98d7563c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713b4f25fdb2de83b3fa7a02ed1be4fb3d6575b89129257f82b426b93667272d`

```dockerfile
```

-	Layers:
	-	`sha256:20b3a51524b762a8891f6e0597a7ae9d42bb6d0afc573ba9d1a4d1d5a6fc232a`  
		Last Modified: Thu, 05 Feb 2026 17:44:50 GMT  
		Size: 2.2 MB (2241185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe4b980ee07e459f24add5ddd8081ca5416aa63c60acade7c769896a80bc879`  
		Last Modified: Thu, 05 Feb 2026 17:44:49 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:cbbd7d8db7a15e5dc80d8d95385b680682cb0e84eea261c019e44143cd4ddf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280689628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207a09eb646169809f017f01cddb7973e5a03b877c9330637979f1b7ad4c28ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 17:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:44:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Feb 2026 17:44:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:44:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Feb 2026 17:44:23 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Thu, 05 Feb 2026 17:44:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Feb 2026 17:44:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 17:44:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:44:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c9a0492e5c85b2eada75f241e70990696105c4719c2709c8a7393d6d3393e8`  
		Last Modified: Thu, 05 Feb 2026 17:44:58 GMT  
		Size: 6.4 MB (6429436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412f1340a6aff8a2ae8da08c828b53b3db82c08005a2d93e7e3b1ba77828f889`  
		Last Modified: Thu, 05 Feb 2026 17:45:03 GMT  
		Size: 243.0 MB (242965966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264e038d1e791c2d235f22fdc9ecd3e290b29032dcbd696948fb3d3fc3f15c4`  
		Last Modified: Thu, 05 Feb 2026 17:44:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ea8cdc764b3729b5e08402a4def95b80a066814f6710d56b8213f858795b9d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afb927c2e6fd58c970910425b0b56b5bc1277f7e302c79d05b582f53aa68f41`

```dockerfile
```

-	Layers:
	-	`sha256:ddc63766577480ca081ed77142f4f36947e7fb2f396cc4f785f318e25f8a2811`  
		Last Modified: Thu, 05 Feb 2026 17:44:58 GMT  
		Size: 2.2 MB (2238012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b98ac7494240179dec6846ddeac7955f8f21fad9f11755a785931c4b15649e4`  
		Last Modified: Thu, 05 Feb 2026 17:44:58 GMT  
		Size: 17.1 KB (17145 bytes)  
		MIME: application/vnd.in-toto+json
