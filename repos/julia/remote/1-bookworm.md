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
