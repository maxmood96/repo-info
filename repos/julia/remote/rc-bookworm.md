## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:3839c8f188036a22e00e05fb921903658e51a43fced1f7ff035c0c58a62b0764
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

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:7fad608a363e805293db3b3ebe14fa6194fa25ba2d252048cd264dac7900aaca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288594937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13ac76f40450472cb896ce2a6aa6f9f310f957a4eebf2e25f707b0cf8908d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 May 2024 17:59:24 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Wed, 29 May 2024 17:59:24 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48087116c7d5fa606977d760eb30f1ffb017ed5a7c7c173327ec876f7feadbd`  
		Last Modified: Thu, 13 Jun 2024 18:29:33 GMT  
		Size: 5.5 MB (5515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c87d186ad6745a380012253d850a78f207d2dc903c14a4d1cd8bc7f343a87e2`  
		Last Modified: Thu, 13 Jun 2024 18:29:40 GMT  
		Size: 253.9 MB (253928924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3976578de2f267188eb11bc2886d6fe35687513702f6ea6ee140d835610708`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5ff8e24173ced8369f8c1e17a6c4697056026a01a283912294b64a74b02b4b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b675861d283a591340cdf503c212c9f46ef9fa8be661c91570d7badbdebb759`

```dockerfile
```

-	Layers:
	-	`sha256:a617a7781627541529a7a5574eb7c5cb19a2b0cb7e473e530c51a837ddb7fa06`  
		Last Modified: Thu, 13 Jun 2024 18:29:33 GMT  
		Size: 2.4 MB (2413059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65330c4fbda814da7e53c351c19b3b252b7672a8ca44655a79f809baf517523`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7cb1733ee699624b95f8c4f001f5e07e2a743338dd4b6d29d98c505eb1ef2fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285318533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95ec65a3afc7c20ab17bac6fced5ad958667d3a1a22fd04f23080601e6368c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 May 2024 17:59:24 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Wed, 29 May 2024 17:59:24 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318e7a947efae55b3087175cfc267ec05fa36fd5cee24cd53f66ab5fcfb6495`  
		Last Modified: Thu, 13 Jun 2024 19:20:07 GMT  
		Size: 5.3 MB (5339473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c0b9580eb5b62706f5b4949a386e4e6cd80c5522f2fd8a97340255c664f671`  
		Last Modified: Thu, 13 Jun 2024 19:20:12 GMT  
		Size: 250.8 MB (250799020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709771913312e3489c7decd19f111b9a86092b0b92aa935d0da70e347cd4fde4`  
		Last Modified: Thu, 13 Jun 2024 19:20:06 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:95834e6b6f51ce845ba3b54a672d53f06c9d87744d4308ec48ec8f0107b5a457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddef36354d0dd959849525fae07eb9b46d48def541ec28839d165b6683ed2c1a`

```dockerfile
```

-	Layers:
	-	`sha256:f276270e07a1143557106a7f603a94ce0fc66c5371ba04ec5fe47de5d35c3567`  
		Last Modified: Thu, 13 Jun 2024 19:20:07 GMT  
		Size: 2.4 MB (2413357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d343483bd9e9239896c4c037d121eb131192ea4844a1bde10ff3066a946c04`  
		Last Modified: Thu, 13 Jun 2024 19:20:06 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:cf6e094061cfd1f1c6e5e81d1357c62683bbb7fd9630d87747274dabaa7e415f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.0 MB (266984866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb8d571ec5a30a24b8326a205184861af2044d7847b980842ce4d197882d5f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 May 2024 17:59:24 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Wed, 29 May 2024 17:59:24 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e108a24c0acf91064260eec4124b7dbabe3e5c7fbc95680d98852639ee191d`  
		Last Modified: Thu, 13 Jun 2024 01:59:46 GMT  
		Size: 5.7 MB (5672140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4725cd94c4fc79fc5a206562acc650a146de8b46739c0575383316100bd9866`  
		Last Modified: Thu, 13 Jun 2024 01:59:51 GMT  
		Size: 231.1 MB (231149696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac25663017975862d3dd90a07bba7cbacab8f4d157a251cec5f87e9f34c3e9c`  
		Last Modified: Thu, 13 Jun 2024 01:59:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:684d55d059cac6b6698ce4296d5e274bb6ee23bb7ee2267f930cb7343374323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c46bb156712e90adf3ce636f23aceb42aec9b9e7e9e463899de92d2eefafa`

```dockerfile
```

-	Layers:
	-	`sha256:f434b14cc27479bbb172d91fd4015d5e00f4767f31deb203f0a3d9eeef740697`  
		Last Modified: Thu, 13 Jun 2024 01:59:46 GMT  
		Size: 2.4 MB (2410141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae0a17b384c15beefc93b82912f7f04e36012b03c1d011212cab865f315eaf9`  
		Last Modified: Thu, 13 Jun 2024 01:59:46 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:d380e9bf733a594fc6dcc56f10ee9fa4e942cf97fd4bb758dd8e1a775e6cf7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280838788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d03bd2e7d8d3fba190afb45ab675045aa65fd6eddc3b062ec9e5500b1a39ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3229ef95efa02c8096dfb801877c49ed4db2f759985e91d23cee9d29a3782ef`  
		Last Modified: Thu, 30 May 2024 03:13:12 GMT  
		Size: 6.0 MB (6047089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d62f3caa40f4f3231d2dcbbe548eea0c582750cbc1c5594a3e3e7e23d13bc8e`  
		Last Modified: Thu, 30 May 2024 03:13:18 GMT  
		Size: 241.7 MB (241650163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1d9cc13b62c81af0bd9e50aadc7dcf8eb18007b66d3c286cbd30841527fd11`  
		Last Modified: Thu, 30 May 2024 03:13:11 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f06fc53a8df01222405011af9e21844aba6d5cb3bc7ce773b710c58e94667c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f75f7495c04ebf400520d22307d6662c0698788a5815998643a81e1ed02859`

```dockerfile
```

-	Layers:
	-	`sha256:04f1d18b4a3d0db3f1cbcbfafc28e2fd42d534274308577ee86628aefcf056fe`  
		Last Modified: Thu, 30 May 2024 03:13:12 GMT  
		Size: 2.4 MB (2417479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0eb965d1d489cc8f545de52a14b47d22ab13b6ca65ac31738f7f5655d44d53`  
		Last Modified: Thu, 30 May 2024 03:13:11 GMT  
		Size: 17.7 KB (17728 bytes)  
		MIME: application/vnd.in-toto+json
