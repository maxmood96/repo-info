## `julia:bullseye`

```console
$ docker pull julia@sha256:23e43fec74df722c24ccbb796844c4080e27a27a64e0d7a23cbdc0ce3812382a
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

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:1216761bde9883d3576eefdbb0bd518e8d60e5d5747d1fcf01ed40ebe42f03d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205785424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d114dab8a9673e51130d7c9e9525fc38d158581fc91ada749a01e3e8bc8f2b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 02 Mar 2024 06:59:15 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521502b675f5d3552b5700ab4583cb0153ea15aaeb0f9c1fba9d62be3f59355a`  
		Last Modified: Wed, 24 Apr 2024 04:55:42 GMT  
		Size: 2.2 MB (2223226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a405af76ea0c8a18868d738ae2ec3b67d7a417dcbdb045082e3f2071badcebc8`  
		Last Modified: Wed, 24 Apr 2024 04:55:45 GMT  
		Size: 172.1 MB (172127566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1815aee35eabb80c2fd58bdcff8745b11a46dbbd201907c0efb0ac2cd6f257`  
		Last Modified: Wed, 24 Apr 2024 04:55:42 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:a7784ca4c7b973aa0e7d8d32a4aa69ddc2d6bb30f526bb4cd59d62223a4ee3a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd70e3a42566b03aa94cb6be42bf23b4b1898f7c9bc07ebfb384bd53192181f`

```dockerfile
```

-	Layers:
	-	`sha256:bb1e73658148c967b229bd0c6e3e08cfbda6a5bb589269d253ba428192a5249f`  
		Last Modified: Wed, 24 Apr 2024 04:55:42 GMT  
		Size: 2.7 MB (2682394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0c3a0adbd6df5847d8e589fc863bdff510d73908c6c412b7724bf5d68fd58e`  
		Last Modified: Wed, 24 Apr 2024 04:55:42 GMT  
		Size: 17.5 KB (17544 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e8e6da0e22e40a3745de2afbb15c3f8a52ad2a4ef7ab46d399664242e40d9870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198203116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842faff1f4cd509498f788cd2ea8c8d863affab94bb807f3de990c35ad76eaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 02 Mar 2024 06:59:15 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a0123b28bc4d8161746e71679f02b0a7f785ddbbfa9c26c2657834de1725f7`  
		Last Modified: Thu, 25 Apr 2024 07:28:02 GMT  
		Size: 2.2 MB (2210858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeb22b59af94c8bf7624336ee0f62826b1c35a7d6f98a3be900c44a73382176`  
		Last Modified: Thu, 25 Apr 2024 07:30:12 GMT  
		Size: 165.9 MB (165904549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4f72cf80b49350a4742c8fbf66680b5397ff22b5e548daaf5257cc542a9ee6`  
		Last Modified: Thu, 25 Apr 2024 07:30:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:7c906c7027f981ff04463d51a8c174925e25e6af8e6590917b7ba2bfc2066624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d9f54dc1d685cc143ebfd9566fb049d85067f1e76f6ec5b5f9192590e1a6f`

```dockerfile
```

-	Layers:
	-	`sha256:b017bbdedf23d32607afbce6dc8e9e76bfe6e9495b4313772b7539fc3c9aec7e`  
		Last Modified: Thu, 25 Apr 2024 07:30:08 GMT  
		Size: 2.7 MB (2681638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cac858b252fd780fc4cb76624b9cf2af810855278ac197254adcd1db200f0e`  
		Last Modified: Thu, 25 Apr 2024 07:30:07 GMT  
		Size: 17.4 KB (17387 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:1f199196c804cb961d75cd6fdc357acd1ed5775fb73a388e17cd81f5a8e3a2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192303342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2200284bafa14e14058628a9a665f13030dd1d3ab12923c011760f4517cafb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
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
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacdab45319bb454ea81b205df119732e9ef7229213cbe86751c666808385b8e`  
		Last Modified: Tue, 30 Apr 2024 21:50:26 GMT  
		Size: 2.3 MB (2328973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5e16e903a4d013922806fe1ace5af4a93b76e3dde304f14594c7b47e02e8d6`  
		Last Modified: Tue, 30 Apr 2024 21:50:30 GMT  
		Size: 157.5 MB (157549226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d4dcbaaa74a857e0ca37d8dd77774ed3b6df9d58520a20897bb43dcede4171`  
		Last Modified: Tue, 30 Apr 2024 21:50:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:3e7e020eac056d8dc3cd361b57baec309f64aab2edb464e13b8d0845655eda32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2449638b738c0eb1ac62b4d502d2d9c91b0937e84d16b8436411ab0397394c`

```dockerfile
```

-	Layers:
	-	`sha256:3495afe3fd6232f645aaeb18a77d269977f84d076f3d6af683e044d739311be8`  
		Last Modified: Tue, 30 Apr 2024 21:50:26 GMT  
		Size: 2.7 MB (2679492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459839462bc89fdf8de2841f873714be0a70e0ae5805e8ef82b1eb4d7ee160fc`  
		Last Modified: Tue, 30 Apr 2024 21:50:26 GMT  
		Size: 18.2 KB (18159 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:34e38bddb83d3e554661ccd943af43cdb864af337b665e80d319d17641dcae38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191918984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2e008edde3927a13f00754ee8f8a138c1cccfbf871fbecc2c26aa365977fee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["bash"]
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Dec 2023 21:02:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Dec 2023 21:02:39 GMT
ENV JULIA_VERSION=1.10.0
# Wed, 27 Dec 2023 21:02:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc406362a4b5aed4760caff7c4bc06a04cb2bd3834a923f056a5baf70eb0d7ff`  
		Last Modified: Tue, 13 Feb 2024 21:56:31 GMT  
		Size: 2.6 MB (2629991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278b4e0551a3587b5d022b566e56d527b968803375aa151bdd2dc6d30b7c7813`  
		Last Modified: Tue, 13 Feb 2024 21:56:34 GMT  
		Size: 154.0 MB (153990822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a158664e796ca3ee0566bb6b7e2b79e13c3161c9f36f6dadb04bf7cdcbb6e58`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:074faa55f685aff95e390f40bbece0962016efb2de45e76932ad7ec77379eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae430aa8a2857fe05d29dfd22203f96e4ba41334491bf64c9bcf168e2689ce`

```dockerfile
```

-	Layers:
	-	`sha256:a3834b7b363b094f8ccc42c1d8c1266c29a4d88ab2002bc4a6d745aef0871e7b`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 2.4 MB (2363081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd53c802c699b2d4eec0a68f896ffad71210add2b28509849ee2d177075647`  
		Last Modified: Tue, 13 Feb 2024 21:56:30 GMT  
		Size: 18.1 KB (18059 bytes)  
		MIME: application/vnd.in-toto+json
