## `julia:bullseye`

```console
$ docker pull julia@sha256:3a26de0f543c8ca03efa6f71294dd581fad4539a2274c293c9827884e2499257
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
$ docker pull julia@sha256:cfe58f055a102dd1854fc7c502fa97050b0810aec6c1a41f4f1fc1b08e6eb14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321095191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531f530c8cca1506c35a3681b57b79a772a22649867a9d14f07bca0a84356679`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 14 Apr 2025 23:59:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a4fc36fce420b13f76023473585a828bbf86cbb3742c4379be589631f4fe8f`  
		Last Modified: Wed, 21 May 2025 23:13:13 GMT  
		Size: 2.4 MB (2427402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3c2cd2538d5d0d39944bda720eb1adb29624d4c23f03eeee69b0e6ae07439f`  
		Last Modified: Wed, 21 May 2025 23:13:18 GMT  
		Size: 288.4 MB (288411478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2b0ba2dfb7d681964f433733805752257404c0a0225fab29e2b9eec35a9f79`  
		Last Modified: Wed, 21 May 2025 23:13:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:a124a14506b53f6cc76fe95eae8bd751efecdc3f919b5b713e4f023b9d3cf2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86b9d84bb6d0064bc5d403ac35820157cfab406570c80ac0bc7c62b2a5d319e`

```dockerfile
```

-	Layers:
	-	`sha256:fbcc9ea2f41fee43047b44cdf2c100a16b5cf2fb7fdebcd45dc23c22288e9f70`  
		Last Modified: Wed, 21 May 2025 23:13:13 GMT  
		Size: 2.7 MB (2736364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0f0f6e6ec58446d2804fa608840c75e76337bf90631aedf274871a6c661534`  
		Last Modified: Wed, 21 May 2025 23:13:13 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:434f7508a312b48592c5bc2afa699c55f001cdcde8db92b7d69ed35301a2fff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335157415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6aa6946cd50a7d047d7bc691e123174110a2118b36af0815eb959c26ea077e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 14 Apr 2025 23:59:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932f1cadf49cac0791552ce7b80be7cf7d54ae754682a52d26b5e36dd891c9d4`  
		Last Modified: Thu, 22 May 2025 00:02:30 GMT  
		Size: 2.4 MB (2416935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d2241dccd385837dbd2713e2e910a32d39cc76260821cde17c9e7f4c6ac9bf`  
		Last Modified: Thu, 22 May 2025 00:05:32 GMT  
		Size: 304.0 MB (303993853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8051bd960fa3e6eca21bb7530e8beb09e98e91df2925c71ec32ad9c7afc17e5f`  
		Last Modified: Thu, 22 May 2025 00:05:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b58620d6b4088a59e2f63c6e84457e43f7cc8424ed3a6f6ce2891ce175a3d404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a811b02b98547a5403d084c49879e7c17c3cc65676276fd4734af14d68b0568`

```dockerfile
```

-	Layers:
	-	`sha256:69eb7024c830cc27a2bfc4f017c9e94f2234228495e1484bcdaf923e599276af`  
		Last Modified: Thu, 22 May 2025 00:05:25 GMT  
		Size: 2.7 MB (2736627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47b4d583f0d436ae705897528736bcf279efdfbe1a17605e7032db1ef08e950`  
		Last Modified: Thu, 22 May 2025 00:05:24 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:437d87ac3b8f567ba8e64239e97d6b326f24ff049cd7279d9e20548fe6c638d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.0 MB (270985215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d62a43dca6318bfdf9f40a113a5d70f9b78f5eee12c0c2e5503641b7192901e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 14 Apr 2025 23:59:20 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
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
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53badd8757502a1fcd57b4a91c2118daf8623f7b82ff9a46f69458ef53bf7330`  
		Last Modified: Wed, 21 May 2025 23:13:03 GMT  
		Size: 2.5 MB (2534583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209cbed0ff6b5ff23caf896dd42c2a3fa044ade85ec14ec28eab201956aeac58`  
		Last Modified: Wed, 21 May 2025 23:13:08 GMT  
		Size: 237.3 MB (237261064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeed6df5ce49504da1f4c6bbb52c0a962a8eb96346f22a864bab6bf2c87d2b7`  
		Last Modified: Wed, 21 May 2025 23:13:02 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:6d3663d6f2dd643c569f6deae2cde77bc406902e3dc2a85767b1c57dbdce26b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a8c82ec85e159e1815a13d37005e5515cb5cf0eeac8dbed97e4366ccaf8ba3`

```dockerfile
```

-	Layers:
	-	`sha256:83feae3fa6c46a013d90290aa3a13d41fadb6c4d0939cba1e73022d613450023`  
		Last Modified: Wed, 21 May 2025 23:13:03 GMT  
		Size: 2.7 MB (2733519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700d3462c967d74ab8bc54b2d93f37e814dd06a2d785991b311907459fdf3006`  
		Last Modified: Wed, 21 May 2025 23:13:02 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json
