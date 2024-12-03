<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
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
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11.1`](#julia1111)
-	[`julia:1.11.1-bookworm`](#julia1111-bookworm)
-	[`julia:1.11.1-bullseye`](#julia1111-bullseye)
-	[`julia:1.11.1-windowsservercore`](#julia1111-windowsservercore)
-	[`julia:1.11.1-windowsservercore-1809`](#julia1111-windowsservercore-1809)
-	[`julia:1.11.1-windowsservercore-ltsc2022`](#julia1111-windowsservercore-ltsc2022)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:b3aca3cb8b8d22c8d260cc0144d1c08f6479bf0247bff7675a9b36cf133aa91e
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
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:f8032b445fbfe3a0e5af146feaff626877dc7b883294eec49a3f229a03fc4381
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
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:9ad976e364edc34edd72583734a234e66013f7c895fc1bc9c8248b59592ecd29
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
$ docker pull julia@sha256:e21ad0137c8b8a15b07d3f6195f181369084e6886674d03d719466e1b8e693b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289573975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283efac7b94defa0b6bf2d95465edbfa72c96aa45afe84530634df90f493a72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf17a4a247bda6618c4fd4a5e2f697d84b4575bbcbf5eed6aec8b9683260fa`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f3196fc55c0e1e266503f136dee778f9b3fb1a1b7543173ba25f340eed634`  
		Last Modified: Tue, 03 Dec 2024 02:17:44 GMT  
		Size: 257.1 MB (257098268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11c3c7d35a020e8396741424315667aa7faa7a2ca25960cc125143b9abe43d1`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:71390e2a136bad7f3e40597957def443cd71973d3311409ab6d4a6549dfaa6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c1127c7065175fb5bca231291874782eb785033aa605ae403ef16fa16d3586`

```dockerfile
```

-	Layers:
	-	`sha256:1d374a3dba343ba78f019fa976918d8e81b3b75e469edfb85cc0aaf1875c1128`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.7 MB (2715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8dd6d13c2a59f9838ab75ab90af9396914516dedbb45330ee63f7c2d7b8442`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f798c57648a0e9839faed7b80605afe746f10e91233bd9c8d56323833473f113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284962256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8bac96e1f5e359fb62d7ea7ea96350af77e69578b892ddc739b837d4fd7dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ecb8ff42f5d159e95271acfe6754860a7e5caa81f142e067200dd251f84166`  
		Last Modified: Tue, 03 Dec 2024 02:51:29 GMT  
		Size: 254.0 MB (254006669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603847c85db951da72dc623ab26bfa0d8b611f3c6000045ee8aec29142e4084e`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2ae870ab0aa4cd721b585fd780c47adba288682908c90fd92712ea9066906d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a711dd34c6db70375fac74699c4537d82afccb7009df2ecd59365e9c0fc3a9a6`

```dockerfile
```

-	Layers:
	-	`sha256:422a95300688a576bcbcbffd8a35fc6ddaeda8dd68da465003ee23070526ca61`  
		Last Modified: Tue, 03 Dec 2024 02:51:24 GMT  
		Size: 2.7 MB (2715422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1a191ece5d050addd22e2bcd4b95df69c526f26db24f10570c867801c775e0`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:b8c5e00251f9072e18e6056341881292bda3ac7500641b86ea9b162f8ce1db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57d4abd1e50829e2dc8e48cdba72d41ceb67b43b3741bfdc515f360389b2dea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac99d6f64ac9099c145ee3db62bcfb8030850642fcdaa4429e523d6dc8fd80`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.3 MB (2328053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d157d5a761800b63ba98bdc82e9dcf56f24fc61b6df22284c10440f8a9e80`  
		Last Modified: Tue, 03 Dec 2024 02:15:06 GMT  
		Size: 234.7 MB (234658568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7d4ace25cdb8d2c5af7784bbf5625e038a9aa4e5b4ca90923f419010e1865`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:91263673457c8bc3c6a544d8083a5a7c3cd1c0dd296375da915012199187e637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecac8533b702416bddd428020d4c57838b9e633eff9c177f36aeddfa3e0d6c5`

```dockerfile
```

-	Layers:
	-	`sha256:2475be50377543347fcc684091713d6f8f1dd527b1e6eb8e5583d6e2c1928b81`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.7 MB (2712258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8835e1f2292911817cb16e50f7a082b1766f67c8fca1808216394d3b54ff92da`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:b34203110520d462f78b9b325fa3286f72d98752663c82f296ebb1f05977029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:01bef96047f40618e8bccb38b594dcb343f5bae3fbe5187006d2f10f87744502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2a0dd1446d94fdbffd2075628d86db8741612040d64d4a94e23b42b57ab2f462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:8b8b31dfec4fd59cb37744ba2a9dcf127d71b1610af615d434eaad8f99a3fd41
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
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:fd662a947fa78060c0650b7a009eab5e49555ee6d826e282c52867c7b3c13788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1768a63d5416136eb731a03019100bea1b20b45eccaad2f07aecfffe1b59b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790894c7ce293337316f6f3a7c428ca2143951146e7ac3e6bfd85997cf7aa31`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 5.5 MB (5518386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21b4d26c2e5b06840758981d1a93e46b327bb58e7dda074a13d2a7305de901`  
		Last Modified: Tue, 03 Dec 2024 02:17:39 GMT  
		Size: 175.9 MB (175894824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a53ab9eaa489e45f11102bcc5e1385a7eaebafc9424f407c43b796120e5e828`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:c76250c1f81e990134e59d071981e542b26d652de2800396531828075535f60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ed07e1dd17117b209104bbc702e3bce4ec1769ba1088d7c7cb7b3f9cde83e`

```dockerfile
```

-	Layers:
	-	`sha256:4abfa1d4d3043dc73e55077ef43cb29ba7b1d1d5fdae9c625cee880223b49be6`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 2.4 MB (2447964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89755339f6aa3f9a248de2056d6c1e76e516b699f842da5ca6851e2dddf8534`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4197af0f2b930cb4f50315ceded7d34bd4b06ff5d78af6320cf8d27c963012c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88695edab0293b2e3dd6cdef45aaef8def8b8aa34bf0fff04d5a302a5c3e229`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d9d540b1d6f7a7aafc486f8b4c6bbc7fff11341ee917d9b18b7ac5fc89e823`  
		Last Modified: Tue, 03 Dec 2024 02:52:27 GMT  
		Size: 177.7 MB (177651904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52b1db90986551f9db5857b707165b6340ba2062b2168d9d3e80893beccc44`  
		Last Modified: Tue, 03 Dec 2024 02:52:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:eba2a7eb6319e4bd14dc22ef6644bed9b05dace9b933201b79176c233d130cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e792085a9084d7f845b6d9f33090a1e309f2f1755406410b2f3c07bae3ebb0`

```dockerfile
```

-	Layers:
	-	`sha256:f8db31c135756253792fe486578d6a749ffa77708f72dafdbb1ccaaf0153c47b`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 2.4 MB (2447016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cedf662b1c4d20362315198477517404af44184163db6eafe440edbfa434a99`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:820ad4d23728521a82841b2cf63c4c7cd6e7f3bde54bfc6760c8db09b235cdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e15e4f927bd54ab31a6f42a69a6366c4e1837eabba4a3f001cc47ad84e7271f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc72b80b653978b6782bf494e51729ed99d337e4b8ec2ee5e0d6d525eb9051`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 5.7 MB (5679154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf2693ee77f996b5ddce9f592a33d06fd5bff9916a3d32fffe38fc60b683b5`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 157.8 MB (157784869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868b4e5b8ff97c1490af9439a98eebf5bb5909d5192d5b0afa848af37966a1d1`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:891500a192a6129cdb617516e9b66fedbb858901d8851a931cc01620800d3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05ca23656c741272fcba266db9fd174c8838dcd359666ef537732e0df68d042`

```dockerfile
```

-	Layers:
	-	`sha256:ba949ffebd0805d506e2244e0c6474befcd6fa7d15c72a74b9961c02666dfa36`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 2.4 MB (2445056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f604a9f7020b898316574dde640cd26a6658d2153ebc7c0919e8b12f9a875b`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:30112123ce291e6d21205323c5f4ed69380d3c731b307afb38561db306e198a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf14335e4c3622ad827c74025e9143a232c789e78661ca2af2bbed3f453d27bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d1148f8fffb7847e45ac4930cd58d42bc12795484cce61b255b13c0101744d`  
		Last Modified: Tue, 03 Dec 2024 02:38:48 GMT  
		Size: 155.5 MB (155493317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996d347c0409e68f13a4f5b718c28a63aedcc0a85e561b9163c8af5a1383d40b`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:431a04b9e4dae61fa620fa2987f0ad882d48c99d09403124ed84a1a386436e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c5c352e33d40810b621b047241f02f7d3e2c5c118a8622a06a7ffc97d4cbcf`

```dockerfile
```

-	Layers:
	-	`sha256:de998a6eea7f1c9f08dd6c8869207b0d2b8c717c9536295faa3beb605956f70c`  
		Last Modified: Tue, 03 Dec 2024 02:38:44 GMT  
		Size: 2.5 MB (2451149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c904a42c879a49aaf8180233934f5332655e371a640e5e4d2fced5fed542b237`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:f7b4ede3f5c2408c7c8534ec776ce9bc36d5bcb0a887543fb9017369728acf0b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441583248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71b7014f17ba69e4a32950bdcbaa9d1f502c06ea47238ce7d47f95377a8cb1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 27 Nov 2024 18:23:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:09 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:24:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:24:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa6aa624f3bfd9ddbb2bfa80e6906c4f9407490a2bb7a1c8eec783221936c8`  
		Last Modified: Wed, 27 Nov 2024 18:24:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0aedfd409a9653247572a7614e80df4f8f1140b3d03c06e2d9fdcc793976b5`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd3a3e2f4588b48b57565995636ea71d461d49b186a056c0d9ce206c35b7834`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6914c1e7bd201a0c735819a46795e058b54b2d6ace74f8aee1d6aa257cb1d`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9914aa6cc20f1ce5afa64235fff7aa7e1a3483d84fc00fa49b3692db59fb0b`  
		Last Modified: Wed, 27 Nov 2024 18:25:11 GMT  
		Size: 189.1 MB (189092535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6826d228b0b39cba020f951d56ef9a45dffeeb1a81045313b4f39665b08aa9`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:2523b646ff1bbf02eadb2268d9b4fe0edfefe60d9da0d56fa184305bfe27d471
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199873526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1356e5c8e2b74a52a101c26c287939349c27a5af5f0b31a1080c2b58fb302a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 27 Nov 2024 18:23:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:06 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:25:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:25:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229fa5e9f995bc80cefd5d49c4bce39025cff42c23bac06ecccd794d3f57cd3`  
		Last Modified: Wed, 27 Nov 2024 18:25:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af840676c667902bf03b5f217acae860de62e50d74b46974db17964b306ba005`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1fbf2c4207a2b3a7151f3c87fadf010211963c8a7023a2b751c3ed49f982e`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa5fff7ec0d49051cc0c1319dd5976a72b9fe232fc5f932950a3a63ef293732`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfd53f8cac131a4112a31780174b170cb25bcfadfec5211d720d0ededb111b4`  
		Last Modified: Wed, 27 Nov 2024 18:25:42 GMT  
		Size: 189.2 MB (189213272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89e389b7bba7125a7cc1a4756dd955387fcacf64e61c88c7a015730160dabc`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:4498ed4f1e0afc1b9c821fa075fafa093773729e350120ef6193bd7839dccb46
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
$ docker pull julia@sha256:fd662a947fa78060c0650b7a009eab5e49555ee6d826e282c52867c7b3c13788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1768a63d5416136eb731a03019100bea1b20b45eccaad2f07aecfffe1b59b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790894c7ce293337316f6f3a7c428ca2143951146e7ac3e6bfd85997cf7aa31`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 5.5 MB (5518386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21b4d26c2e5b06840758981d1a93e46b327bb58e7dda074a13d2a7305de901`  
		Last Modified: Tue, 03 Dec 2024 02:17:39 GMT  
		Size: 175.9 MB (175894824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a53ab9eaa489e45f11102bcc5e1385a7eaebafc9424f407c43b796120e5e828`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c76250c1f81e990134e59d071981e542b26d652de2800396531828075535f60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ed07e1dd17117b209104bbc702e3bce4ec1769ba1088d7c7cb7b3f9cde83e`

```dockerfile
```

-	Layers:
	-	`sha256:4abfa1d4d3043dc73e55077ef43cb29ba7b1d1d5fdae9c625cee880223b49be6`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 2.4 MB (2447964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89755339f6aa3f9a248de2056d6c1e76e516b699f842da5ca6851e2dddf8534`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4197af0f2b930cb4f50315ceded7d34bd4b06ff5d78af6320cf8d27c963012c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88695edab0293b2e3dd6cdef45aaef8def8b8aa34bf0fff04d5a302a5c3e229`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d9d540b1d6f7a7aafc486f8b4c6bbc7fff11341ee917d9b18b7ac5fc89e823`  
		Last Modified: Tue, 03 Dec 2024 02:52:27 GMT  
		Size: 177.7 MB (177651904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52b1db90986551f9db5857b707165b6340ba2062b2168d9d3e80893beccc44`  
		Last Modified: Tue, 03 Dec 2024 02:52:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:eba2a7eb6319e4bd14dc22ef6644bed9b05dace9b933201b79176c233d130cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e792085a9084d7f845b6d9f33090a1e309f2f1755406410b2f3c07bae3ebb0`

```dockerfile
```

-	Layers:
	-	`sha256:f8db31c135756253792fe486578d6a749ffa77708f72dafdbb1ccaaf0153c47b`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 2.4 MB (2447016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cedf662b1c4d20362315198477517404af44184163db6eafe440edbfa434a99`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:820ad4d23728521a82841b2cf63c4c7cd6e7f3bde54bfc6760c8db09b235cdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e15e4f927bd54ab31a6f42a69a6366c4e1837eabba4a3f001cc47ad84e7271f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc72b80b653978b6782bf494e51729ed99d337e4b8ec2ee5e0d6d525eb9051`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 5.7 MB (5679154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf2693ee77f996b5ddce9f592a33d06fd5bff9916a3d32fffe38fc60b683b5`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 157.8 MB (157784869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868b4e5b8ff97c1490af9439a98eebf5bb5909d5192d5b0afa848af37966a1d1`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:891500a192a6129cdb617516e9b66fedbb858901d8851a931cc01620800d3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05ca23656c741272fcba266db9fd174c8838dcd359666ef537732e0df68d042`

```dockerfile
```

-	Layers:
	-	`sha256:ba949ffebd0805d506e2244e0c6474befcd6fa7d15c72a74b9961c02666dfa36`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 2.4 MB (2445056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f604a9f7020b898316574dde640cd26a6658d2153ebc7c0919e8b12f9a875b`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:30112123ce291e6d21205323c5f4ed69380d3c731b307afb38561db306e198a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf14335e4c3622ad827c74025e9143a232c789e78661ca2af2bbed3f453d27bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d1148f8fffb7847e45ac4930cd58d42bc12795484cce61b255b13c0101744d`  
		Last Modified: Tue, 03 Dec 2024 02:38:48 GMT  
		Size: 155.5 MB (155493317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996d347c0409e68f13a4f5b718c28a63aedcc0a85e561b9163c8af5a1383d40b`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:431a04b9e4dae61fa620fa2987f0ad882d48c99d09403124ed84a1a386436e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c5c352e33d40810b621b047241f02f7d3e2c5c118a8622a06a7ffc97d4cbcf`

```dockerfile
```

-	Layers:
	-	`sha256:de998a6eea7f1c9f08dd6c8869207b0d2b8c717c9536295faa3beb605956f70c`  
		Last Modified: Tue, 03 Dec 2024 02:38:44 GMT  
		Size: 2.5 MB (2451149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c904a42c879a49aaf8180233934f5332655e371a640e5e4d2fced5fed542b237`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:fdba313cb6ee5b3d997b4ddfe55bd4dd0bb30d21d6cdd349eef1356a495a4c0e
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
$ docker pull julia@sha256:a4fbe2cad2992c27b3fdb8d90855c08f070511bb9172692ab4ed51e22fc617a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf895713fcc9a37a82015cd30894eec904235dca77d59a87e1d6cc21c93d5018`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e494ac0fd0b4e883b6e84ecfeb34ec110a9703aa6fa0b2468151782e1cf6b7db`  
		Last Modified: Tue, 03 Dec 2024 03:27:21 GMT  
		Size: 2.2 MB (2222664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43995af421ba68e5cd3ad6338e70e7008a92457b3aea6551a449d5694ba9dd70`  
		Last Modified: Tue, 03 Dec 2024 03:27:25 GMT  
		Size: 175.9 MB (175895537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805ba392b197ea6ec4d51520acf682e4d0d9945182c2e3686648d9c06afbec1`  
		Last Modified: Tue, 03 Dec 2024 03:27:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5ab84d849f0db958c8e195b8e06ce50c6bd059c602b957d4459960ff234c4472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179fc31fd44a24ba31f25256029a7664d6bee1bbce8cac497aa603cfa70801af`

```dockerfile
```

-	Layers:
	-	`sha256:00a005e5a9a81b7f85ea2141981c56c974ae58de7a62a74a9834322411980dd0`  
		Last Modified: Tue, 03 Dec 2024 03:27:21 GMT  
		Size: 2.7 MB (2715778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ac29469c9bb625267d90a13f820881722766f628dc5f57b45840b3249bb410`  
		Last Modified: Tue, 03 Dec 2024 03:27:20 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4150795cf077fcd522ff1d05ea171dc4273f66a4f95d5df78c06afbbdf0cfcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d1979226dfc42bfad4a752600117d4cee9c5ff26a8e98c3276b7a667aba56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d5055a1eeee0d8c4e020579309e11571a87409737b4f8ab2f5e39ed2588ae6`  
		Last Modified: Tue, 03 Dec 2024 02:53:21 GMT  
		Size: 177.7 MB (177651869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd9754aeac347190f4e53fbc0c7e3223d7204e7f2e95965102c32523d4d300`  
		Last Modified: Tue, 03 Dec 2024 02:53:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4bce91d98cd9185ccbfdb2886407374c978aec241bd70b12b8bf96a81b076f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b313814c5443bd96a13d5821c207b33736559ca2b96185cfdb8c3982cfcec83`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e3ee8289ccbe4361c75c054536cbc5b67ce2d8632c2bd6da319e85328cbe5`  
		Last Modified: Tue, 03 Dec 2024 02:53:18 GMT  
		Size: 2.7 MB (2714794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d087e594d94e8666744b2269657b4ea46a84e1c203dd9761f9885b804305c3c9`  
		Last Modified: Tue, 03 Dec 2024 02:53:17 GMT  
		Size: 16.7 KB (16719 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:fdb6080560a8a147629a9cd9c79b96896b6135c42cdc21f716a156756c1a8070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ce640537bccea32e674f3a7553aef9d385a55ef052f8731782d2479e332c63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84a64daeb38ef810055a734dfb9badf83fb560c812fead338da22c961649f8b`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 2.3 MB (2328071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dba70bb5085d5400c49175761f7e129c1cdf188f01e42df277dba7c2621299c`  
		Last Modified: Tue, 03 Dec 2024 02:16:17 GMT  
		Size: 157.8 MB (157784861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cce4946cb41578a643e906c38307dbdc4ba800d23419ae86829f7ca0aef820`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cb2cb6ff8e7dc3a7eea0ed455e4b99a15c6aaaa894713f0b5ac1f80fab633c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414a2fb3b2020de32e6f0ecb10190c5c106287b6e5fcfd7bbec871b182746000`

```dockerfile
```

-	Layers:
	-	`sha256:cf3c6f258231b32e3cd1faf6476412948a607e9a5e0be33bf6b7cf2f6fe8a971`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 2.7 MB (2712886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928bbabcbaf74430af1d0d157bb8904de585cf76421b1720a41cd7bdbf798021`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:10b1dac30692ba42e1f28b104a13fa6197e288bf82ddae8279d05b5b31879f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:f7b4ede3f5c2408c7c8534ec776ce9bc36d5bcb0a887543fb9017369728acf0b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441583248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71b7014f17ba69e4a32950bdcbaa9d1f502c06ea47238ce7d47f95377a8cb1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 27 Nov 2024 18:23:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:09 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:24:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:24:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa6aa624f3bfd9ddbb2bfa80e6906c4f9407490a2bb7a1c8eec783221936c8`  
		Last Modified: Wed, 27 Nov 2024 18:24:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0aedfd409a9653247572a7614e80df4f8f1140b3d03c06e2d9fdcc793976b5`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd3a3e2f4588b48b57565995636ea71d461d49b186a056c0d9ce206c35b7834`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6914c1e7bd201a0c735819a46795e058b54b2d6ace74f8aee1d6aa257cb1d`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9914aa6cc20f1ce5afa64235fff7aa7e1a3483d84fc00fa49b3692db59fb0b`  
		Last Modified: Wed, 27 Nov 2024 18:25:11 GMT  
		Size: 189.1 MB (189092535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6826d228b0b39cba020f951d56ef9a45dffeeb1a81045313b4f39665b08aa9`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:2523b646ff1bbf02eadb2268d9b4fe0edfefe60d9da0d56fa184305bfe27d471
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199873526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1356e5c8e2b74a52a101c26c287939349c27a5af5f0b31a1080c2b58fb302a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 27 Nov 2024 18:23:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:06 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:25:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:25:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229fa5e9f995bc80cefd5d49c4bce39025cff42c23bac06ecccd794d3f57cd3`  
		Last Modified: Wed, 27 Nov 2024 18:25:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af840676c667902bf03b5f217acae860de62e50d74b46974db17964b306ba005`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1fbf2c4207a2b3a7151f3c87fadf010211963c8a7023a2b751c3ed49f982e`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa5fff7ec0d49051cc0c1319dd5976a72b9fe232fc5f932950a3a63ef293732`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfd53f8cac131a4112a31780174b170cb25bcfadfec5211d720d0ededb111b4`  
		Last Modified: Wed, 27 Nov 2024 18:25:42 GMT  
		Size: 189.2 MB (189213272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89e389b7bba7125a7cc1a4756dd955387fcacf64e61c88c7a015730160dabc`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:33c7c7c37047a0544e3c0d7502c1dd9e209bd884b9a9227dc3b3e52c0bba83f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:2523b646ff1bbf02eadb2268d9b4fe0edfefe60d9da0d56fa184305bfe27d471
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199873526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1356e5c8e2b74a52a101c26c287939349c27a5af5f0b31a1080c2b58fb302a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 27 Nov 2024 18:23:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:06 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:25:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:25:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229fa5e9f995bc80cefd5d49c4bce39025cff42c23bac06ecccd794d3f57cd3`  
		Last Modified: Wed, 27 Nov 2024 18:25:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af840676c667902bf03b5f217acae860de62e50d74b46974db17964b306ba005`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1fbf2c4207a2b3a7151f3c87fadf010211963c8a7023a2b751c3ed49f982e`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa5fff7ec0d49051cc0c1319dd5976a72b9fe232fc5f932950a3a63ef293732`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfd53f8cac131a4112a31780174b170cb25bcfadfec5211d720d0ededb111b4`  
		Last Modified: Wed, 27 Nov 2024 18:25:42 GMT  
		Size: 189.2 MB (189213272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89e389b7bba7125a7cc1a4756dd955387fcacf64e61c88c7a015730160dabc`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:f7a5ebe44595b1ddd706575a1c3e42c36b508c2b40befe61b064d92838455d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:f7b4ede3f5c2408c7c8534ec776ce9bc36d5bcb0a887543fb9017369728acf0b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441583248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71b7014f17ba69e4a32950bdcbaa9d1f502c06ea47238ce7d47f95377a8cb1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 27 Nov 2024 18:23:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:09 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:24:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:24:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa6aa624f3bfd9ddbb2bfa80e6906c4f9407490a2bb7a1c8eec783221936c8`  
		Last Modified: Wed, 27 Nov 2024 18:24:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0aedfd409a9653247572a7614e80df4f8f1140b3d03c06e2d9fdcc793976b5`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd3a3e2f4588b48b57565995636ea71d461d49b186a056c0d9ce206c35b7834`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6914c1e7bd201a0c735819a46795e058b54b2d6ace74f8aee1d6aa257cb1d`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9914aa6cc20f1ce5afa64235fff7aa7e1a3483d84fc00fa49b3692db59fb0b`  
		Last Modified: Wed, 27 Nov 2024 18:25:11 GMT  
		Size: 189.1 MB (189092535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6826d228b0b39cba020f951d56ef9a45dffeeb1a81045313b4f39665b08aa9`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7`

```console
$ docker pull julia@sha256:8b8b31dfec4fd59cb37744ba2a9dcf127d71b1610af615d434eaad8f99a3fd41
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
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.10.7` - linux; amd64

```console
$ docker pull julia@sha256:fd662a947fa78060c0650b7a009eab5e49555ee6d826e282c52867c7b3c13788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1768a63d5416136eb731a03019100bea1b20b45eccaad2f07aecfffe1b59b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790894c7ce293337316f6f3a7c428ca2143951146e7ac3e6bfd85997cf7aa31`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 5.5 MB (5518386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21b4d26c2e5b06840758981d1a93e46b327bb58e7dda074a13d2a7305de901`  
		Last Modified: Tue, 03 Dec 2024 02:17:39 GMT  
		Size: 175.9 MB (175894824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a53ab9eaa489e45f11102bcc5e1385a7eaebafc9424f407c43b796120e5e828`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:c76250c1f81e990134e59d071981e542b26d652de2800396531828075535f60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ed07e1dd17117b209104bbc702e3bce4ec1769ba1088d7c7cb7b3f9cde83e`

```dockerfile
```

-	Layers:
	-	`sha256:4abfa1d4d3043dc73e55077ef43cb29ba7b1d1d5fdae9c625cee880223b49be6`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 2.4 MB (2447964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89755339f6aa3f9a248de2056d6c1e76e516b699f842da5ca6851e2dddf8534`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4197af0f2b930cb4f50315ceded7d34bd4b06ff5d78af6320cf8d27c963012c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88695edab0293b2e3dd6cdef45aaef8def8b8aa34bf0fff04d5a302a5c3e229`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d9d540b1d6f7a7aafc486f8b4c6bbc7fff11341ee917d9b18b7ac5fc89e823`  
		Last Modified: Tue, 03 Dec 2024 02:52:27 GMT  
		Size: 177.7 MB (177651904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52b1db90986551f9db5857b707165b6340ba2062b2168d9d3e80893beccc44`  
		Last Modified: Tue, 03 Dec 2024 02:52:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:eba2a7eb6319e4bd14dc22ef6644bed9b05dace9b933201b79176c233d130cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e792085a9084d7f845b6d9f33090a1e309f2f1755406410b2f3c07bae3ebb0`

```dockerfile
```

-	Layers:
	-	`sha256:f8db31c135756253792fe486578d6a749ffa77708f72dafdbb1ccaaf0153c47b`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 2.4 MB (2447016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cedf662b1c4d20362315198477517404af44184163db6eafe440edbfa434a99`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; 386

```console
$ docker pull julia@sha256:820ad4d23728521a82841b2cf63c4c7cd6e7f3bde54bfc6760c8db09b235cdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e15e4f927bd54ab31a6f42a69a6366c4e1837eabba4a3f001cc47ad84e7271f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc72b80b653978b6782bf494e51729ed99d337e4b8ec2ee5e0d6d525eb9051`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 5.7 MB (5679154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf2693ee77f996b5ddce9f592a33d06fd5bff9916a3d32fffe38fc60b683b5`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 157.8 MB (157784869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868b4e5b8ff97c1490af9439a98eebf5bb5909d5192d5b0afa848af37966a1d1`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:891500a192a6129cdb617516e9b66fedbb858901d8851a931cc01620800d3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05ca23656c741272fcba266db9fd174c8838dcd359666ef537732e0df68d042`

```dockerfile
```

-	Layers:
	-	`sha256:ba949ffebd0805d506e2244e0c6474befcd6fa7d15c72a74b9961c02666dfa36`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 2.4 MB (2445056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f604a9f7020b898316574dde640cd26a6658d2153ebc7c0919e8b12f9a875b`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; ppc64le

```console
$ docker pull julia@sha256:30112123ce291e6d21205323c5f4ed69380d3c731b307afb38561db306e198a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf14335e4c3622ad827c74025e9143a232c789e78661ca2af2bbed3f453d27bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d1148f8fffb7847e45ac4930cd58d42bc12795484cce61b255b13c0101744d`  
		Last Modified: Tue, 03 Dec 2024 02:38:48 GMT  
		Size: 155.5 MB (155493317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996d347c0409e68f13a4f5b718c28a63aedcc0a85e561b9163c8af5a1383d40b`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:431a04b9e4dae61fa620fa2987f0ad882d48c99d09403124ed84a1a386436e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c5c352e33d40810b621b047241f02f7d3e2c5c118a8622a06a7ffc97d4cbcf`

```dockerfile
```

-	Layers:
	-	`sha256:de998a6eea7f1c9f08dd6c8869207b0d2b8c717c9536295faa3beb605956f70c`  
		Last Modified: Tue, 03 Dec 2024 02:38:44 GMT  
		Size: 2.5 MB (2451149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c904a42c879a49aaf8180233934f5332655e371a640e5e4d2fced5fed542b237`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:f7b4ede3f5c2408c7c8534ec776ce9bc36d5bcb0a887543fb9017369728acf0b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441583248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71b7014f17ba69e4a32950bdcbaa9d1f502c06ea47238ce7d47f95377a8cb1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 27 Nov 2024 18:23:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:09 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:24:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:24:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa6aa624f3bfd9ddbb2bfa80e6906c4f9407490a2bb7a1c8eec783221936c8`  
		Last Modified: Wed, 27 Nov 2024 18:24:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0aedfd409a9653247572a7614e80df4f8f1140b3d03c06e2d9fdcc793976b5`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd3a3e2f4588b48b57565995636ea71d461d49b186a056c0d9ce206c35b7834`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6914c1e7bd201a0c735819a46795e058b54b2d6ace74f8aee1d6aa257cb1d`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9914aa6cc20f1ce5afa64235fff7aa7e1a3483d84fc00fa49b3692db59fb0b`  
		Last Modified: Wed, 27 Nov 2024 18:25:11 GMT  
		Size: 189.1 MB (189092535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6826d228b0b39cba020f951d56ef9a45dffeeb1a81045313b4f39665b08aa9`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:2523b646ff1bbf02eadb2268d9b4fe0edfefe60d9da0d56fa184305bfe27d471
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199873526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1356e5c8e2b74a52a101c26c287939349c27a5af5f0b31a1080c2b58fb302a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 27 Nov 2024 18:23:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:06 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:25:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:25:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229fa5e9f995bc80cefd5d49c4bce39025cff42c23bac06ecccd794d3f57cd3`  
		Last Modified: Wed, 27 Nov 2024 18:25:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af840676c667902bf03b5f217acae860de62e50d74b46974db17964b306ba005`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1fbf2c4207a2b3a7151f3c87fadf010211963c8a7023a2b751c3ed49f982e`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa5fff7ec0d49051cc0c1319dd5976a72b9fe232fc5f932950a3a63ef293732`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfd53f8cac131a4112a31780174b170cb25bcfadfec5211d720d0ededb111b4`  
		Last Modified: Wed, 27 Nov 2024 18:25:42 GMT  
		Size: 189.2 MB (189213272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89e389b7bba7125a7cc1a4756dd955387fcacf64e61c88c7a015730160dabc`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-bookworm`

```console
$ docker pull julia@sha256:4498ed4f1e0afc1b9c821fa075fafa093773729e350120ef6193bd7839dccb46
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
$ docker pull julia@sha256:fd662a947fa78060c0650b7a009eab5e49555ee6d826e282c52867c7b3c13788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209645161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1768a63d5416136eb731a03019100bea1b20b45eccaad2f07aecfffe1b59b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790894c7ce293337316f6f3a7c428ca2143951146e7ac3e6bfd85997cf7aa31`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 5.5 MB (5518386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc21b4d26c2e5b06840758981d1a93e46b327bb58e7dda074a13d2a7305de901`  
		Last Modified: Tue, 03 Dec 2024 02:17:39 GMT  
		Size: 175.9 MB (175894824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a53ab9eaa489e45f11102bcc5e1385a7eaebafc9424f407c43b796120e5e828`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c76250c1f81e990134e59d071981e542b26d652de2800396531828075535f60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ed07e1dd17117b209104bbc702e3bce4ec1769ba1088d7c7cb7b3f9cde83e`

```dockerfile
```

-	Layers:
	-	`sha256:4abfa1d4d3043dc73e55077ef43cb29ba7b1d1d5fdae9c625cee880223b49be6`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 2.4 MB (2447964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89755339f6aa3f9a248de2056d6c1e76e516b699f842da5ca6851e2dddf8534`  
		Last Modified: Tue, 03 Dec 2024 02:17:36 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4197af0f2b930cb4f50315ceded7d34bd4b06ff5d78af6320cf8d27c963012c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211057161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88695edab0293b2e3dd6cdef45aaef8def8b8aa34bf0fff04d5a302a5c3e229`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d9d540b1d6f7a7aafc486f8b4c6bbc7fff11341ee917d9b18b7ac5fc89e823`  
		Last Modified: Tue, 03 Dec 2024 02:52:27 GMT  
		Size: 177.7 MB (177651904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52b1db90986551f9db5857b707165b6340ba2062b2168d9d3e80893beccc44`  
		Last Modified: Tue, 03 Dec 2024 02:52:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:eba2a7eb6319e4bd14dc22ef6644bed9b05dace9b933201b79176c233d130cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e792085a9084d7f845b6d9f33090a1e309f2f1755406410b2f3c07bae3ebb0`

```dockerfile
```

-	Layers:
	-	`sha256:f8db31c135756253792fe486578d6a749ffa77708f72dafdbb1ccaaf0153c47b`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 2.4 MB (2447016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cedf662b1c4d20362315198477517404af44184163db6eafe440edbfa434a99`  
		Last Modified: Tue, 03 Dec 2024 02:52:23 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:820ad4d23728521a82841b2cf63c4c7cd6e7f3bde54bfc6760c8db09b235cdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192669878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e15e4f927bd54ab31a6f42a69a6366c4e1837eabba4a3f001cc47ad84e7271f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc72b80b653978b6782bf494e51729ed99d337e4b8ec2ee5e0d6d525eb9051`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 5.7 MB (5679154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bf2693ee77f996b5ddce9f592a33d06fd5bff9916a3d32fffe38fc60b683b5`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 157.8 MB (157784869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868b4e5b8ff97c1490af9439a98eebf5bb5909d5192d5b0afa848af37966a1d1`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:891500a192a6129cdb617516e9b66fedbb858901d8851a931cc01620800d3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05ca23656c741272fcba266db9fd174c8838dcd359666ef537732e0df68d042`

```dockerfile
```

-	Layers:
	-	`sha256:ba949ffebd0805d506e2244e0c6474befcd6fa7d15c72a74b9961c02666dfa36`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 2.4 MB (2445056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f604a9f7020b898316574dde640cd26a6658d2153ebc7c0919e8b12f9a875b`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:30112123ce291e6d21205323c5f4ed69380d3c731b307afb38561db306e198a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193613396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf14335e4c3622ad827c74025e9143a232c789e78661ca2af2bbed3f453d27bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d1148f8fffb7847e45ac4930cd58d42bc12795484cce61b255b13c0101744d`  
		Last Modified: Tue, 03 Dec 2024 02:38:48 GMT  
		Size: 155.5 MB (155493317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996d347c0409e68f13a4f5b718c28a63aedcc0a85e561b9163c8af5a1383d40b`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:431a04b9e4dae61fa620fa2987f0ad882d48c99d09403124ed84a1a386436e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c5c352e33d40810b621b047241f02f7d3e2c5c118a8622a06a7ffc97d4cbcf`

```dockerfile
```

-	Layers:
	-	`sha256:de998a6eea7f1c9f08dd6c8869207b0d2b8c717c9536295faa3beb605956f70c`  
		Last Modified: Tue, 03 Dec 2024 02:38:44 GMT  
		Size: 2.5 MB (2451149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c904a42c879a49aaf8180233934f5332655e371a640e5e4d2fced5fed542b237`  
		Last Modified: Tue, 03 Dec 2024 02:38:43 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-bullseye`

```console
$ docker pull julia@sha256:fdba313cb6ee5b3d997b4ddfe55bd4dd0bb30d21d6cdd349eef1356a495a4c0e
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
$ docker pull julia@sha256:a4fbe2cad2992c27b3fdb8d90855c08f070511bb9172692ab4ed51e22fc617a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf895713fcc9a37a82015cd30894eec904235dca77d59a87e1d6cc21c93d5018`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e494ac0fd0b4e883b6e84ecfeb34ec110a9703aa6fa0b2468151782e1cf6b7db`  
		Last Modified: Tue, 03 Dec 2024 03:27:21 GMT  
		Size: 2.2 MB (2222664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43995af421ba68e5cd3ad6338e70e7008a92457b3aea6551a449d5694ba9dd70`  
		Last Modified: Tue, 03 Dec 2024 03:27:25 GMT  
		Size: 175.9 MB (175895537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805ba392b197ea6ec4d51520acf682e4d0d9945182c2e3686648d9c06afbec1`  
		Last Modified: Tue, 03 Dec 2024 03:27:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:5ab84d849f0db958c8e195b8e06ce50c6bd059c602b957d4459960ff234c4472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179fc31fd44a24ba31f25256029a7664d6bee1bbce8cac497aa603cfa70801af`

```dockerfile
```

-	Layers:
	-	`sha256:00a005e5a9a81b7f85ea2141981c56c974ae58de7a62a74a9834322411980dd0`  
		Last Modified: Tue, 03 Dec 2024 03:27:21 GMT  
		Size: 2.7 MB (2715778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ac29469c9bb625267d90a13f820881722766f628dc5f57b45840b3249bb410`  
		Last Modified: Tue, 03 Dec 2024 03:27:20 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4150795cf077fcd522ff1d05ea171dc4273f66a4f95d5df78c06afbbdf0cfcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d1979226dfc42bfad4a752600117d4cee9c5ff26a8e98c3276b7a667aba56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d5055a1eeee0d8c4e020579309e11571a87409737b4f8ab2f5e39ed2588ae6`  
		Last Modified: Tue, 03 Dec 2024 02:53:21 GMT  
		Size: 177.7 MB (177651869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbd9754aeac347190f4e53fbc0c7e3223d7204e7f2e95965102c32523d4d300`  
		Last Modified: Tue, 03 Dec 2024 02:53:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4bce91d98cd9185ccbfdb2886407374c978aec241bd70b12b8bf96a81b076f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b313814c5443bd96a13d5821c207b33736559ca2b96185cfdb8c3982cfcec83`

```dockerfile
```

-	Layers:
	-	`sha256:ac7e3ee8289ccbe4361c75c054536cbc5b67ce2d8632c2bd6da319e85328cbe5`  
		Last Modified: Tue, 03 Dec 2024 02:53:18 GMT  
		Size: 2.7 MB (2714794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d087e594d94e8666744b2269657b4ea46a84e1c203dd9761f9885b804305c3c9`  
		Last Modified: Tue, 03 Dec 2024 02:53:17 GMT  
		Size: 16.7 KB (16719 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:fdb6080560a8a147629a9cd9c79b96896b6135c42cdc21f716a156756c1a8070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ce640537bccea32e674f3a7553aef9d385a55ef052f8731782d2479e332c63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84a64daeb38ef810055a734dfb9badf83fb560c812fead338da22c961649f8b`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 2.3 MB (2328071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dba70bb5085d5400c49175761f7e129c1cdf188f01e42df277dba7c2621299c`  
		Last Modified: Tue, 03 Dec 2024 02:16:17 GMT  
		Size: 157.8 MB (157784861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cce4946cb41578a643e906c38307dbdc4ba800d23419ae86829f7ca0aef820`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cb2cb6ff8e7dc3a7eea0ed455e4b99a15c6aaaa894713f0b5ac1f80fab633c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414a2fb3b2020de32e6f0ecb10190c5c106287b6e5fcfd7bbec871b182746000`

```dockerfile
```

-	Layers:
	-	`sha256:cf3c6f258231b32e3cd1faf6476412948a607e9a5e0be33bf6b7cf2f6fe8a971`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 2.7 MB (2712886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928bbabcbaf74430af1d0d157bb8904de585cf76421b1720a41cd7bdbf798021`  
		Last Modified: Tue, 03 Dec 2024 02:16:14 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-windowsservercore`

```console
$ docker pull julia@sha256:10b1dac30692ba42e1f28b104a13fa6197e288bf82ddae8279d05b5b31879f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.10.7-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:f7b4ede3f5c2408c7c8534ec776ce9bc36d5bcb0a887543fb9017369728acf0b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441583248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71b7014f17ba69e4a32950bdcbaa9d1f502c06ea47238ce7d47f95377a8cb1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 27 Nov 2024 18:23:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:09 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:24:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:24:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa6aa624f3bfd9ddbb2bfa80e6906c4f9407490a2bb7a1c8eec783221936c8`  
		Last Modified: Wed, 27 Nov 2024 18:24:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0aedfd409a9653247572a7614e80df4f8f1140b3d03c06e2d9fdcc793976b5`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd3a3e2f4588b48b57565995636ea71d461d49b186a056c0d9ce206c35b7834`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6914c1e7bd201a0c735819a46795e058b54b2d6ace74f8aee1d6aa257cb1d`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9914aa6cc20f1ce5afa64235fff7aa7e1a3483d84fc00fa49b3692db59fb0b`  
		Last Modified: Wed, 27 Nov 2024 18:25:11 GMT  
		Size: 189.1 MB (189092535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6826d228b0b39cba020f951d56ef9a45dffeeb1a81045313b4f39665b08aa9`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:2523b646ff1bbf02eadb2268d9b4fe0edfefe60d9da0d56fa184305bfe27d471
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199873526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1356e5c8e2b74a52a101c26c287939349c27a5af5f0b31a1080c2b58fb302a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 27 Nov 2024 18:23:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:06 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:25:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:25:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229fa5e9f995bc80cefd5d49c4bce39025cff42c23bac06ecccd794d3f57cd3`  
		Last Modified: Wed, 27 Nov 2024 18:25:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af840676c667902bf03b5f217acae860de62e50d74b46974db17964b306ba005`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1fbf2c4207a2b3a7151f3c87fadf010211963c8a7023a2b751c3ed49f982e`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa5fff7ec0d49051cc0c1319dd5976a72b9fe232fc5f932950a3a63ef293732`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfd53f8cac131a4112a31780174b170cb25bcfadfec5211d720d0ededb111b4`  
		Last Modified: Wed, 27 Nov 2024 18:25:42 GMT  
		Size: 189.2 MB (189213272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89e389b7bba7125a7cc1a4756dd955387fcacf64e61c88c7a015730160dabc`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:33c7c7c37047a0544e3c0d7502c1dd9e209bd884b9a9227dc3b3e52c0bba83f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `julia:1.10.7-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:2523b646ff1bbf02eadb2268d9b4fe0edfefe60d9da0d56fa184305bfe27d471
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199873526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1356e5c8e2b74a52a101c26c287939349c27a5af5f0b31a1080c2b58fb302a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 27 Nov 2024 18:23:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:06 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:07 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:25:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:25:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229fa5e9f995bc80cefd5d49c4bce39025cff42c23bac06ecccd794d3f57cd3`  
		Last Modified: Wed, 27 Nov 2024 18:25:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af840676c667902bf03b5f217acae860de62e50d74b46974db17964b306ba005`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb1fbf2c4207a2b3a7151f3c87fadf010211963c8a7023a2b751c3ed49f982e`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa5fff7ec0d49051cc0c1319dd5976a72b9fe232fc5f932950a3a63ef293732`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfd53f8cac131a4112a31780174b170cb25bcfadfec5211d720d0ededb111b4`  
		Last Modified: Wed, 27 Nov 2024 18:25:42 GMT  
		Size: 189.2 MB (189213272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc89e389b7bba7125a7cc1a4756dd955387fcacf64e61c88c7a015730160dabc`  
		Last Modified: Wed, 27 Nov 2024 18:25:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:f7a5ebe44595b1ddd706575a1c3e42c36b508c2b40befe61b064d92838455d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `julia:1.10.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:f7b4ede3f5c2408c7c8534ec776ce9bc36d5bcb0a887543fb9017369728acf0b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441583248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b71b7014f17ba69e4a32950bdcbaa9d1f502c06ea47238ce7d47f95377a8cb1`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Wed, 27 Nov 2024 18:23:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 18:23:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 27 Nov 2024 18:23:09 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 27 Nov 2024 18:24:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 27 Nov 2024 18:24:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baa6aa624f3bfd9ddbb2bfa80e6906c4f9407490a2bb7a1c8eec783221936c8`  
		Last Modified: Wed, 27 Nov 2024 18:24:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0aedfd409a9653247572a7614e80df4f8f1140b3d03c06e2d9fdcc793976b5`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd3a3e2f4588b48b57565995636ea71d461d49b186a056c0d9ce206c35b7834`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6914c1e7bd201a0c735819a46795e058b54b2d6ace74f8aee1d6aa257cb1d`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9914aa6cc20f1ce5afa64235fff7aa7e1a3483d84fc00fa49b3692db59fb0b`  
		Last Modified: Wed, 27 Nov 2024 18:25:11 GMT  
		Size: 189.1 MB (189092535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6826d228b0b39cba020f951d56ef9a45dffeeb1a81045313b4f39665b08aa9`  
		Last Modified: Wed, 27 Nov 2024 18:24:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:b3aca3cb8b8d22c8d260cc0144d1c08f6479bf0247bff7675a9b36cf133aa91e
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
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:f8032b445fbfe3a0e5af146feaff626877dc7b883294eec49a3f229a03fc4381
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
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:9ad976e364edc34edd72583734a234e66013f7c895fc1bc9c8248b59592ecd29
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
$ docker pull julia@sha256:e21ad0137c8b8a15b07d3f6195f181369084e6886674d03d719466e1b8e693b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289573975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283efac7b94defa0b6bf2d95465edbfa72c96aa45afe84530634df90f493a72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf17a4a247bda6618c4fd4a5e2f697d84b4575bbcbf5eed6aec8b9683260fa`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f3196fc55c0e1e266503f136dee778f9b3fb1a1b7543173ba25f340eed634`  
		Last Modified: Tue, 03 Dec 2024 02:17:44 GMT  
		Size: 257.1 MB (257098268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11c3c7d35a020e8396741424315667aa7faa7a2ca25960cc125143b9abe43d1`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:71390e2a136bad7f3e40597957def443cd71973d3311409ab6d4a6549dfaa6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c1127c7065175fb5bca231291874782eb785033aa605ae403ef16fa16d3586`

```dockerfile
```

-	Layers:
	-	`sha256:1d374a3dba343ba78f019fa976918d8e81b3b75e469edfb85cc0aaf1875c1128`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.7 MB (2715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8dd6d13c2a59f9838ab75ab90af9396914516dedbb45330ee63f7c2d7b8442`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f798c57648a0e9839faed7b80605afe746f10e91233bd9c8d56323833473f113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284962256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8bac96e1f5e359fb62d7ea7ea96350af77e69578b892ddc739b837d4fd7dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ecb8ff42f5d159e95271acfe6754860a7e5caa81f142e067200dd251f84166`  
		Last Modified: Tue, 03 Dec 2024 02:51:29 GMT  
		Size: 254.0 MB (254006669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603847c85db951da72dc623ab26bfa0d8b611f3c6000045ee8aec29142e4084e`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2ae870ab0aa4cd721b585fd780c47adba288682908c90fd92712ea9066906d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a711dd34c6db70375fac74699c4537d82afccb7009df2ecd59365e9c0fc3a9a6`

```dockerfile
```

-	Layers:
	-	`sha256:422a95300688a576bcbcbffd8a35fc6ddaeda8dd68da465003ee23070526ca61`  
		Last Modified: Tue, 03 Dec 2024 02:51:24 GMT  
		Size: 2.7 MB (2715422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1a191ece5d050addd22e2bcd4b95df69c526f26db24f10570c867801c775e0`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:b8c5e00251f9072e18e6056341881292bda3ac7500641b86ea9b162f8ce1db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57d4abd1e50829e2dc8e48cdba72d41ceb67b43b3741bfdc515f360389b2dea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac99d6f64ac9099c145ee3db62bcfb8030850642fcdaa4429e523d6dc8fd80`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.3 MB (2328053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d157d5a761800b63ba98bdc82e9dcf56f24fc61b6df22284c10440f8a9e80`  
		Last Modified: Tue, 03 Dec 2024 02:15:06 GMT  
		Size: 234.7 MB (234658568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7d4ace25cdb8d2c5af7784bbf5625e038a9aa4e5b4ca90923f419010e1865`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:91263673457c8bc3c6a544d8083a5a7c3cd1c0dd296375da915012199187e637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecac8533b702416bddd428020d4c57838b9e633eff9c177f36aeddfa3e0d6c5`

```dockerfile
```

-	Layers:
	-	`sha256:2475be50377543347fcc684091713d6f8f1dd527b1e6eb8e5583d6e2c1928b81`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.7 MB (2712258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8835e1f2292911817cb16e50f7a082b1766f67c8fca1808216394d3b54ff92da`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:b34203110520d462f78b9b325fa3286f72d98752663c82f296ebb1f05977029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:01bef96047f40618e8bccb38b594dcb343f5bae3fbe5187006d2f10f87744502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2a0dd1446d94fdbffd2075628d86db8741612040d64d4a94e23b42b57ab2f462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1`

```console
$ docker pull julia@sha256:b3aca3cb8b8d22c8d260cc0144d1c08f6479bf0247bff7675a9b36cf133aa91e
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
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.11.1` - linux; amd64

```console
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.1` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-bookworm`

```console
$ docker pull julia@sha256:f8032b445fbfe3a0e5af146feaff626877dc7b883294eec49a3f229a03fc4381
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

### `julia:1.11.1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.1-bullseye`

```console
$ docker pull julia@sha256:9ad976e364edc34edd72583734a234e66013f7c895fc1bc9c8248b59592ecd29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:e21ad0137c8b8a15b07d3f6195f181369084e6886674d03d719466e1b8e693b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289573975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283efac7b94defa0b6bf2d95465edbfa72c96aa45afe84530634df90f493a72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf17a4a247bda6618c4fd4a5e2f697d84b4575bbcbf5eed6aec8b9683260fa`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f3196fc55c0e1e266503f136dee778f9b3fb1a1b7543173ba25f340eed634`  
		Last Modified: Tue, 03 Dec 2024 02:17:44 GMT  
		Size: 257.1 MB (257098268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11c3c7d35a020e8396741424315667aa7faa7a2ca25960cc125143b9abe43d1`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:71390e2a136bad7f3e40597957def443cd71973d3311409ab6d4a6549dfaa6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c1127c7065175fb5bca231291874782eb785033aa605ae403ef16fa16d3586`

```dockerfile
```

-	Layers:
	-	`sha256:1d374a3dba343ba78f019fa976918d8e81b3b75e469edfb85cc0aaf1875c1128`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.7 MB (2715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8dd6d13c2a59f9838ab75ab90af9396914516dedbb45330ee63f7c2d7b8442`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f798c57648a0e9839faed7b80605afe746f10e91233bd9c8d56323833473f113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284962256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8bac96e1f5e359fb62d7ea7ea96350af77e69578b892ddc739b837d4fd7dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ecb8ff42f5d159e95271acfe6754860a7e5caa81f142e067200dd251f84166`  
		Last Modified: Tue, 03 Dec 2024 02:51:29 GMT  
		Size: 254.0 MB (254006669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603847c85db951da72dc623ab26bfa0d8b611f3c6000045ee8aec29142e4084e`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2ae870ab0aa4cd721b585fd780c47adba288682908c90fd92712ea9066906d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a711dd34c6db70375fac74699c4537d82afccb7009df2ecd59365e9c0fc3a9a6`

```dockerfile
```

-	Layers:
	-	`sha256:422a95300688a576bcbcbffd8a35fc6ddaeda8dd68da465003ee23070526ca61`  
		Last Modified: Tue, 03 Dec 2024 02:51:24 GMT  
		Size: 2.7 MB (2715422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1a191ece5d050addd22e2bcd4b95df69c526f26db24f10570c867801c775e0`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:b8c5e00251f9072e18e6056341881292bda3ac7500641b86ea9b162f8ce1db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57d4abd1e50829e2dc8e48cdba72d41ceb67b43b3741bfdc515f360389b2dea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac99d6f64ac9099c145ee3db62bcfb8030850642fcdaa4429e523d6dc8fd80`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.3 MB (2328053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d157d5a761800b63ba98bdc82e9dcf56f24fc61b6df22284c10440f8a9e80`  
		Last Modified: Tue, 03 Dec 2024 02:15:06 GMT  
		Size: 234.7 MB (234658568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7d4ace25cdb8d2c5af7784bbf5625e038a9aa4e5b4ca90923f419010e1865`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:91263673457c8bc3c6a544d8083a5a7c3cd1c0dd296375da915012199187e637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecac8533b702416bddd428020d4c57838b9e633eff9c177f36aeddfa3e0d6c5`

```dockerfile
```

-	Layers:
	-	`sha256:2475be50377543347fcc684091713d6f8f1dd527b1e6eb8e5583d6e2c1928b81`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.7 MB (2712258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8835e1f2292911817cb16e50f7a082b1766f67c8fca1808216394d3b54ff92da`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.1-windowsservercore`

```console
$ docker pull julia@sha256:b34203110520d462f78b9b325fa3286f72d98752663c82f296ebb1f05977029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:1.11.1-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.1-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-windowsservercore-1809`

```console
$ docker pull julia@sha256:01bef96047f40618e8bccb38b594dcb343f5bae3fbe5187006d2f10f87744502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `julia:1.11.1-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2a0dd1446d94fdbffd2075628d86db8741612040d64d4a94e23b42b57ab2f462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `julia:1.11.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:f8032b445fbfe3a0e5af146feaff626877dc7b883294eec49a3f229a03fc4381
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
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:9ad976e364edc34edd72583734a234e66013f7c895fc1bc9c8248b59592ecd29
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
$ docker pull julia@sha256:e21ad0137c8b8a15b07d3f6195f181369084e6886674d03d719466e1b8e693b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289573975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283efac7b94defa0b6bf2d95465edbfa72c96aa45afe84530634df90f493a72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf17a4a247bda6618c4fd4a5e2f697d84b4575bbcbf5eed6aec8b9683260fa`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f3196fc55c0e1e266503f136dee778f9b3fb1a1b7543173ba25f340eed634`  
		Last Modified: Tue, 03 Dec 2024 02:17:44 GMT  
		Size: 257.1 MB (257098268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11c3c7d35a020e8396741424315667aa7faa7a2ca25960cc125143b9abe43d1`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:71390e2a136bad7f3e40597957def443cd71973d3311409ab6d4a6549dfaa6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c1127c7065175fb5bca231291874782eb785033aa605ae403ef16fa16d3586`

```dockerfile
```

-	Layers:
	-	`sha256:1d374a3dba343ba78f019fa976918d8e81b3b75e469edfb85cc0aaf1875c1128`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.7 MB (2715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8dd6d13c2a59f9838ab75ab90af9396914516dedbb45330ee63f7c2d7b8442`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f798c57648a0e9839faed7b80605afe746f10e91233bd9c8d56323833473f113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284962256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8bac96e1f5e359fb62d7ea7ea96350af77e69578b892ddc739b837d4fd7dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ecb8ff42f5d159e95271acfe6754860a7e5caa81f142e067200dd251f84166`  
		Last Modified: Tue, 03 Dec 2024 02:51:29 GMT  
		Size: 254.0 MB (254006669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603847c85db951da72dc623ab26bfa0d8b611f3c6000045ee8aec29142e4084e`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2ae870ab0aa4cd721b585fd780c47adba288682908c90fd92712ea9066906d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a711dd34c6db70375fac74699c4537d82afccb7009df2ecd59365e9c0fc3a9a6`

```dockerfile
```

-	Layers:
	-	`sha256:422a95300688a576bcbcbffd8a35fc6ddaeda8dd68da465003ee23070526ca61`  
		Last Modified: Tue, 03 Dec 2024 02:51:24 GMT  
		Size: 2.7 MB (2715422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1a191ece5d050addd22e2bcd4b95df69c526f26db24f10570c867801c775e0`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:b8c5e00251f9072e18e6056341881292bda3ac7500641b86ea9b162f8ce1db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57d4abd1e50829e2dc8e48cdba72d41ceb67b43b3741bfdc515f360389b2dea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac99d6f64ac9099c145ee3db62bcfb8030850642fcdaa4429e523d6dc8fd80`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.3 MB (2328053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d157d5a761800b63ba98bdc82e9dcf56f24fc61b6df22284c10440f8a9e80`  
		Last Modified: Tue, 03 Dec 2024 02:15:06 GMT  
		Size: 234.7 MB (234658568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7d4ace25cdb8d2c5af7784bbf5625e038a9aa4e5b4ca90923f419010e1865`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:91263673457c8bc3c6a544d8083a5a7c3cd1c0dd296375da915012199187e637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecac8533b702416bddd428020d4c57838b9e633eff9c177f36aeddfa3e0d6c5`

```dockerfile
```

-	Layers:
	-	`sha256:2475be50377543347fcc684091713d6f8f1dd527b1e6eb8e5583d6e2c1928b81`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.7 MB (2712258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8835e1f2292911817cb16e50f7a082b1766f67c8fca1808216394d3b54ff92da`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:b3aca3cb8b8d22c8d260cc0144d1c08f6479bf0247bff7675a9b36cf133aa91e
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
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:d03159c422f5b8f0ec9a3f17e8228f9c806e697a5adccd954a702844844e8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290848430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfec6f3cb4967e391b1229336eb200b18825842e3eea9e6ef78536bb72cf00f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8792d0efcb798d6259dc7cbcc42e29e474bb2c91fba352fd73de1b8f2e6edb`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 5.5 MB (5518421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196746a9411d2148762a2fc607133290231ff3fb4ed56689f4b2a9e9c8635c65`  
		Last Modified: Tue, 03 Dec 2024 03:27:33 GMT  
		Size: 257.1 MB (257098058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d24d55fb4249d6efd4736b5c623cf3438babfd56ad3f1078c5f103e1aac38`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:8c8c293088bf94af765247c00616420c5c2a06cdb840a66368c7fa5e3ea341ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3692ba29d5da582cdb0ecab12f7f2a2f9cd375db7e6f3eefa4c19cd8255286`

```dockerfile
```

-	Layers:
	-	`sha256:3497d66a5443880473a8560b64a0d5a0f2da4c9d1ae22686591c7de5f5ba28c1`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 2.4 MB (2447928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e79d42c836fa2a73c49cf324d241493eee87c60df715a8a25ca8b3204efa35e`  
		Last Modified: Tue, 03 Dec 2024 03:27:30 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ddf36aa726c0d079a60237a816e174f69b547c998f51a9b2833d672d81f71c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287412043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaa3b7fa5b5c9b238d0770621f6a20ada74bee8b24dc8b0a785a45361f78647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dc19524960cdd82da6b406c31ddbfbaeb65f9a7bddc588b8c79a41ec88a6b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 5.3 MB (5346075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd2ce26587881de1937f634170620a3d0217355d81e24c444eeb43237e307`  
		Last Modified: Tue, 03 Dec 2024 02:50:14 GMT  
		Size: 254.0 MB (254006791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa784cd7464d6537aec09b41e04d6c7eebaf9738bf0386b9b66ed8bf36aaa116`  
		Last Modified: Tue, 03 Dec 2024 02:50:08 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:a7eeacf62bbaf9c1a9b475f71ff2207d1b8974d6181d63d0bf380185d5251557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bdf617cc1f3805036341700a4b7e095b59e0618248101dc3ecdb8cca1ac24a`

```dockerfile
```

-	Layers:
	-	`sha256:b57fa4c8f0e50248513a8d39f435c36a95776f0b1d915a20999d24393806d6c2`  
		Last Modified: Tue, 03 Dec 2024 02:50:10 GMT  
		Size: 2.4 MB (2448250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51473d1de90daf5cc2cf821801ce6d96b9abda134c1e293e6b21eeb46f83fe2b`  
		Last Modified: Tue, 03 Dec 2024 02:50:09 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:88c89c040fcfb2bff27f237f98167bdff87471fa7a70f7b2da7f7aceb525908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269542587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe65cee505befe4e97648acc87c89fa138b7f0dfda68d7436fc7275f114f739`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b042ddc40b6269e978cad390be50f849ecdf11c5077f784ab74339cf3034c`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 5.7 MB (5679121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834376b21f79821236a2ab2b5ae007a865ff3c76990233c56dd4a3e639dad43`  
		Last Modified: Tue, 03 Dec 2024 02:15:02 GMT  
		Size: 234.7 MB (234657609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a8ba0a0c49813b9aaf6df75a1c652cadfb578bc7159435067a3aa88059f303`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:e44acfa84b9c107629a20c7880df9e983611b18615f3bf5b1601b824b6f048ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dbd6c2a794f2998a9a2e34cf731e6333ff0f4e224ce2aa5fdb01f405430816`

```dockerfile
```

-	Layers:
	-	`sha256:7eef1e88c6ffd91109134fb007e3f1d31cf4fc63357c834adf1fecb0e5fbbb98`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 2.4 MB (2445000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3c1a0b69254f9cf8522702d653db157845d640ecc86a2fdef85d4f26a73cdf`  
		Last Modified: Tue, 03 Dec 2024 02:14:56 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:b23adba87b11bd54cfc38b154cb62177953369d2f1bfa394244ea8b9d019eb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282595281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f5d13373c77a628384d99298a0b27a97e61783b6fb11bd89b71a9a2c7df88f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee6f72457100da92ed891299fef0234da9579f781622a6071d551f5f481e9a0`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 6.1 MB (6056445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bddb401e87bacd7cf7d7634ef9ec0b6f9554bdf95c236f8302bb384892e40bd`  
		Last Modified: Tue, 03 Dec 2024 02:36:55 GMT  
		Size: 244.5 MB (244475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258df8db73936ea510423d8bbac76bc125fa0d1775764afa166ee39fda76e19d`  
		Last Modified: Tue, 03 Dec 2024 02:36:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:eb7d927555213b87952fa04e706205ed11b41b16ee706f1f85d48ac3ac9b0b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1cb27bfd5de75a212ed4ca4892b312f9b64c737ab63c1e98dfc1c2f5e24be9`

```dockerfile
```

-	Layers:
	-	`sha256:a7b5a95fba64f975f649877a95d5417dfd0e029d6086dbfd51c945ddae85c4fd`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 2.5 MB (2452359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90894d1de5700ac5573cc5121a071fa8c4ed4ceeff756aef709d4a793cf55e1`  
		Last Modified: Tue, 03 Dec 2024 02:36:43 GMT  
		Size: 18.5 KB (18468 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:b34203110520d462f78b9b325fa3286f72d98752663c82f296ebb1f05977029b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:01bef96047f40618e8bccb38b594dcb343f5bae3fbe5187006d2f10f87744502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:04d65dc71825a0e62873aa07f2bf958e1cc630f2f988f1e20c7c27b115d59062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2263738589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf04bc0ee604ef14cf94ccb822bd9787af76ecc9317bb525bda6b271e76f8aab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:11:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:11:06 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 20:11:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 20:11:08 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 20:13:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:13:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ac7478d781520948dee873cb5d2cf770bd10c3c6ed930aba62173776da168`  
		Last Modified: Thu, 14 Nov 2024 20:13:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88d29a5daa7282de02478c5c6ebf7b4b0a0e09dd5837f81b0f5dd5e3e81c38d`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe1ac052e14f2c90eede131b7382fcf5c7acefa5e5174deed1eb350a3522460`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c9e3256eb12b700ef990e6118dcc919487c7500e38aebda079c0260444522`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90bd610af82143c3dbf950d7b9ea5988a4d48cf1691dc0b2f657ef1ee982788`  
		Last Modified: Thu, 14 Nov 2024 20:13:48 GMT  
		Size: 253.1 MB (253078308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efefb51ffffb89baae8c1ddfe0ad3d79bdd9dd40ae825256908986738652a3b`  
		Last Modified: Thu, 14 Nov 2024 20:13:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2a0dd1446d94fdbffd2075628d86db8741612040d64d4a94e23b42b57ab2f462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull julia@sha256:5473412d40ee7da801ba0bed69ead384c932edb63bd20968f2d80c6cefc2384c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef5c641a7bc603770fb28a5e51723e299eea5e6502b524bff730313925ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 21:09:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 14 Nov 2024 21:09:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 14 Nov 2024 21:09:54 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 14 Nov 2024 21:10:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 21:11:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383d047b8aa90b5d767f0d79c755b6f3deb7acc8fae168031e6d993bc5e09547`  
		Last Modified: Thu, 14 Nov 2024 21:11:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c22e500af5e35199a7c9e4ccb603cfea143dc176b2b36969589af6d3a17def7`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806b688bb18a36dc39adf3181213ecd9d04a688829825e001ee783e0b47174c1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517f1846367d6ca3492fa4e95f93077650f30858291ede06b582862e2fd93bc1`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb6986a4e8fd22abbf4b71690c2c08c6083f0dc7ef52b7cd0cb23b32432a175`  
		Last Modified: Thu, 14 Nov 2024 21:11:36 GMT  
		Size: 252.9 MB (252947423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a407cb80af5e8d1fc4e3076bc4a9c51733fe8f2ccc3c1195305ba42ed5183f76`  
		Last Modified: Thu, 14 Nov 2024 21:11:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
