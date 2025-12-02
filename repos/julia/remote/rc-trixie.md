## `julia:rc-trixie`

```console
$ docker pull julia@sha256:0dcaeede6fda092821d12b1a1685b75667cfeadbbc0e19bad4ae202563da4bac
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
$ docker pull julia@sha256:368d23427a70543f06d175be51bedd60ddcb712bb9eff268d85d488efca8870c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321709134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd50718b5e180978482f71825be85e9932df6a2fbb7be5ee6fdbc20b71b87cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 28 Sep 2025 11:59:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Fri, 28 Nov 2025 23:54:57 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196a13415fde7b596295337b8bb3f46b6d79cf10335533f9ce63c6c0212d8ccf`  
		Last Modified: Mon, 29 Sep 2025 23:51:21 GMT  
		Size: 6.2 MB (6242752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dcb501c175c87589004dc25443bb643721569b6b39a24fa2bd599b40f9ba41`  
		Last Modified: Mon, 29 Sep 2025 23:51:39 GMT  
		Size: 285.7 MB (285688249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41ac1bbec77f8ad85a90cd0295db020a1d16e6aa104469132a67f37075ee40f`  
		Last Modified: Mon, 29 Sep 2025 23:51:20 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7e0f42fb4b49a64a32654ef9c13426e88a9640c09324973fc6175b8fbd849ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1504b3d28ea0ceceb11e3595a0cf7861f257e3e81e950532ed46b6ee5198b842`

```dockerfile
```

-	Layers:
	-	`sha256:ac1d7c73120365fea8ff58ac46ef6ec62686b82e341ca8f8b602af1fd0f740b2`  
		Last Modified: Mon, 29 Sep 2025 23:51:20 GMT  
		Size: 2.2 MB (2239479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c3162e7e998ae8fdd0b5aedc550c442ee681d3afd5861b008f2018293188f7`  
		Last Modified: Mon, 29 Sep 2025 23:51:20 GMT  
		Size: 17.2 KB (17219 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:74edb39b7fb0b93532ec85e03abe03c97f36f9b7fb3db2d5fc5a7e1b142b026b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341871300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a717300aa3aa317182dc8358ded665509eed2f558713ecd128f3375f17c29618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 28 Sep 2025 11:59:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Fri, 28 Nov 2025 23:55:28 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27280897a412405206c664e08a2fbc1ab97313bdbecf943cffbc472d6a57bd7e`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 6.2 MB (6153042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbdde2811c897d605ccbf467066f3b136e78e7a4d736a4fe3641b7e57e6c64e`  
		Last Modified: Mon, 29 Sep 2025 23:55:20 GMT  
		Size: 305.6 MB (305577046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ead3f60d83349d2084956a2793406f402f18fc5c2e8f677409d36c60c81bfc`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f9f8e3710f942eaf68b1f652b6737b8a7b8e1e78940f87fca59ecc9300e7a955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7514a4a0065ce43301cc564703da671cffa0075e9acd221e4282bfafcd9adf9`

```dockerfile
```

-	Layers:
	-	`sha256:da11521b1863ab3890c87e45a266fc611dad37905bf8f304e4e5222bd89ff41e`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 2.2 MB (2239787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70cee7031e4876dd9506112c9b497951eecc5bcb60f9d7d8b3b5d976bd3c5d91`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:d43e5c3c97540a33f9580e4af0d01137af3e829a09652093069e7e1276b54fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267485550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3345b4b8c7ea50278cf63b08b028dd0c70eab07bbabb93005a97c81d4b5357`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 28 Sep 2025 11:59:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Sat, 29 Nov 2025 00:13:08 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aeccacc651e9f09841f3b1df282d843852874a7973d4f0a239cde04bcb11d`  
		Last Modified: Mon, 29 Sep 2025 23:55:13 GMT  
		Size: 6.4 MB (6427717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9363f2169793329ecad4b11384f01d88aecc3994144799e2c60ef47f6b118646`  
		Last Modified: Mon, 29 Sep 2025 23:55:18 GMT  
		Size: 229.8 MB (229762927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c39ed66ba25ac36c359ca94496a419cc16e1b074edf5590b17c200398c94df`  
		Last Modified: Mon, 29 Sep 2025 23:55:13 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:d55acecc8c01c6b4cb30edeba59794e8804cefd958dd4a33345c16a57f33b132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18ef68bf4a1098811d018eb05d4fa62658da0e791fae6afe7e6220464cbb3c3`

```dockerfile
```

-	Layers:
	-	`sha256:16ed06a1d8b5f9bbabca297d1462a0c17797b79ba4aeafafb4ad5aa772d2c558`  
		Last Modified: Mon, 29 Sep 2025 23:55:13 GMT  
		Size: 2.2 MB (2236614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1daed00c7e63d8bac4763574ac7882bc304d5202081857044d15062605cac8b`  
		Last Modified: Mon, 29 Sep 2025 23:55:13 GMT  
		Size: 17.2 KB (17175 bytes)  
		MIME: application/vnd.in-toto+json
