## `julia:rc`

```console
$ docker pull julia@sha256:f545366e0ef796bf3f1c1cb3bcafa9f2c0fa4009ea872b5c9c3dfc4d58707122
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
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `julia:rc` - linux; amd64

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

### `julia:rc` - unknown; unknown

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

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e461d7a8af213559d1745c61d159f4c0166893c1aed4434df321191708e82813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285318311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401509d8a3dc7c8b9a926c2b760de9c51e3fac8b84d89a175884ada221baa300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef5031429e5d0f5d64d54591db2c7d845363231c4bd944ea1efcfbb6f35245`  
		Last Modified: Thu, 30 May 2024 11:33:27 GMT  
		Size: 5.3 MB (5339441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e35fe131d906e9b0f57a62f292093da676d13e4377b0551787e09cdbba2ae15`  
		Last Modified: Thu, 30 May 2024 11:33:32 GMT  
		Size: 250.8 MB (250798993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f0c4418d0f8d99d89631e7cd65cdb047569744e2fad5177236e44bc5619f8e`  
		Last Modified: Thu, 30 May 2024 11:33:26 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:c538566bb7d01ddac85b170f2c8efa87e169b1fa46de14b26b909bae12374ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc8943eb1b304b8981292186d30dea8b4bbb95d82aa0011367338c613e9083a`

```dockerfile
```

-	Layers:
	-	`sha256:67066b509b13f7822efd073377fcce126e2bca490e7680c1b9201b1dea1bea29`  
		Last Modified: Thu, 30 May 2024 11:33:27 GMT  
		Size: 2.4 MB (2413358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b32a15fae6cff5f142b2544b64db31b7e3c2ca1d4b82ff0586c9cc44d1e52a3`  
		Last Modified: Thu, 30 May 2024 11:33:27 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

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

### `julia:rc` - unknown; unknown

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

### `julia:rc` - linux; ppc64le

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

### `julia:rc` - unknown; unknown

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

### `julia:rc` - windows version 10.0.20348.2527; amd64

```console
$ docker pull julia@sha256:021b41b0bcfc58f38bf2a1577da654680099e08ff9397c60d4a4ea71ba47b8e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2367034771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad31eefdc274bc4d873e14f5a045c3d16914c054ea1a40a63fad5a218690d6d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:05:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:05:47 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 12 Jun 2024 18:05:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-beta2-win64.exe
# Wed, 12 Jun 2024 18:05:49 GMT
ENV JULIA_SHA256=e6d27f8a5819fd9e63ecb4ed19bed8a0c1ab719a5a6cf0f772c240eb44b46d68
# Wed, 12 Jun 2024 18:06:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:06:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d836b1cbe8114822d26d6d232fd2f71ea03417c0882b71fd64c9e5007994`  
		Last Modified: Wed, 12 Jun 2024 18:06:51 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90575249a29884484eb9d712b0bdd30260058c850835a6d445b211900fb03741`  
		Last Modified: Wed, 12 Jun 2024 18:06:50 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48aa561abf863134553712043a4df37cd5a631ad2cbd06b5241618f812c5348c`  
		Last Modified: Wed, 12 Jun 2024 18:06:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3df32652bf77311c40aad9a01f064b632db288db88b1590097edc1ee01b233`  
		Last Modified: Wed, 12 Jun 2024 18:06:50 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be3997769acfcb4ab6f7ef99f722867ffe2b13ecc9bf7355ac0fc486e623652`  
		Last Modified: Wed, 12 Jun 2024 18:07:21 GMT  
		Size: 248.8 MB (248849512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8533d6b015656011b1dfbaeddcc501ac0e30187ca5b4306ff95cc76b9fed1b85`  
		Last Modified: Wed, 12 Jun 2024 18:06:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.5936; amd64

```console
$ docker pull julia@sha256:aa9e71793ca1ed74c38727635776de97077aababb2a381758efae0df5cfaf6dc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2469627943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d69a10cf626749fefb8f490b3102351231e6d385cea547f0cbd2d7e2bf218`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:14:05 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 12 Jun 2024 18:14:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-beta2-win64.exe
# Wed, 12 Jun 2024 18:14:07 GMT
ENV JULIA_SHA256=e6d27f8a5819fd9e63ecb4ed19bed8a0c1ab719a5a6cf0f772c240eb44b46d68
# Wed, 12 Jun 2024 18:16:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Jun 2024 18:16:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f2848b507d340046821201398db87834f5d7a8d7e418f888f3a904e4b5afed`  
		Last Modified: Wed, 12 Jun 2024 18:16:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03878b5efd7a4a26ac690ef352963e31ca6398ebf8323539ed7732affd47507b`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc6f58c70479f78d5a9c19f8c725ca3d96e58f6ebd936977e9b958c437584f7`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71f6834e00a050a5aebc0b88a91b19df0a4104d7af64849734be80b8f351e67`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206ece9174ecfdd1698fae1fedf5c2bf920a2de5121235bf20a00a16aa8f22a9`  
		Last Modified: Wed, 12 Jun 2024 18:17:03 GMT  
		Size: 248.9 MB (248940285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88ab638f6b0150e77b9a23480dbe9d498b670181a6c91f5c01c3c26ee2e2288`  
		Last Modified: Wed, 12 Jun 2024 18:16:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
