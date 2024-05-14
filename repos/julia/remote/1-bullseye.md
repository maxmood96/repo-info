## `julia:1-bullseye`

```console
$ docker pull julia@sha256:fbe29f0e492a961deccbf5775cdf3cea099b06f1058dcd7534a6b57f15335505
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

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:eeadfb556a36126bd617d301009746af09a64df721f6da5cbadfe433a8d6b25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209672021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027f980876be6da628bd3ce4a7a115045b0e3bb8962eb1d34f8f796156c7611d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 30 Apr 2024 17:59:16 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 30 Apr 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.3?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847230c47c0b1cfdc2ecc5fb79ae8c6a6ec0e7b09b92e8976da26b16d99e989e`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 2.2 MB (2223174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40a6006985f6cba8706adc4cb1a18b2b5d142f0162c6a0523653fab07326e5d`  
		Last Modified: Tue, 14 May 2024 02:56:34 GMT  
		Size: 176.0 MB (176014544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7900d8665cc36f33f1116f93a83aae31c279d751424304a476d73ea253207d99`  
		Last Modified: Tue, 14 May 2024 02:56:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f4db399074e53bde3e98fd843069ec196f8193a47233f40286b1f13915e8f7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2609036ba575e4ed02d4b44bb558d38adfea0d49179c886fb14c943727bc55`

```dockerfile
```

-	Layers:
	-	`sha256:1c6294c4d76eba2a525675875983bf2c85cf1ca2e0ee1c4ef2b01ad73e3bbe0d`  
		Last Modified: Tue, 14 May 2024 02:56:32 GMT  
		Size: 2.7 MB (2682400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91425709012dea760dcbe8d137d8ca28386612ee020cfa82217375fc0e901e49`  
		Last Modified: Tue, 14 May 2024 02:56:32 GMT  
		Size: 18.2 KB (18190 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:340b773831767c1c02ae3024875afdfaccb7e2091119b0971039b0675e688148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210461735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04061531c2d20967e613c62d338b3d9fd1d3fe0b9cd818c3e9d6be0255ff0ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 30 Apr 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.3?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca3bdae07badd4448d5c3470672c85e6b07f52b75603aee1a77172e5e335b7`  
		Last Modified: Tue, 30 Apr 2024 23:16:47 GMT  
		Size: 2.2 MB (2210795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638125e7d3db2aa5fb7ca904233d9931fa7dea21256bced4b0ea13c6043882f2`  
		Last Modified: Tue, 30 Apr 2024 23:16:51 GMT  
		Size: 178.2 MB (178163229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a46fc052a685e5a704bb54433bbe3212f33b56a74d3d7aa667589d04c2ca1d`  
		Last Modified: Tue, 30 Apr 2024 23:16:46 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:7fa66738da6986e84f05a04df0da15bd74ce26770cbb4b4c973956c01ab56790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907179a37e4819bfb0dc6c21d06c98740c8d5fac3d621d3386b35e7edbd31b83`

```dockerfile
```

-	Layers:
	-	`sha256:542e7ffad2e5f6a94b96fd9b1bef2d910eb0f4a1996282e06ec21d1169b5ef60`  
		Last Modified: Tue, 30 Apr 2024 23:16:47 GMT  
		Size: 2.7 MB (2681638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9ab7e187f55ecf49483f3b16d9bc48f5861348aca856a564efb5b4ab1e7e753`  
		Last Modified: Tue, 30 Apr 2024 23:16:47 GMT  
		Size: 18.0 KB (18033 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:c0ed4ac15abcb2be87103c76f6fcb180c9911b88a71ed24834b7bde1e68812c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192302679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6d32873810221f5886e3d3c8f2ed9d2034a696e2c84c65d626edfe262cce46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 30 Apr 2024 17:59:16 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 30 Apr 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.3?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b75a230e2c5a8a7688bfb2eecf66029661f30dbfe64822a44bce6ddd6949d25`  
		Last Modified: Tue, 14 May 2024 01:54:03 GMT  
		Size: 2.3 MB (2328980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad829017effb1de244fd203eea4d0039d495668efd61f3d14a35ec2e61598c52`  
		Last Modified: Tue, 14 May 2024 01:54:07 GMT  
		Size: 157.5 MB (157549289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405093eba21d0109502f8d4a758cb82b0efc1f53671a33230941877149ffd2ec`  
		Last Modified: Tue, 14 May 2024 01:54:03 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:22a0c283135867a43fc18d73872fb1be9fa4b2bae979113af210e7b66db8949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfe77685e1e38ad1d66474dc6451018df0bef0967c64271187cc2f11d75539c`

```dockerfile
```

-	Layers:
	-	`sha256:ceec3a6e108e75a5432377517d7a7708c1bb2c454daf429fa855af919163af74`  
		Last Modified: Tue, 14 May 2024 01:54:03 GMT  
		Size: 2.7 MB (2679498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256098147dfd79d1812bb1dc61be3943ac41382b2ab9e51c4b6247e58794f54c`  
		Last Modified: Tue, 14 May 2024 01:54:03 GMT  
		Size: 18.2 KB (18159 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:09bfae000ee6d9e64a4ae8040390cb238c68b5bffe9c4445bd2eb1ba4d9dd442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192417168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14790d503938f7e0655045a4205652b0b8111412c4d03084b8e47e0ead624f92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 30 Apr 2024 17:59:16 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 30 Apr 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 30 Apr 2024 17:59:16 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.3?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b34723e47ba2ee8e054a2104e7b86857769fefadca33b43ee36fcf92e586140`  
		Last Modified: Tue, 14 May 2024 13:26:18 GMT  
		Size: 2.4 MB (2425682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8957e47c62c12f85a946c00c3252e009f7c0b550486a5ccc42dbf34dbaa2bbfb`  
		Last Modified: Tue, 14 May 2024 13:29:35 GMT  
		Size: 154.7 MB (154679954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c80f56888c30d44344ddf2b992e8c0f0d45fc201a493454a7507e9b704b5992`  
		Last Modified: Tue, 14 May 2024 13:29:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:3e3674b908b15af6827f73657e2ea723282abddb1e366cae2953278c6d16eb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a3e1fe3af5d74113a3938d707f01fe01374a2df4c31ab36c78c64fe1fb3383`

```dockerfile
```

-	Layers:
	-	`sha256:d70161c7b277efe7c99e7a03b479a430ee2c2649b749d89091e0e1bb4a669644`  
		Last Modified: Tue, 14 May 2024 13:29:29 GMT  
		Size: 2.7 MB (2685822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4fdb79160efeb88731717ebe90d03502a384df79de1ef00bf1239cb389f14e`  
		Last Modified: Tue, 14 May 2024 13:29:29 GMT  
		Size: 18.1 KB (18062 bytes)  
		MIME: application/vnd.in-toto+json
