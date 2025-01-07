<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-alpine`](#julia1-alpine)
-	[`julia:1-alpine3.20`](#julia1-alpine320)
-	[`julia:1-alpine3.21`](#julia1-alpine321)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10.7`](#julia1107)
-	[`julia:1.10.7-bookworm`](#julia1107-bookworm)
-	[`julia:1.10.7-bullseye`](#julia1107-bullseye)
-	[`julia:1.10.7-windowsservercore`](#julia1107-windowsservercore)
-	[`julia:1.10.7-windowsservercore-1809`](#julia1107-windowsservercore-1809)
-	[`julia:1.10.7-windowsservercore-ltsc2022`](#julia1107-windowsservercore-ltsc2022)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-alpine`](#julia111-alpine)
-	[`julia:1.11-alpine3.20`](#julia111-alpine320)
-	[`julia:1.11-alpine3.21`](#julia111-alpine321)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11.2`](#julia1112)
-	[`julia:1.11.2-alpine`](#julia1112-alpine)
-	[`julia:1.11.2-alpine3.20`](#julia1112-alpine320)
-	[`julia:1.11.2-alpine3.21`](#julia1112-alpine321)
-	[`julia:1.11.2-bookworm`](#julia1112-bookworm)
-	[`julia:1.11.2-bullseye`](#julia1112-bullseye)
-	[`julia:1.11.2-windowsservercore`](#julia1112-windowsservercore)
-	[`julia:1.11.2-windowsservercore-1809`](#julia1112-windowsservercore-1809)
-	[`julia:1.11.2-windowsservercore-ltsc2022`](#julia1112-windowsservercore-ltsc2022)
-	[`julia:alpine`](#juliaalpine)
-	[`julia:alpine3.20`](#juliaalpine320)
-	[`julia:alpine3.21`](#juliaalpine321)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:170e8401b4265a188bd5f981ea5dcc9c604bfa02d89f054ba2deb28eb6653930
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.20`

```console
$ docker pull julia@sha256:a0d1e60754e7968334173a0fd3fae454be24e2ad91eb57ee7c14aeccfc6f5a19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:4aab52e8513e46d81ce40be84ae6e5cab39340b8bfea20dede7978edf1e5bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294447636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72689465fa12a8fba467e61fdba62ce815b991bf2bbfb17eccc03f72c8396e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f153b9b51f4a623f7c462332c4dc8a97778b1474f292e3b5026a6dc83a3c5e`  
		Last Modified: Tue, 07 Jan 2025 03:20:45 GMT  
		Size: 290.8 MB (290833273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c423ef0e6a199a26aeaebfc65cc5d903e38cdd48f25bafe8dd7061a937aa52b`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:25d841fae1bf7314c44f9a4520e46fc3fcd7144adc4fc76139580058c2ad905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0636e1e9a44e35a4d1c66372e6026d79a5d47b4e8137c916327a47ae735e89c8`

```dockerfile
```

-	Layers:
	-	`sha256:e3cceaf1730b482cc423d00f99d68f023e7e133c32ab4d64e25a4aa17e4a2d90`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fe7e08665f30c655e283c43a74233c43ae52f3ae5a7a22d760679775edd95d`  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.21`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:285a3bae293b2792a5913dbc9f65ea83dfdca15c1bcd0874aabcce6a37800cb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:cd8f32ca639f35a85945561fd1295e05e21c9a905b3062324cc2c0da8439fe7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:5a97cdb7d45113e5113507875bc487d083c3635074a48880b552a64a5eecbfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18821a62c1d8618dc5df89692a96601d27bceccd77cdbff4d97969debd5dac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8881345e71d9bcc70bf3887b3d2332ddf2479459f8c5947061739acd90809f3`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.2 MB (2222681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b883d5f544de0d007a117979564a6dd5d99891dc767265dd4c580f6dc4802`  
		Last Modified: Tue, 24 Dec 2024 22:18:37 GMT  
		Size: 288.5 MB (288487930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548c5b42027516b21f101149d293ea00da9f37c545eb12991c5608f13823911`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5a6c8b42ec2931eb1e855f9bae5715f2fce5a49746859eec0af0158744931352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a04d02394fd49887693719ff1e147ca3703742ce8465d8dcc7d570af6eaeec`

```dockerfile
```

-	Layers:
	-	`sha256:dac735d67bc50567ef4bc58c46aaea627c9e12b539ca5c507a3b754e4b1c9620`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9b00da95435cf5ebac668793035b35d292f81944d530686cad44bda20444d4`  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d6c7077f28d26f09b3fdfa159bea7c9c2a5aa12c2e4534a3924500b4519f7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7bb7a4817f0e1f12b035b1524c4900a38d8e81de33d40b55239d6d4842112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b30040d42393764b30ee9fe0d7df28a5e4284ae841d1b33ad33c5b50d64937`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.2 MB (2210269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6895e19b215321cca937d71be96dd81493a7191bbc9a63a0b1ca2e3fa210deb`  
		Last Modified: Tue, 24 Dec 2024 22:57:13 GMT  
		Size: 303.7 MB (303658749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84195d59fc25b7d8e1ef832bafd320be00083bb82610bccfbb9ebdc675a0099f`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e99994c50ba3dfdbe3e87e78d6a3898fdcddda2def2ef3c45a5ca744b3991230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358464a318dcdc1a2534fc8496f82968f2b5946abad3603d3125c48cfcef08ab`

```dockerfile
```

-	Layers:
	-	`sha256:303b41587b13e532e459b7a32ec1264fb48b584e7bf56bb6dba6ad895478bd78`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682ecaf251bf124c14cb279f9c415d1fe6c4c561c06620d5ad01925bf2779a9c`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:45a93e591281b1425ab4f38bc8ae3c6bf69f269b1085fdcaaf58f626ea9bbcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e75bdf641a5771324e59f7710367a8f433ad06516a860191ec651a2cc23876b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf450fc4bceff1e049c9ac3f4c6fb6f2c805c3cb9802cb678ede551f8271778`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.3 MB (2328070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e594f1817abc00a10b99af5a0911549589f2ebd18e7d714ac6836babea10dd7`  
		Last Modified: Tue, 24 Dec 2024 22:14:47 GMT  
		Size: 237.1 MB (237136266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03efcc14fabc0f7d32eecb671c9eefeb19af19b8e8f7d90394b4918069423714`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e4eb7480f72a41ee5b43acd058a12d398b98631b569cd611e23941105904e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3072085890e77d746e2fd968972f8bd7c6c8884aecfdfd494c9ce20bfda47b`

```dockerfile
```

-	Layers:
	-	`sha256:053737e018dedc63ec680f88496205b5fb15ecba4e08cd9b44430454b72e975f`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e622e1cb2156c68ad61d1d30382a279bea2babe409704a847fee4cbfc019cb0e`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:b7f4fde7cba6946455f9522b2702cca96d9be2a665735bdb146a4c62e6f2e91e
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:5334bd17dbc23b1c2c65f905faa17c95a06ff327463c2c858e9b78edc52beb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a6ffe1c3315bdcd160733487f4e4de6de621e35229229605a69e5e5a3a52e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493f24aca2e1da7b662bb03deabfcef416dd2f1fc6f5a0f0e993a617a18f0e3`  
		Size: 5.5 MB (5518309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e35c3cd0f95eb71a8c856d1f180a404d3b7e97607e54b8c1e367584a0df890`  
		Last Modified: Tue, 24 Dec 2024 22:18:02 GMT  
		Size: 175.9 MB (175894804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2c97bfba2ef354f855891362d2074b0ebdcea9f78ee733d9d7e672324b6e09`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:5803fe8921fe1d4317bf3fb7b1093895c3bac03396a57eaf807abf5e9ae60135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4559c7f7a184100a140e64f1f202ea1ca8dcc20ad6b6b3936ffc02d5f4dcdcca`

```dockerfile
```

-	Layers:
	-	`sha256:f4abe01871aaec592280cff88f354d5e0700a44392c638c568bf79ba6eadb12e`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f95993ce599b12da49f14d8b5efdf25ffcb2a4835f761a177c974f6dbe0aa7`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:cd9da175de2eb95b4a72eee08e36d9cffd274e3881861c0cc442b73bae7d4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efa32c612f48f78d76a71ae1761faddf7ec08fae3493c96e74a521b7c20af8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d2c29914595d8187eee7071dc8c44af42d77e495059b5e83d1ccd323877f0`  
		Size: 177.7 MB (177651972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3e04f829abd55952f0e58a23b4827dabec30f2f78768b415dd94536ca06464`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:1315448360906603e976e4f88f5458b159e10a6717a4c25b4d75f98059681bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e13ae8cddfdaa87f098e7587eaa3f74497b3e49a0fb519ca82ef787dd60dfbb`

```dockerfile
```

-	Layers:
	-	`sha256:1dc241a497ec2fc17f9413b9bca1cc2b1090fc85345f09b5efc17777580b9ae2`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7677f6dd5a320a93736828c8ececfd857d679976102aee3e9922a3539ef265d`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:d200f6842f12a2973d6691fd74760502d49709f79701f9549b93488daefaaeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5872bf8a9ed5a222717abf54abd55a3c634bad7d20e04fafa0344bf9c268a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1f46476895e069ff57f9962ec718e0b8737a7769a9d235cfe398ea8fa301f`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 5.7 MB (5679235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157462030691e775ff2db87b80e7b1bed5020ea67cf6e222ec7f73901a67e4d1`  
		Last Modified: Tue, 24 Dec 2024 22:14:30 GMT  
		Size: 157.8 MB (157784892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad18fba3f2d80d356f9de6085b60d8f9c80ec40069adce4fd1b709787538202`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:2f40498d48370569f8079d1c404d9047c98954a45603532622c109e00f3cb069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9466b7efbc0bb633b48a9cc0e27ddd7e77694f04623abdd351fa632b2713d367`

```dockerfile
```

-	Layers:
	-	`sha256:ac8266adece51f1e543201833fa8a1eb062a80fcca0177c7286254ac9f55dc88`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da95133cf296dfd2d52c3579a4de79a8932e53482d4716b681fcc1bd26714012`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:3cf5c361f7b5bd860e971ecbfa2f212f4b3b5b6bac17e1dbcfd4848edbf2e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12084d4008549f70b5aa52f439d1e37c2a1347c15d3c8f2589c5054946b0caca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0045525092dfb1ee4c2ed6fc940c1fedc48f41582bddb05957a83bf75955be9e`  
		Last Modified: Wed, 25 Dec 2024 04:13:58 GMT  
		Size: 155.5 MB (155493227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc06b1ae1dcef3a86056a919faa99b1edf34464ddd6ada6dfb01f2c11a163d`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:368b3a949028a51a8bdbbd72ac7dafd0574699ab0183afd84ea287116f81a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46698696df1f658f639dae5a2189e97639005df5cb8ec7e2633c3fc95a9f949`

```dockerfile
```

-	Layers:
	-	`sha256:e75c172b78ce821c12f8bc1fa90cdb023240b838e1f5c99f19cf0603a63c0b69`  
		Last Modified: Wed, 25 Dec 2024 04:13:54 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f0cd5d14331b41739f9969a7bd4eb5f616fd9f52075daee31c2a36111be3dc`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Wed, 11 Dec 2024 20:39:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Wed, 11 Dec 2024 20:39:57 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Wed, 11 Dec 2024 20:38:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Wed, 11 Dec 2024 20:39:00 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:d6f8128446dc566d8c1eaf407f6e47dc8cbf5989add7d45cff015b0b63b988b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:5334bd17dbc23b1c2c65f905faa17c95a06ff327463c2c858e9b78edc52beb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a6ffe1c3315bdcd160733487f4e4de6de621e35229229605a69e5e5a3a52e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493f24aca2e1da7b662bb03deabfcef416dd2f1fc6f5a0f0e993a617a18f0e3`  
		Size: 5.5 MB (5518309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e35c3cd0f95eb71a8c856d1f180a404d3b7e97607e54b8c1e367584a0df890`  
		Last Modified: Tue, 24 Dec 2024 22:18:02 GMT  
		Size: 175.9 MB (175894804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2c97bfba2ef354f855891362d2074b0ebdcea9f78ee733d9d7e672324b6e09`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5803fe8921fe1d4317bf3fb7b1093895c3bac03396a57eaf807abf5e9ae60135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4559c7f7a184100a140e64f1f202ea1ca8dcc20ad6b6b3936ffc02d5f4dcdcca`

```dockerfile
```

-	Layers:
	-	`sha256:f4abe01871aaec592280cff88f354d5e0700a44392c638c568bf79ba6eadb12e`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f95993ce599b12da49f14d8b5efdf25ffcb2a4835f761a177c974f6dbe0aa7`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:cd9da175de2eb95b4a72eee08e36d9cffd274e3881861c0cc442b73bae7d4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efa32c612f48f78d76a71ae1761faddf7ec08fae3493c96e74a521b7c20af8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d2c29914595d8187eee7071dc8c44af42d77e495059b5e83d1ccd323877f0`  
		Size: 177.7 MB (177651972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3e04f829abd55952f0e58a23b4827dabec30f2f78768b415dd94536ca06464`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1315448360906603e976e4f88f5458b159e10a6717a4c25b4d75f98059681bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e13ae8cddfdaa87f098e7587eaa3f74497b3e49a0fb519ca82ef787dd60dfbb`

```dockerfile
```

-	Layers:
	-	`sha256:1dc241a497ec2fc17f9413b9bca1cc2b1090fc85345f09b5efc17777580b9ae2`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7677f6dd5a320a93736828c8ececfd857d679976102aee3e9922a3539ef265d`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d200f6842f12a2973d6691fd74760502d49709f79701f9549b93488daefaaeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5872bf8a9ed5a222717abf54abd55a3c634bad7d20e04fafa0344bf9c268a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1f46476895e069ff57f9962ec718e0b8737a7769a9d235cfe398ea8fa301f`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 5.7 MB (5679235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157462030691e775ff2db87b80e7b1bed5020ea67cf6e222ec7f73901a67e4d1`  
		Last Modified: Tue, 24 Dec 2024 22:14:30 GMT  
		Size: 157.8 MB (157784892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad18fba3f2d80d356f9de6085b60d8f9c80ec40069adce4fd1b709787538202`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2f40498d48370569f8079d1c404d9047c98954a45603532622c109e00f3cb069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9466b7efbc0bb633b48a9cc0e27ddd7e77694f04623abdd351fa632b2713d367`

```dockerfile
```

-	Layers:
	-	`sha256:ac8266adece51f1e543201833fa8a1eb062a80fcca0177c7286254ac9f55dc88`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da95133cf296dfd2d52c3579a4de79a8932e53482d4716b681fcc1bd26714012`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3cf5c361f7b5bd860e971ecbfa2f212f4b3b5b6bac17e1dbcfd4848edbf2e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12084d4008549f70b5aa52f439d1e37c2a1347c15d3c8f2589c5054946b0caca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0045525092dfb1ee4c2ed6fc940c1fedc48f41582bddb05957a83bf75955be9e`  
		Last Modified: Wed, 25 Dec 2024 04:13:58 GMT  
		Size: 155.5 MB (155493227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc06b1ae1dcef3a86056a919faa99b1edf34464ddd6ada6dfb01f2c11a163d`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:368b3a949028a51a8bdbbd72ac7dafd0574699ab0183afd84ea287116f81a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46698696df1f658f639dae5a2189e97639005df5cb8ec7e2633c3fc95a9f949`

```dockerfile
```

-	Layers:
	-	`sha256:e75c172b78ce821c12f8bc1fa90cdb023240b838e1f5c99f19cf0603a63c0b69`  
		Last Modified: Wed, 25 Dec 2024 04:13:54 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f0cd5d14331b41739f9969a7bd4eb5f616fd9f52075daee31c2a36111be3dc`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:b8bf719f7c769b21bf5ba060d29a67347ed029b73a8406283a78fb02cb30d8a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8b2ac6b41109a91c5aa740f04cd85458de723862674d94a6f768a72bc3f63016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b6ab0c7f11f64505741e69d522ee1b032fbdd75aa3270c427b665e592a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7c1c61055330586c07a16ddc182b94ea57bb175aeb4386b117f109c3f0c05`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 2.2 MB (2222648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf95a703ca17058d729bf3997059808f229b4e703370d555fce9fe0d6938a4a7`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 175.9 MB (175895651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f0ba78270f77435139776cc9880b8aa4ad59f3203ad4a520d0492d36e9e974`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d07f02fd9d66e791c522bc77f1f327f4155fd1f85ecef814ecbea1dc5476546f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6140b3354e0179a8304f38e523b069b4f55e63e451aaf6465ebacb40751f9f0d`

```dockerfile
```

-	Layers:
	-	`sha256:2a312ca6fc53c4cfb3375b4bcbfba02c8f1b523a7a9b8ff9b9078b35c5df9874`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0e599dca69a7cbb00e150d5949341b12a035d581184a9c1a3158e4534a83eb`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:86a515171554b7122c107f0bce76f10ef2a71c5d368b9b2e73b3d7bd5f7e5b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e9f062882b979f95189d7af5a6812e6183a0378fbba8f459d6329032d5b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b30040d42393764b30ee9fe0d7df28a5e4284ae841d1b33ad33c5b50d64937`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.2 MB (2210269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b424ad335e3be4bc60efb5b1f8f511112526ffe730b614b31075a218732ff1db`  
		Last Modified: Tue, 24 Dec 2024 22:59:15 GMT  
		Size: 177.7 MB (177651898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdf994c301242a3b81de97783bfa31f6fade4c0745ef80e343373e49a5a64f4`  
		Last Modified: Tue, 24 Dec 2024 22:59:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0b504e1bbb232351126c93080954bc10dc8629773d8f0a1acfe11e7ddcdbc7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cffbdbf993a2f32accdef0b692fa8758d9bd1edffeb8345c79ea466cb64c1af`

```dockerfile
```

-	Layers:
	-	`sha256:dcfad358101bc29422457dba604d89d8b3fae6b7a19071073e34af5ad7e182c5`  
		Last Modified: Tue, 24 Dec 2024 22:59:11 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1ac59b8840cf0fdebe1442c39a85b6f6428877f26112f0e83b69947afe90c5`  
		Last Modified: Tue, 24 Dec 2024 22:59:11 GMT  
		Size: 16.7 KB (16720 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:1ab8307feb509654d0ac95f1bba6cc8dc9e84cd02a082863a4db23f8c6959af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91c1f94f93dc31611a14169e74333041b6066e20f9295316e783eccc3c6d019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db8525b71f938f145f448a438c7a3f1df3d9641f29006c667fcb900fe087f0e`  
		Last Modified: Tue, 24 Dec 2024 22:14:27 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbf49bdffe3ff9bdeeec1c560da926b7c0009e0e954afcce5cd1d79b02df60e`  
		Last Modified: Tue, 24 Dec 2024 22:14:31 GMT  
		Size: 157.8 MB (157784821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8399591e1a7a4b9f9973f07acd013e44a434dc93f353d72097905bc13edf45`  
		Last Modified: Tue, 24 Dec 2024 22:14:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:72a018d780b3add0cc2d01b8ddebe6b3af71322b38f7873fb824d15831bf07b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd2f75137f577fc59fcb3a52e0b0ac8c4a460030b2be0cc42b0c07d0fd1826`

```dockerfile
```

-	Layers:
	-	`sha256:f0401557bb813f42252ac86b742ad67cfd4e51356a6b9642280a8094e7203a8c`  
		Last Modified: Tue, 24 Dec 2024 22:14:28 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9b6c05a37a8b79a0176c56f489ede2a825b3b59a5a881f05e5baa61c59afbc`  
		Last Modified: Tue, 24 Dec 2024 22:14:27 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:079eb9a75382cf1e65691ee7a837961f549e71a42f5475f72bbaaca2ffd12306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Wed, 11 Dec 2024 20:39:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Wed, 11 Dec 2024 20:39:57 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Wed, 11 Dec 2024 20:38:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Wed, 11 Dec 2024 20:39:00 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:bb2bc3e84f5cc89b10bf6764d626eea3f27071788bed326ec896dc70dc009db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Wed, 11 Dec 2024 20:38:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Wed, 11 Dec 2024 20:39:00 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:c8dc5bad2f3491515a7f125757486f9992622121c585cfe77945cef34b8e5d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Wed, 11 Dec 2024 20:39:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Wed, 11 Dec 2024 20:39:57 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7`

```console
$ docker pull julia@sha256:b7f4fde7cba6946455f9522b2702cca96d9be2a665735bdb146a4c62e6f2e91e
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10.7` - linux; amd64

```console
$ docker pull julia@sha256:5334bd17dbc23b1c2c65f905faa17c95a06ff327463c2c858e9b78edc52beb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a6ffe1c3315bdcd160733487f4e4de6de621e35229229605a69e5e5a3a52e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493f24aca2e1da7b662bb03deabfcef416dd2f1fc6f5a0f0e993a617a18f0e3`  
		Size: 5.5 MB (5518309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e35c3cd0f95eb71a8c856d1f180a404d3b7e97607e54b8c1e367584a0df890`  
		Last Modified: Tue, 24 Dec 2024 22:18:02 GMT  
		Size: 175.9 MB (175894804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2c97bfba2ef354f855891362d2074b0ebdcea9f78ee733d9d7e672324b6e09`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:5803fe8921fe1d4317bf3fb7b1093895c3bac03396a57eaf807abf5e9ae60135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4559c7f7a184100a140e64f1f202ea1ca8dcc20ad6b6b3936ffc02d5f4dcdcca`

```dockerfile
```

-	Layers:
	-	`sha256:f4abe01871aaec592280cff88f354d5e0700a44392c638c568bf79ba6eadb12e`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f95993ce599b12da49f14d8b5efdf25ffcb2a4835f761a177c974f6dbe0aa7`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:cd9da175de2eb95b4a72eee08e36d9cffd274e3881861c0cc442b73bae7d4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efa32c612f48f78d76a71ae1761faddf7ec08fae3493c96e74a521b7c20af8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d2c29914595d8187eee7071dc8c44af42d77e495059b5e83d1ccd323877f0`  
		Size: 177.7 MB (177651972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3e04f829abd55952f0e58a23b4827dabec30f2f78768b415dd94536ca06464`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:1315448360906603e976e4f88f5458b159e10a6717a4c25b4d75f98059681bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e13ae8cddfdaa87f098e7587eaa3f74497b3e49a0fb519ca82ef787dd60dfbb`

```dockerfile
```

-	Layers:
	-	`sha256:1dc241a497ec2fc17f9413b9bca1cc2b1090fc85345f09b5efc17777580b9ae2`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7677f6dd5a320a93736828c8ececfd857d679976102aee3e9922a3539ef265d`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; 386

```console
$ docker pull julia@sha256:d200f6842f12a2973d6691fd74760502d49709f79701f9549b93488daefaaeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5872bf8a9ed5a222717abf54abd55a3c634bad7d20e04fafa0344bf9c268a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1f46476895e069ff57f9962ec718e0b8737a7769a9d235cfe398ea8fa301f`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 5.7 MB (5679235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157462030691e775ff2db87b80e7b1bed5020ea67cf6e222ec7f73901a67e4d1`  
		Last Modified: Tue, 24 Dec 2024 22:14:30 GMT  
		Size: 157.8 MB (157784892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad18fba3f2d80d356f9de6085b60d8f9c80ec40069adce4fd1b709787538202`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:2f40498d48370569f8079d1c404d9047c98954a45603532622c109e00f3cb069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9466b7efbc0bb633b48a9cc0e27ddd7e77694f04623abdd351fa632b2713d367`

```dockerfile
```

-	Layers:
	-	`sha256:ac8266adece51f1e543201833fa8a1eb062a80fcca0177c7286254ac9f55dc88`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da95133cf296dfd2d52c3579a4de79a8932e53482d4716b681fcc1bd26714012`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; ppc64le

```console
$ docker pull julia@sha256:3cf5c361f7b5bd860e971ecbfa2f212f4b3b5b6bac17e1dbcfd4848edbf2e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12084d4008549f70b5aa52f439d1e37c2a1347c15d3c8f2589c5054946b0caca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0045525092dfb1ee4c2ed6fc940c1fedc48f41582bddb05957a83bf75955be9e`  
		Last Modified: Wed, 25 Dec 2024 04:13:58 GMT  
		Size: 155.5 MB (155493227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc06b1ae1dcef3a86056a919faa99b1edf34464ddd6ada6dfb01f2c11a163d`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:368b3a949028a51a8bdbbd72ac7dafd0574699ab0183afd84ea287116f81a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46698696df1f658f639dae5a2189e97639005df5cb8ec7e2633c3fc95a9f949`

```dockerfile
```

-	Layers:
	-	`sha256:e75c172b78ce821c12f8bc1fa90cdb023240b838e1f5c99f19cf0603a63c0b69`  
		Last Modified: Wed, 25 Dec 2024 04:13:54 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f0cd5d14331b41739f9969a7bd4eb5f616fd9f52075daee31c2a36111be3dc`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Wed, 11 Dec 2024 20:39:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Wed, 11 Dec 2024 20:39:57 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Wed, 11 Dec 2024 20:38:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Wed, 11 Dec 2024 20:39:00 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-bookworm`

```console
$ docker pull julia@sha256:d6f8128446dc566d8c1eaf407f6e47dc8cbf5989add7d45cff015b0b63b988b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10.7-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:5334bd17dbc23b1c2c65f905faa17c95a06ff327463c2c858e9b78edc52beb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a6ffe1c3315bdcd160733487f4e4de6de621e35229229605a69e5e5a3a52e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493f24aca2e1da7b662bb03deabfcef416dd2f1fc6f5a0f0e993a617a18f0e3`  
		Size: 5.5 MB (5518309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e35c3cd0f95eb71a8c856d1f180a404d3b7e97607e54b8c1e367584a0df890`  
		Last Modified: Tue, 24 Dec 2024 22:18:02 GMT  
		Size: 175.9 MB (175894804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2c97bfba2ef354f855891362d2074b0ebdcea9f78ee733d9d7e672324b6e09`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5803fe8921fe1d4317bf3fb7b1093895c3bac03396a57eaf807abf5e9ae60135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4559c7f7a184100a140e64f1f202ea1ca8dcc20ad6b6b3936ffc02d5f4dcdcca`

```dockerfile
```

-	Layers:
	-	`sha256:f4abe01871aaec592280cff88f354d5e0700a44392c638c568bf79ba6eadb12e`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f95993ce599b12da49f14d8b5efdf25ffcb2a4835f761a177c974f6dbe0aa7`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:cd9da175de2eb95b4a72eee08e36d9cffd274e3881861c0cc442b73bae7d4315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efa32c612f48f78d76a71ae1761faddf7ec08fae3493c96e74a521b7c20af8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d2c29914595d8187eee7071dc8c44af42d77e495059b5e83d1ccd323877f0`  
		Size: 177.7 MB (177651972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3e04f829abd55952f0e58a23b4827dabec30f2f78768b415dd94536ca06464`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1315448360906603e976e4f88f5458b159e10a6717a4c25b4d75f98059681bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e13ae8cddfdaa87f098e7587eaa3f74497b3e49a0fb519ca82ef787dd60dfbb`

```dockerfile
```

-	Layers:
	-	`sha256:1dc241a497ec2fc17f9413b9bca1cc2b1090fc85345f09b5efc17777580b9ae2`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7677f6dd5a320a93736828c8ececfd857d679976102aee3e9922a3539ef265d`  
		Last Modified: Tue, 24 Dec 2024 22:58:16 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d200f6842f12a2973d6691fd74760502d49709f79701f9549b93488daefaaeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5872bf8a9ed5a222717abf54abd55a3c634bad7d20e04fafa0344bf9c268a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1f46476895e069ff57f9962ec718e0b8737a7769a9d235cfe398ea8fa301f`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 5.7 MB (5679235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157462030691e775ff2db87b80e7b1bed5020ea67cf6e222ec7f73901a67e4d1`  
		Last Modified: Tue, 24 Dec 2024 22:14:30 GMT  
		Size: 157.8 MB (157784892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad18fba3f2d80d356f9de6085b60d8f9c80ec40069adce4fd1b709787538202`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2f40498d48370569f8079d1c404d9047c98954a45603532622c109e00f3cb069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9466b7efbc0bb633b48a9cc0e27ddd7e77694f04623abdd351fa632b2713d367`

```dockerfile
```

-	Layers:
	-	`sha256:ac8266adece51f1e543201833fa8a1eb062a80fcca0177c7286254ac9f55dc88`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da95133cf296dfd2d52c3579a4de79a8932e53482d4716b681fcc1bd26714012`  
		Last Modified: Tue, 24 Dec 2024 22:14:26 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3cf5c361f7b5bd860e971ecbfa2f212f4b3b5b6bac17e1dbcfd4848edbf2e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12084d4008549f70b5aa52f439d1e37c2a1347c15d3c8f2589c5054946b0caca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0045525092dfb1ee4c2ed6fc940c1fedc48f41582bddb05957a83bf75955be9e`  
		Last Modified: Wed, 25 Dec 2024 04:13:58 GMT  
		Size: 155.5 MB (155493227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fc06b1ae1dcef3a86056a919faa99b1edf34464ddd6ada6dfb01f2c11a163d`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:368b3a949028a51a8bdbbd72ac7dafd0574699ab0183afd84ea287116f81a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46698696df1f658f639dae5a2189e97639005df5cb8ec7e2633c3fc95a9f949`

```dockerfile
```

-	Layers:
	-	`sha256:e75c172b78ce821c12f8bc1fa90cdb023240b838e1f5c99f19cf0603a63c0b69`  
		Last Modified: Wed, 25 Dec 2024 04:13:54 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f0cd5d14331b41739f9969a7bd4eb5f616fd9f52075daee31c2a36111be3dc`  
		Last Modified: Wed, 25 Dec 2024 04:13:53 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-bullseye`

```console
$ docker pull julia@sha256:b8bf719f7c769b21bf5ba060d29a67347ed029b73a8406283a78fb02cb30d8a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.7-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:8b2ac6b41109a91c5aa740f04cd85458de723862674d94a6f768a72bc3f63016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b6ab0c7f11f64505741e69d522ee1b032fbdd75aa3270c427b665e592a373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7c1c61055330586c07a16ddc182b94ea57bb175aeb4386b117f109c3f0c05`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 2.2 MB (2222648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf95a703ca17058d729bf3997059808f229b4e703370d555fce9fe0d6938a4a7`  
		Last Modified: Tue, 24 Dec 2024 22:18:00 GMT  
		Size: 175.9 MB (175895651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f0ba78270f77435139776cc9880b8aa4ad59f3203ad4a520d0492d36e9e974`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d07f02fd9d66e791c522bc77f1f327f4155fd1f85ecef814ecbea1dc5476546f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6140b3354e0179a8304f38e523b069b4f55e63e451aaf6465ebacb40751f9f0d`

```dockerfile
```

-	Layers:
	-	`sha256:2a312ca6fc53c4cfb3375b4bcbfba02c8f1b523a7a9b8ff9b9078b35c5df9874`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0e599dca69a7cbb00e150d5949341b12a035d581184a9c1a3158e4534a83eb`  
		Last Modified: Tue, 24 Dec 2024 22:17:58 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:86a515171554b7122c107f0bce76f10ef2a71c5d368b9b2e73b3d7bd5f7e5b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e9f062882b979f95189d7af5a6812e6183a0378fbba8f459d6329032d5b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b30040d42393764b30ee9fe0d7df28a5e4284ae841d1b33ad33c5b50d64937`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.2 MB (2210269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b424ad335e3be4bc60efb5b1f8f511112526ffe730b614b31075a218732ff1db`  
		Last Modified: Tue, 24 Dec 2024 22:59:15 GMT  
		Size: 177.7 MB (177651898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdf994c301242a3b81de97783bfa31f6fade4c0745ef80e343373e49a5a64f4`  
		Last Modified: Tue, 24 Dec 2024 22:59:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0b504e1bbb232351126c93080954bc10dc8629773d8f0a1acfe11e7ddcdbc7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cffbdbf993a2f32accdef0b692fa8758d9bd1edffeb8345c79ea466cb64c1af`

```dockerfile
```

-	Layers:
	-	`sha256:dcfad358101bc29422457dba604d89d8b3fae6b7a19071073e34af5ad7e182c5`  
		Last Modified: Tue, 24 Dec 2024 22:59:11 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1ac59b8840cf0fdebe1442c39a85b6f6428877f26112f0e83b69947afe90c5`  
		Last Modified: Tue, 24 Dec 2024 22:59:11 GMT  
		Size: 16.7 KB (16720 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:1ab8307feb509654d0ac95f1bba6cc8dc9e84cd02a082863a4db23f8c6959af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91c1f94f93dc31611a14169e74333041b6066e20f9295316e783eccc3c6d019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db8525b71f938f145f448a438c7a3f1df3d9641f29006c667fcb900fe087f0e`  
		Last Modified: Tue, 24 Dec 2024 22:14:27 GMT  
		Size: 2.3 MB (2328090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbf49bdffe3ff9bdeeec1c560da926b7c0009e0e954afcce5cd1d79b02df60e`  
		Last Modified: Tue, 24 Dec 2024 22:14:31 GMT  
		Size: 157.8 MB (157784821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8399591e1a7a4b9f9973f07acd013e44a434dc93f353d72097905bc13edf45`  
		Last Modified: Tue, 24 Dec 2024 22:14:27 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:72a018d780b3add0cc2d01b8ddebe6b3af71322b38f7873fb824d15831bf07b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd2f75137f577fc59fcb3a52e0b0ac8c4a460030b2be0cc42b0c07d0fd1826`

```dockerfile
```

-	Layers:
	-	`sha256:f0401557bb813f42252ac86b742ad67cfd4e51356a6b9642280a8094e7203a8c`  
		Last Modified: Tue, 24 Dec 2024 22:14:28 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9b6c05a37a8b79a0176c56f489ede2a825b3b59a5a881f05e5baa61c59afbc`  
		Last Modified: Tue, 24 Dec 2024 22:14:27 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-windowsservercore`

```console
$ docker pull julia@sha256:079eb9a75382cf1e65691ee7a837961f549e71a42f5475f72bbaaca2ffd12306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10.7-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Wed, 11 Dec 2024 20:39:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Wed, 11 Dec 2024 20:39:57 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Wed, 11 Dec 2024 20:38:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Wed, 11 Dec 2024 20:39:00 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:bb2bc3e84f5cc89b10bf6764d626eea3f27071788bed326ec896dc70dc009db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10.7-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Wed, 11 Dec 2024 20:38:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Wed, 11 Dec 2024 20:39:00 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Wed, 11 Dec 2024 20:38:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:c8dc5bad2f3491515a7f125757486f9992622121c585cfe77945cef34b8e5d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.10.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Wed, 11 Dec 2024 20:39:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Wed, 11 Dec 2024 20:39:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Wed, 11 Dec 2024 20:39:57 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:170e8401b4265a188bd5f981ea5dcc9c604bfa02d89f054ba2deb28eb6653930
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-alpine`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11-alpine` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-alpine3.20`

```console
$ docker pull julia@sha256:a0d1e60754e7968334173a0fd3fae454be24e2ad91eb57ee7c14aeccfc6f5a19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:4aab52e8513e46d81ce40be84ae6e5cab39340b8bfea20dede7978edf1e5bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294447636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72689465fa12a8fba467e61fdba62ce815b991bf2bbfb17eccc03f72c8396e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f153b9b51f4a623f7c462332c4dc8a97778b1474f292e3b5026a6dc83a3c5e`  
		Last Modified: Tue, 07 Jan 2025 03:20:45 GMT  
		Size: 290.8 MB (290833273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c423ef0e6a199a26aeaebfc65cc5d903e38cdd48f25bafe8dd7061a937aa52b`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:25d841fae1bf7314c44f9a4520e46fc3fcd7144adc4fc76139580058c2ad905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0636e1e9a44e35a4d1c66372e6026d79a5d47b4e8137c916327a47ae735e89c8`

```dockerfile
```

-	Layers:
	-	`sha256:e3cceaf1730b482cc423d00f99d68f023e7e133c32ab4d64e25a4aa17e4a2d90`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fe7e08665f30c655e283c43a74233c43ae52f3ae5a7a22d760679775edd95d`  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-alpine3.21`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:285a3bae293b2792a5913dbc9f65ea83dfdca15c1bcd0874aabcce6a37800cb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:cd8f32ca639f35a85945561fd1295e05e21c9a905b3062324cc2c0da8439fe7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:5a97cdb7d45113e5113507875bc487d083c3635074a48880b552a64a5eecbfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18821a62c1d8618dc5df89692a96601d27bceccd77cdbff4d97969debd5dac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8881345e71d9bcc70bf3887b3d2332ddf2479459f8c5947061739acd90809f3`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.2 MB (2222681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b883d5f544de0d007a117979564a6dd5d99891dc767265dd4c580f6dc4802`  
		Last Modified: Tue, 24 Dec 2024 22:18:37 GMT  
		Size: 288.5 MB (288487930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548c5b42027516b21f101149d293ea00da9f37c545eb12991c5608f13823911`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5a6c8b42ec2931eb1e855f9bae5715f2fce5a49746859eec0af0158744931352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a04d02394fd49887693719ff1e147ca3703742ce8465d8dcc7d570af6eaeec`

```dockerfile
```

-	Layers:
	-	`sha256:dac735d67bc50567ef4bc58c46aaea627c9e12b539ca5c507a3b754e4b1c9620`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9b00da95435cf5ebac668793035b35d292f81944d530686cad44bda20444d4`  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d6c7077f28d26f09b3fdfa159bea7c9c2a5aa12c2e4534a3924500b4519f7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7bb7a4817f0e1f12b035b1524c4900a38d8e81de33d40b55239d6d4842112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b30040d42393764b30ee9fe0d7df28a5e4284ae841d1b33ad33c5b50d64937`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.2 MB (2210269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6895e19b215321cca937d71be96dd81493a7191bbc9a63a0b1ca2e3fa210deb`  
		Last Modified: Tue, 24 Dec 2024 22:57:13 GMT  
		Size: 303.7 MB (303658749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84195d59fc25b7d8e1ef832bafd320be00083bb82610bccfbb9ebdc675a0099f`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e99994c50ba3dfdbe3e87e78d6a3898fdcddda2def2ef3c45a5ca744b3991230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358464a318dcdc1a2534fc8496f82968f2b5946abad3603d3125c48cfcef08ab`

```dockerfile
```

-	Layers:
	-	`sha256:303b41587b13e532e459b7a32ec1264fb48b584e7bf56bb6dba6ad895478bd78`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682ecaf251bf124c14cb279f9c415d1fe6c4c561c06620d5ad01925bf2779a9c`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:45a93e591281b1425ab4f38bc8ae3c6bf69f269b1085fdcaaf58f626ea9bbcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e75bdf641a5771324e59f7710367a8f433ad06516a860191ec651a2cc23876b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf450fc4bceff1e049c9ac3f4c6fb6f2c805c3cb9802cb678ede551f8271778`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.3 MB (2328070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e594f1817abc00a10b99af5a0911549589f2ebd18e7d714ac6836babea10dd7`  
		Last Modified: Tue, 24 Dec 2024 22:14:47 GMT  
		Size: 237.1 MB (237136266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03efcc14fabc0f7d32eecb671c9eefeb19af19b8e8f7d90394b4918069423714`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e4eb7480f72a41ee5b43acd058a12d398b98631b569cd611e23941105904e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3072085890e77d746e2fd968972f8bd7c6c8884aecfdfd494c9ce20bfda47b`

```dockerfile
```

-	Layers:
	-	`sha256:053737e018dedc63ec680f88496205b5fb15ecba4e08cd9b44430454b72e975f`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e622e1cb2156c68ad61d1d30382a279bea2babe409704a847fee4cbfc019cb0e`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2`

```console
$ docker pull julia@sha256:170e8401b4265a188bd5f981ea5dcc9c604bfa02d89f054ba2deb28eb6653930
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11.2` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.2` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2-alpine`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11.2-alpine` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-alpine3.20`

```console
$ docker pull julia@sha256:a0d1e60754e7968334173a0fd3fae454be24e2ad91eb57ee7c14aeccfc6f5a19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11.2-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:4aab52e8513e46d81ce40be84ae6e5cab39340b8bfea20dede7978edf1e5bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294447636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72689465fa12a8fba467e61fdba62ce815b991bf2bbfb17eccc03f72c8396e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f153b9b51f4a623f7c462332c4dc8a97778b1474f292e3b5026a6dc83a3c5e`  
		Last Modified: Tue, 07 Jan 2025 03:20:45 GMT  
		Size: 290.8 MB (290833273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c423ef0e6a199a26aeaebfc65cc5d903e38cdd48f25bafe8dd7061a937aa52b`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:25d841fae1bf7314c44f9a4520e46fc3fcd7144adc4fc76139580058c2ad905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0636e1e9a44e35a4d1c66372e6026d79a5d47b4e8137c916327a47ae735e89c8`

```dockerfile
```

-	Layers:
	-	`sha256:e3cceaf1730b482cc423d00f99d68f023e7e133c32ab4d64e25a4aa17e4a2d90`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fe7e08665f30c655e283c43a74233c43ae52f3ae5a7a22d760679775edd95d`  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-alpine3.21`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11.2-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-bookworm`

```console
$ docker pull julia@sha256:285a3bae293b2792a5913dbc9f65ea83dfdca15c1bcd0874aabcce6a37800cb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11.2-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bookworm` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-bullseye`

```console
$ docker pull julia@sha256:cd8f32ca639f35a85945561fd1295e05e21c9a905b3062324cc2c0da8439fe7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.2-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:5a97cdb7d45113e5113507875bc487d083c3635074a48880b552a64a5eecbfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18821a62c1d8618dc5df89692a96601d27bceccd77cdbff4d97969debd5dac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8881345e71d9bcc70bf3887b3d2332ddf2479459f8c5947061739acd90809f3`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.2 MB (2222681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b883d5f544de0d007a117979564a6dd5d99891dc767265dd4c580f6dc4802`  
		Last Modified: Tue, 24 Dec 2024 22:18:37 GMT  
		Size: 288.5 MB (288487930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548c5b42027516b21f101149d293ea00da9f37c545eb12991c5608f13823911`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5a6c8b42ec2931eb1e855f9bae5715f2fce5a49746859eec0af0158744931352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a04d02394fd49887693719ff1e147ca3703742ce8465d8dcc7d570af6eaeec`

```dockerfile
```

-	Layers:
	-	`sha256:dac735d67bc50567ef4bc58c46aaea627c9e12b539ca5c507a3b754e4b1c9620`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9b00da95435cf5ebac668793035b35d292f81944d530686cad44bda20444d4`  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d6c7077f28d26f09b3fdfa159bea7c9c2a5aa12c2e4534a3924500b4519f7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7bb7a4817f0e1f12b035b1524c4900a38d8e81de33d40b55239d6d4842112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b30040d42393764b30ee9fe0d7df28a5e4284ae841d1b33ad33c5b50d64937`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.2 MB (2210269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6895e19b215321cca937d71be96dd81493a7191bbc9a63a0b1ca2e3fa210deb`  
		Last Modified: Tue, 24 Dec 2024 22:57:13 GMT  
		Size: 303.7 MB (303658749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84195d59fc25b7d8e1ef832bafd320be00083bb82610bccfbb9ebdc675a0099f`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e99994c50ba3dfdbe3e87e78d6a3898fdcddda2def2ef3c45a5ca744b3991230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358464a318dcdc1a2534fc8496f82968f2b5946abad3603d3125c48cfcef08ab`

```dockerfile
```

-	Layers:
	-	`sha256:303b41587b13e532e459b7a32ec1264fb48b584e7bf56bb6dba6ad895478bd78`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682ecaf251bf124c14cb279f9c415d1fe6c4c561c06620d5ad01925bf2779a9c`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bullseye` - linux; 386

```console
$ docker pull julia@sha256:45a93e591281b1425ab4f38bc8ae3c6bf69f269b1085fdcaaf58f626ea9bbcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e75bdf641a5771324e59f7710367a8f433ad06516a860191ec651a2cc23876b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf450fc4bceff1e049c9ac3f4c6fb6f2c805c3cb9802cb678ede551f8271778`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.3 MB (2328070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e594f1817abc00a10b99af5a0911549589f2ebd18e7d714ac6836babea10dd7`  
		Last Modified: Tue, 24 Dec 2024 22:14:47 GMT  
		Size: 237.1 MB (237136266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03efcc14fabc0f7d32eecb671c9eefeb19af19b8e8f7d90394b4918069423714`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e4eb7480f72a41ee5b43acd058a12d398b98631b569cd611e23941105904e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3072085890e77d746e2fd968972f8bd7c6c8884aecfdfd494c9ce20bfda47b`

```dockerfile
```

-	Layers:
	-	`sha256:053737e018dedc63ec680f88496205b5fb15ecba4e08cd9b44430454b72e975f`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e622e1cb2156c68ad61d1d30382a279bea2babe409704a847fee4cbfc019cb0e`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11.2-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.2-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11.2-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.11.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.20`

```console
$ docker pull julia@sha256:a0d1e60754e7968334173a0fd3fae454be24e2ad91eb57ee7c14aeccfc6f5a19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:4aab52e8513e46d81ce40be84ae6e5cab39340b8bfea20dede7978edf1e5bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294447636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72689465fa12a8fba467e61fdba62ce815b991bf2bbfb17eccc03f72c8396e35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f153b9b51f4a623f7c462332c4dc8a97778b1474f292e3b5026a6dc83a3c5e`  
		Last Modified: Tue, 07 Jan 2025 03:20:45 GMT  
		Size: 290.8 MB (290833273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c423ef0e6a199a26aeaebfc65cc5d903e38cdd48f25bafe8dd7061a937aa52b`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:25d841fae1bf7314c44f9a4520e46fc3fcd7144adc4fc76139580058c2ad905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0636e1e9a44e35a4d1c66372e6026d79a5d47b4e8137c916327a47ae735e89c8`

```dockerfile
```

-	Layers:
	-	`sha256:e3cceaf1730b482cc423d00f99d68f023e7e133c32ab4d64e25a4aa17e4a2d90`  
		Last Modified: Tue, 07 Jan 2025 03:20:41 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29fe7e08665f30c655e283c43a74233c43ae52f3ae5a7a22d760679775edd95d`  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.21`

```console
$ docker pull julia@sha256:2507c7383723a2640374faca3591f23855d783b802a47ef2f58ef6d075c0eb52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:b417bc3321b3cf200ad88a843507a92feaa932d258e13897ebcbde5879ad1028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294471139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aede10c17a3e713881506dee5d6f8f3320bf026a988cfa65c96c36e88e0982d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea49443540670719feb5b3d7c84731772edf05c3e93d4964afc7998620b59e`  
		Last Modified: Tue, 07 Jan 2025 03:20:12 GMT  
		Size: 290.8 MB (290834551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47927b09580152f08c6622435dd06aed768d4c82187a3a995395aa2e2b3a2904`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:883b67a9da670bb9e091d5ebe606731e2b44b586460fcfc8ada5114cbd29b5a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd797ede3b284b34e696b6f3577afa7365d3a5256dd405b71f00d24ae1dd1b8`

```dockerfile
```

-	Layers:
	-	`sha256:982a4a256bcf596a2c2235aec615b649703d2209e147df58a9048810ae38803f`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdfce3f0aef8729b76cd6a85cd2a2395ea0bc8a28ba7a8c2a4c063a5fc87f20`  
		Last Modified: Tue, 07 Jan 2025 03:20:09 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bookworm`

```console
$ docker pull julia@sha256:285a3bae293b2792a5913dbc9f65ea83dfdca15c1bcd0874aabcce6a37800cb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:cd8f32ca639f35a85945561fd1295e05e21c9a905b3062324cc2c0da8439fe7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:5a97cdb7d45113e5113507875bc487d083c3635074a48880b552a64a5eecbfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18821a62c1d8618dc5df89692a96601d27bceccd77cdbff4d97969debd5dac2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8881345e71d9bcc70bf3887b3d2332ddf2479459f8c5947061739acd90809f3`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.2 MB (2222681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291b883d5f544de0d007a117979564a6dd5d99891dc767265dd4c580f6dc4802`  
		Last Modified: Tue, 24 Dec 2024 22:18:37 GMT  
		Size: 288.5 MB (288487930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548c5b42027516b21f101149d293ea00da9f37c545eb12991c5608f13823911`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5a6c8b42ec2931eb1e855f9bae5715f2fce5a49746859eec0af0158744931352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a04d02394fd49887693719ff1e147ca3703742ce8465d8dcc7d570af6eaeec`

```dockerfile
```

-	Layers:
	-	`sha256:dac735d67bc50567ef4bc58c46aaea627c9e12b539ca5c507a3b754e4b1c9620`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9b00da95435cf5ebac668793035b35d292f81944d530686cad44bda20444d4`  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d6c7077f28d26f09b3fdfa159bea7c9c2a5aa12c2e4534a3924500b4519f7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e7bb7a4817f0e1f12b035b1524c4900a38d8e81de33d40b55239d6d4842112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b30040d42393764b30ee9fe0d7df28a5e4284ae841d1b33ad33c5b50d64937`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.2 MB (2210269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6895e19b215321cca937d71be96dd81493a7191bbc9a63a0b1ca2e3fa210deb`  
		Last Modified: Tue, 24 Dec 2024 22:57:13 GMT  
		Size: 303.7 MB (303658749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84195d59fc25b7d8e1ef832bafd320be00083bb82610bccfbb9ebdc675a0099f`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e99994c50ba3dfdbe3e87e78d6a3898fdcddda2def2ef3c45a5ca744b3991230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358464a318dcdc1a2534fc8496f82968f2b5946abad3603d3125c48cfcef08ab`

```dockerfile
```

-	Layers:
	-	`sha256:303b41587b13e532e459b7a32ec1264fb48b584e7bf56bb6dba6ad895478bd78`  
		Last Modified: Tue, 24 Dec 2024 22:57:07 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682ecaf251bf124c14cb279f9c415d1fe6c4c561c06620d5ad01925bf2779a9c`  
		Last Modified: Tue, 24 Dec 2024 22:57:06 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:45a93e591281b1425ab4f38bc8ae3c6bf69f269b1085fdcaaf58f626ea9bbcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e75bdf641a5771324e59f7710367a8f433ad06516a860191ec651a2cc23876b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eabd0eca84f0fa21c2f70f76b8b8cf28e46ca9b60ad0046239cb7712afdf935c`  
		Last Modified: Tue, 24 Dec 2024 21:32:27 GMT  
		Size: 31.2 MB (31178945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf450fc4bceff1e049c9ac3f4c6fb6f2c805c3cb9802cb678ede551f8271778`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.3 MB (2328070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e594f1817abc00a10b99af5a0911549589f2ebd18e7d714ac6836babea10dd7`  
		Last Modified: Tue, 24 Dec 2024 22:14:47 GMT  
		Size: 237.1 MB (237136266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03efcc14fabc0f7d32eecb671c9eefeb19af19b8e8f7d90394b4918069423714`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e4eb7480f72a41ee5b43acd058a12d398b98631b569cd611e23941105904e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3072085890e77d746e2fd968972f8bd7c6c8884aecfdfd494c9ce20bfda47b`

```dockerfile
```

-	Layers:
	-	`sha256:053737e018dedc63ec680f88496205b5fb15ecba4e08cd9b44430454b72e975f`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e622e1cb2156c68ad61d1d30382a279bea2babe409704a847fee4cbfc019cb0e`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:170e8401b4265a188bd5f981ea5dcc9c604bfa02d89f054ba2deb28eb6653930
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
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:2027c60ee22eeff3423d45b8830e2e37487a070503af95be757262e7e14a30c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322238483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d741e414406ad138a10ef6af2114ed29280608c661f05d94339f5f3e87b33604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b87a4b9c258af484c2dcc7074196db2556acef83a6f39deada584cb16f96fd`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 5.5 MB (5518323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f21e51b90b734c73f2b8e73a719c07035bfedbcc1637ed42f00317f7c625e60`  
		Last Modified: Tue, 24 Dec 2024 22:17:44 GMT  
		Size: 288.5 MB (288488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a6e8752c752f2d84fc455348a04b29bf1bdde2a0f1708cd097720bf21b7ceb`  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:6f3e5bb7a371d1e75646ed50129027b76395c01a3597f1435d8fa3038d60472f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a337d942affcceef6512ef822563301d69f11e286cadd0a786a2425a595820cf`

```dockerfile
```

-	Layers:
	-	`sha256:8e7d56c19835e01f91f9c6285d6f34ba91d8aefa8335e82e7691fde728520aa8`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46439d0935f7e51c9ac83bf4ee0d659ad834ad92663411a77423cdcd46d3b698`  
		Last Modified: Tue, 24 Dec 2024 22:17:40 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3aac1e622749e9105629c4e1ae5e1c512789c3b1f741532ebc18333d09052689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337064452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4586d6d1ff92833e94cfc6f2141e62500f761a313737c9a57ce609597ab30a9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c6ddb057a519a4393647643373d6173640925526f5c37daf76977451dd5b9e`  
		Size: 5.3 MB (5346061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e09fd9bba891fa9cc69a3fa2dfc189fbfbfecf8f526571decc5e2c8545e09e`  
		Last Modified: Tue, 24 Dec 2024 22:55:49 GMT  
		Size: 303.7 MB (303659300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d16bd9d6ec3d4b3aa0f590774c22a4a8bd057597d19140128cfa84a132c404`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:e34bac63e99b8e2f78f29d9716419ffa43af16e33279edb4f2b564e5323650c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53dbf54143f12dd218bfb482c2b1655c56f3e52ff213dd9ccaf5cc18c760f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a69c0637668fddb6ad26422fcc0b8dd5fc063041e0f3fb9a1de73d6baec973c7`  
		Last Modified: Tue, 24 Dec 2024 22:55:42 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df92be54dcf98d416fcfc1e2354f1ae384bff280b7e53dc494829b7947fc6cc6`  
		Last Modified: Tue, 24 Dec 2024 22:55:41 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:115e518e5b7bb2dc1d494af8e927cb1befff8825e3107c3cf84f300aba52a21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272022273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445f5ddfa82b6160f09cd90b7b582c0ea626717300f05e52c33479d3711b1488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f2944e892354af7ec7f4a3e728c1ff26827a51dc13f927a9ba00d01840d903`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 5.7 MB (5679205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44cf4d55f8a48cbc26777477694253e7ba49cd4730b617459ad50041c60f41`  
		Last Modified: Tue, 24 Dec 2024 22:14:44 GMT  
		Size: 237.1 MB (237137311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f72f77c4d75ac657d92bda8f55c287c3824f87707ad5a9361d117656d1e71`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:fb333d159297d2de92634d812e6c2d82bd27132f6a68eb3903898d4c7d54a8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925fdeaec37509ddc15c849c029c2bb7d0be89802c974e238b966a3f38e4d86`

```dockerfile
```

-	Layers:
	-	`sha256:cb023797be6ece6246662784d1ca73f86d6bf72efe9e82cc7a7feb32908d472d`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed986b2490f80195b4d259334a066a9868c7635d27f9a5904bf524e601c1bcc0`  
		Last Modified: Tue, 24 Dec 2024 22:14:39 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:94bd24d8fa28e55d0acb5f02c8900e00f797513074a6259f23fa4a4df38c172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286048269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c89132c80b31d6bf423bdba7c33af82b377f01d8a70ba77a06fb89152236362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305732d8370d1081d125889e36faef44a888002ac19cd93800718c3b1aa4f1c`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 6.1 MB (6056364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae0131b3fd9576eca9306defccc248bab1f18f185920fccfa11e7926628e43`  
		Last Modified: Wed, 25 Dec 2024 04:12:06 GMT  
		Size: 247.9 MB (247928294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6210be4497c447f254b423fd23ba395710a36673d6eb8ff97b6e1617f0b3f`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:1040dc24c0d36dc93098b4e9f6e2e9fa8b853002f92c3d35483b015acaed960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84161a19f39097a4900d9f1d98b0f759206558056fd8fb82ae331d9b13344963`

```dockerfile
```

-	Layers:
	-	`sha256:ef23ed108ae81e8421ddc45b36ed63b398220e2b4127f8189ff88ddde2b87404`  
		Last Modified: Wed, 25 Dec 2024 04:12:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28a5ce7819a4198c4dc67b42409f821b0045a3885fa0cdca3d2e7959a756c1`  
		Last Modified: Wed, 25 Dec 2024 04:11:59 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Wed, 11 Dec 2024 20:37:52 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Wed, 11 Dec 2024 20:38:26 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Wed, 11 Dec 2024 20:37:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
