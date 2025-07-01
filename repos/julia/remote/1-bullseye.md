## `julia:1-bullseye`

```console
$ docker pull julia@sha256:f78106d0d39138b6a9fe819eb6d91ea9d63344126bf484198c5f64309154faa2
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
$ docker pull julia@sha256:3acea388e7f1d206814649c8f5586adf88f0f83c1c4cc0f1baab5a4b7ceef424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321095285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fb0f69985ae8689d2ae8fc91c872d80331e8017484f97baed968f1d0904565`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 14 Apr 2025 23:59:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.5-linux-x86_64.tar.gz'; 			sha256='723e878c642220cc0251a0e13758c059a389cadc7f01376feaf1ea7388fe8f9c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.5-linux-aarch64.tar.gz'; 			sha256='f63203574fba25c9bda5e98b2f87f985d4672109855633a46bae32bfba3cbc0d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.5-linux-i686.tar.gz'; 			sha256='c2b6f5763edd994cb01407b8e71797bd25901cc513132d155953742f54b3a294'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.5-linux-ppc64le.tar.gz'; 			sha256='11ae7f0b83663de35d9a30e916373378f7985424c030a4a5af96aecc9b6eaa66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761dcc62255b4eb1c7202d959c5ecc9077c0edf1773efbf8b7c7b654eb4d125`  
		Last Modified: Tue, 01 Jul 2025 02:14:06 GMT  
		Size: 2.4 MB (2427431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8ef7cc38b39484d6cca93ba606052a41fed6a22de2ca59d4395fcab55d3cc5`  
		Last Modified: Tue, 01 Jul 2025 05:12:59 GMT  
		Size: 288.4 MB (288411438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759af35bba91714905c02252df2abde8287869b58013e3619cc74a658917b4ea`  
		Last Modified: Tue, 01 Jul 2025 02:13:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:158361e33b6dba8d4bc251fca8481c20e1e964c8f1eafd434592fb69d58bd629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be92e06bdc885ce8930df87c32e4125717e6953e6337f3820239e7be3592ac8`

```dockerfile
```

-	Layers:
	-	`sha256:d77e10dcac7b8105d218b6054577d4b5c659a46dd021dfe805c5d81113b2add0`  
		Last Modified: Tue, 01 Jul 2025 05:02:43 GMT  
		Size: 2.8 MB (2828307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51b10279afab7d753a6a9f0fe1868927b378521e71fd4a1fd6b729444775f0c6`  
		Last Modified: Tue, 01 Jul 2025 05:02:44 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c122f29632d1ba68477fc8d127cd8c69580ac4261405ce63acaccf243db3cae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335155581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6bf7630084576f1667a83dc859b973add8e7659ba0bbd420bc88895864e970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 14 Apr 2025 23:59:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.5-linux-x86_64.tar.gz'; 			sha256='723e878c642220cc0251a0e13758c059a389cadc7f01376feaf1ea7388fe8f9c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.5-linux-aarch64.tar.gz'; 			sha256='f63203574fba25c9bda5e98b2f87f985d4672109855633a46bae32bfba3cbc0d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.5-linux-i686.tar.gz'; 			sha256='c2b6f5763edd994cb01407b8e71797bd25901cc513132d155953742f54b3a294'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.5-linux-ppc64le.tar.gz'; 			sha256='11ae7f0b83663de35d9a30e916373378f7985424c030a4a5af96aecc9b6eaa66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774daeb812e5fece3d60f17b2d0db8aef8f2a19eed94fbbca46c4e49239e2a5d`  
		Last Modified: Tue, 01 Jul 2025 03:02:09 GMT  
		Size: 2.4 MB (2417209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91effef3c80ab2227a8f5d63e9c1084fda519852473bc048752dae4327d7f2e4`  
		Last Modified: Tue, 01 Jul 2025 03:04:57 GMT  
		Size: 304.0 MB (303993866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a891e7f681346618bb36a8fc8661095a49350903d8009688bf2e300b90ebf`  
		Last Modified: Tue, 01 Jul 2025 03:05:04 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:69dab329219e167b2eb0ae633789879baa511d207f1bb49f21e3e31b307f4980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04087b65dad4708a9ac5276aff61dfefbb54ba9b4c90808342fae7d2388abb05`

```dockerfile
```

-	Layers:
	-	`sha256:d25c9211eb0925c8fc6df7609b7d08057e11f7abe314796ac954f86c4334430e`  
		Last Modified: Tue, 01 Jul 2025 05:02:48 GMT  
		Size: 2.8 MB (2828570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a9e65063686d474f0623a82b27d6880025c5d694f75beca43ab7ac8b1cae9dc`  
		Last Modified: Tue, 01 Jul 2025 05:02:48 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:59a44ae263dc2ad08e120d7c109ebfa71433707841ba7b2c1dd5658083819c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.0 MB (270985746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9719af8648416e878d3408a760297de3d040f8b31fa95c306bfb8974046ff2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 14 Apr 2025 23:59:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 14 Apr 2025 23:59:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 14 Apr 2025 23:59:20 GMT
ENV JULIA_VERSION=1.11.5
# Mon, 14 Apr 2025 23:59:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.5-linux-x86_64.tar.gz'; 			sha256='723e878c642220cc0251a0e13758c059a389cadc7f01376feaf1ea7388fe8f9c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.5-linux-aarch64.tar.gz'; 			sha256='f63203574fba25c9bda5e98b2f87f985d4672109855633a46bae32bfba3cbc0d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.5-linux-i686.tar.gz'; 			sha256='c2b6f5763edd994cb01407b8e71797bd25901cc513132d155953742f54b3a294'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.5-linux-ppc64le.tar.gz'; 			sha256='11ae7f0b83663de35d9a30e916373378f7985424c030a4a5af96aecc9b6eaa66'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Apr 2025 23:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 23:59:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:40be1da6146972d9df50a98eef7b5c0f729cd95a3a38782418f354f3b9355a9a`  
		Last Modified: Tue, 01 Jul 2025 01:14:57 GMT  
		Size: 31.2 MB (31189680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd588780160bb29a748d202fe96743145ffe8c8d8c463ceef7db9f24be3e8dd5`  
		Last Modified: Tue, 01 Jul 2025 02:13:14 GMT  
		Size: 2.5 MB (2534608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a986c0afdefe9e75e4879e4d66cca6f9f396513e5e3e9d2fdfd62a9f3b819fd`  
		Last Modified: Tue, 01 Jul 2025 02:13:10 GMT  
		Size: 237.3 MB (237261087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dcbc64b85a728c5f0d08596f74b62998f78ade64cf084bfd29e2d4e49fed3d`  
		Last Modified: Tue, 01 Jul 2025 02:13:14 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:21bca5edbe1d2963447fd0a25511160088234adf0a820949a934721ab00d21af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2842658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b0f744260e2e1f2a492e019a027f1bc7f3c30e31b0f00d2c172f9f6c18c0db`

```dockerfile
```

-	Layers:
	-	`sha256:9684328c215595801eeb1e7934a78fbdcdb4e223fed124f3e75d7a12c3a2234a`  
		Last Modified: Tue, 01 Jul 2025 05:02:53 GMT  
		Size: 2.8 MB (2825462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e2b563fa3bc028e379ba594886117b607c9630e8b910fd85c2e2de76168e55`  
		Last Modified: Tue, 01 Jul 2025 05:02:53 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json
