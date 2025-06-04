## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:b33b72253ef25efd7f7dfdf99b4ce038f5c8d769e4a61d1fa0967ed08eda63e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:df18bb0b76dfcbc7972f5d17a3c99c65977f19fc0d1f6bbca164a3922e3a87d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328415079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabaf46111bcba35da59fd92c4201a6eb8fd8eb9b02e567562dd92c01fa008c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 May 2025 23:59:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Mon, 12 May 2025 23:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 12 May 2025 23:59:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Mon, 12 May 2025 23:59:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta3-linux-x86_64.tar.gz'; 			sha256='ccae00efb7e8797b33c82d3064c8b20da015cbe001848a95149a7a5bdf3b27a5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta3-linux-aarch64.tar.gz'; 			sha256='80ac186be3a581973e8d0a571f7f95b2527728bce2173383fcba628d796cad3c'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta3-linux-i686.tar.gz'; 			sha256='6bf5c7b217dcb86a66e9647935dfed39d729c94974155acb4154d4dc22c5c4ca'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 12 May 2025 23:59:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 12 May 2025 23:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 May 2025 23:59:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5962fcd746be0a9ff33f8864d8b740077dd863a8943c9cadf1b6d81942aba776`  
		Last Modified: Wed, 04 Jun 2025 01:28:38 GMT  
		Size: 5.7 MB (5714660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dea9dd92302dbc202dd457f3ba4d2faf997f46aefcf8b287bbbd6b737aaa92`  
		Last Modified: Wed, 04 Jun 2025 01:28:59 GMT  
		Size: 294.5 MB (294474721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01b03f61131e3ca127bbb5b0935f34e1f9e3af493bea89382379b99b7bc3e16`  
		Last Modified: Wed, 04 Jun 2025 01:28:37 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7c864fa9a3414efcca0e29e1afe750f545c52e621f4b9cda45ae9f673b3c077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2484740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4d086fa29c7b64303b6969245d90009534843f9afb84aeef1a30519cfe41ea`

```dockerfile
```

-	Layers:
	-	`sha256:394aefd77eac6041f3ac6ef3f4bbff57fc609d2ac9609404160232a4d25a84b3`  
		Last Modified: Wed, 21 May 2025 23:13:11 GMT  
		Size: 2.5 MB (2467469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9e6e530eb777f6dc36e67797cf157519092d2d0198a1e0eb90404ec13b8d8b`  
		Last Modified: Wed, 21 May 2025 23:13:11 GMT  
		Size: 17.3 KB (17271 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:04e3c595a3ab8a99158a1b65d2569cfd766674c96364291922cf7adaf3170626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349390449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03339831a722542269676f8131b5798f984f0a02e262fa12d1e7514cabea7e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 May 2025 23:59:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Mon, 12 May 2025 23:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 12 May 2025 23:59:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Mon, 12 May 2025 23:59:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta3-linux-x86_64.tar.gz'; 			sha256='ccae00efb7e8797b33c82d3064c8b20da015cbe001848a95149a7a5bdf3b27a5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta3-linux-aarch64.tar.gz'; 			sha256='80ac186be3a581973e8d0a571f7f95b2527728bce2173383fcba628d796cad3c'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta3-linux-i686.tar.gz'; 			sha256='6bf5c7b217dcb86a66e9647935dfed39d729c94974155acb4154d4dc22c5c4ca'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 12 May 2025 23:59:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 12 May 2025 23:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 May 2025 23:59:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d83c5c1ad223597d53263ad97471bdb00a856e9e085b8d52b21d0ebbb8821c`  
		Last Modified: Tue, 03 Jun 2025 13:35:24 GMT  
		Size: 5.5 MB (5541536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b303e2569d739f93e4d58489474db6244dbd31a2069a5e23b8e1f536691836`  
		Last Modified: Thu, 22 May 2025 00:01:09 GMT  
		Size: 315.8 MB (315783260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629d923f7084d9fa3c25ca1d8edef954b4ad134a5f8730a264791c0664609cd6`  
		Last Modified: Thu, 22 May 2025 00:00:59 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d53334848ff95746736c1fa650628f4f8622c3b6307680629f976aef65ce526b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2485181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc11d1a55965a1d612b63afe47e6ffb1fc6bf7bc271b6edc86c1ab4aa230053d`

```dockerfile
```

-	Layers:
	-	`sha256:ec338c93dd3bcc271d831c59e11b4b63fad6d1ba79f5c2e42ba73ec696281010`  
		Last Modified: Thu, 22 May 2025 00:00:59 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596f2f6d287196fc89cc46e3feaa9e5cf3bcd018fa0ddc6a703f709a1928731a`  
		Last Modified: Thu, 22 May 2025 00:00:59 GMT  
		Size: 17.4 KB (17413 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:1edab3e288952ac9bcce2121cebd57ca409dc793a22b6ba178af68adab791e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271650674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489b75dc7594b1b2e63339ab6ebe0f88e8d5400f367a683d31aa4b1f35058062`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 May 2025 23:59:27 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Mon, 12 May 2025 23:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 12 May 2025 23:59:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 May 2025 23:59:27 GMT
ENV JULIA_VERSION=1.12.0-beta3
# Mon, 12 May 2025 23:59:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta3-linux-x86_64.tar.gz'; 			sha256='ccae00efb7e8797b33c82d3064c8b20da015cbe001848a95149a7a5bdf3b27a5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta3-linux-aarch64.tar.gz'; 			sha256='80ac186be3a581973e8d0a571f7f95b2527728bce2173383fcba628d796cad3c'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta3-linux-i686.tar.gz'; 			sha256='6bf5c7b217dcb86a66e9647935dfed39d729c94974155acb4154d4dc22c5c4ca'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 12 May 2025 23:59:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 12 May 2025 23:59:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 May 2025 23:59:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8988cf184ed245421da6076968178b0c253f2816478948ba94c15ea07b78f`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 5.9 MB (5874734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158f69f1a90c24adf86b840c414a6e6201a66fc70ef363f7aec8825226e633f6`  
		Last Modified: Wed, 21 May 2025 23:12:57 GMT  
		Size: 236.6 MB (236568082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde34afcfd04bd293450f7e10856c4b22e676194d5247f181a2b9f915276c5`  
		Last Modified: Wed, 21 May 2025 23:12:51 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:59f882700a5607a706f277ac09151e78826ba593ae02a4b4cc7b02b9e6d4b2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ad7f0173cc6079813efe9edbd542ee05a7a6c09d210858d99bd0d9c1345ede`

```dockerfile
```

-	Layers:
	-	`sha256:79073a85942eb5c0306af0d0f36bc7f32e4dc79b32124b32c163d91af6e0d4a8`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 2.5 MB (2464606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57067eef14a466733342fa17724449ba5534b75a931c6c9e9c3fcb16870a8fa`  
		Last Modified: Wed, 21 May 2025 23:12:51 GMT  
		Size: 17.2 KB (17227 bytes)  
		MIME: application/vnd.in-toto+json
