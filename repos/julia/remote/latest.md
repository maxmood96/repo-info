## `julia:latest`

```console
$ docker pull julia@sha256:18b2684ec520b0ccc3d2ee2c80d4e939ad30f7a39e48e8db2826b032533af9d0
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
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:52d8799791db869ad50e6fb24010e4b9094cc5da25725ff059b1b61eec981dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206793966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bfc02cbe795dc58520e4f07d19aad666f92c87cc0828f5599c49120126ba29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 02 Mar 2024 06:59:15 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bac1f3687ac215b47633654fa379b15ae68afea476f5a0d99593d6a378bb59`  
		Last Modified: Wed, 24 Apr 2024 04:55:43 GMT  
		Size: 5.5 MB (5515204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ec65900c7c601feca3b398595cd313e43d7c2c3376dd5fbb90806112fa8d9`  
		Last Modified: Wed, 24 Apr 2024 04:55:46 GMT  
		Size: 172.1 MB (172127911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82682c8eb7416a26c05be33adc806a18f05ad5405817d638fe40702f63881dc6`  
		Last Modified: Wed, 24 Apr 2024 04:55:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:a3b0836ef59073b18bff9bcf509442b0325a57c568c40cf6113729fc8ca6fb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb29994cbe35a40db0c54df507abf1b914ea2824474c55d3926a8ec3bdb952b`

```dockerfile
```

-	Layers:
	-	`sha256:b5ed860bd9f59b270f0d6706fc1c12a61f4567e34424e996ba8da1fb621779dd`  
		Last Modified: Wed, 24 Apr 2024 04:55:43 GMT  
		Size: 2.4 MB (2415604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7eece614c1dd402e37a84fe96133bf48a222f4d5bcb3094416bfb2db0e8e64`  
		Last Modified: Wed, 24 Apr 2024 04:55:43 GMT  
		Size: 18.7 KB (18711 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:996adb35c57dd6ad4fe74cbaa39dfc8a31ec8bf3d864eede94434886af0be828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200423156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0843c0eede871905de07826ad819ddbf60540da764a1d92182792811891045`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 02 Mar 2024 06:59:15 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51eba2041d7f36f97184723e7f3ea3756749f4d0321ba12afb498a4c9eed6ae`  
		Last Modified: Thu, 25 Apr 2024 07:26:42 GMT  
		Size: 5.3 MB (5339347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23207d95a2c8f0f15bc5068cfdf69c7099b12e26703de7900861cd5d3873cb8`  
		Last Modified: Thu, 25 Apr 2024 07:29:10 GMT  
		Size: 165.9 MB (165903500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1eb5624f775dc7c67076b77bda82168c68e6d6f1c6a3e4c94aa3aa8cad5310`  
		Last Modified: Thu, 25 Apr 2024 07:29:06 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:a9f7f623049686cb09581c263fa7ba855c91ac50493f1b92a52ea33da96fa3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2433432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29e827cd7bddf9bcd0b5dac2200dc25622a3119ffc5c41d6a42088791f2952a`

```dockerfile
```

-	Layers:
	-	`sha256:d7257d61a808970b0abfdaaab8eb6ca9af4e41d7b86eea3bb480e88a46fba508`  
		Last Modified: Thu, 25 Apr 2024 07:29:07 GMT  
		Size: 2.4 MB (2414868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45efcf6cb52c142612ce638f44ceaba32f3d3354a7ac8feec1e1d38d29630d26`  
		Last Modified: Thu, 25 Apr 2024 07:29:06 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:5476636e75294916b25b75fd675035a2bfd388ff5a2e4ac0aea3dc1e8bf72f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193384435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac40f923c7d3afd0d1fbb2263cded1594e2ae7122f4ace345119468fbae4a40f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.3-linux-x86_64.tar.gz'; 			sha256='81b910c922fff0e27ae1f256f2cc803db81f3960215281eddd2d484721928c70'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.3-linux-aarch64.tar.gz'; 			sha256='2d52a61826872b3170c65f99a954bd9d21a31211cb50948056d924f811a0024f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.3-linux-i686.tar.gz'; 			sha256='f13be078c5ee7c98fd6a39a537199c253543acbd49bedc243f397cd51c7aeb58'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.3-linux-ppc64le.tar.gz'; 			sha256='61e4398df70129ce8184a2b84a12e9d862e92f35b526cd0297b5f2791ca628ba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.3?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9e7985e31c84168b2cec8017119c660d78fd0d42b78025948ed639e2bf18fc`  
		Last Modified: Tue, 30 Apr 2024 21:50:22 GMT  
		Size: 5.7 MB (5672204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174e253ee6538f73878873d8f06a6e95143c35213a3b726853a72713cb5d0ab8`  
		Last Modified: Tue, 30 Apr 2024 21:50:26 GMT  
		Size: 157.5 MB (157548675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e8b848aa14da172648437cc2faa79161598a58fdde2208b4d34fa52789ecd`  
		Last Modified: Tue, 30 Apr 2024 21:50:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:6348dbc6afc7254a2c7a2a280e29cfe056a6be2fe4c9e795d1653556ba7f3fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83432b8813cacc130134319c119514a7bdf9c8d62b4020953a30ffc3caf8ea5`

```dockerfile
```

-	Layers:
	-	`sha256:c8527551411a9e84a1f96001b2d7fd5d4176a36dc1e81168793e292932c4e59c`  
		Last Modified: Tue, 30 Apr 2024 21:50:22 GMT  
		Size: 2.4 MB (2412676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9c5b20b9ebf2553f1a3dcfde797d6021aca8b7d295801859a54c3b6ed67fca5`  
		Last Modified: Tue, 30 Apr 2024 21:50:22 GMT  
		Size: 19.3 KB (19309 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:42518fad4d8a20363e408d6bf3ce4259a1203bc1f3a1720ede05055daf233cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193349040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc361617127c03f5ef43a89da3fa93390c1213068a6e940b721330dc4e63a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-linux-x86_64.tar.gz'; 			sha256='a7298207f72f2b27b2ab1ce392a6ea37afbd1fbee0f1f8d190b054dcaba878fe'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-linux-aarch64.tar.gz'; 			sha256='048d96b4398efd524e94be3f49e8829cf6b30c8f3f4b46c75751a4679635e45b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-linux-i686.tar.gz'; 			sha256='413663f3d85dcf605236d048bd632a29dc31b451b9b04324daa82ba81c6c8c42'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-linux-ppc64le.tar.gz'; 			sha256='231135ada896ca93585a650c4f3498bb94e7c1cdc864457b2f7cf1b6a25af263'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Dec 2023 21:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Dec 2023 21:02:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e6dfe440366f653bf664315e491fe0cb2bb189428018fbcf657460fbbc3fa`  
		Last Modified: Tue, 13 Feb 2024 21:54:47 GMT  
		Size: 154.0 MB (153989961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6306b805ea4661e164d23cfd0d8dfae9d27c498477a790d3351d0f6ecc3e5fd`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:8ed461f46641215c54d31c67c06954851c85f63b1d2b4eebe9351ecff9289da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286b8e56e5b1f465b474b30b2fe8512b0c2238bef520a8bd95c4e5e31b59df2c`

```dockerfile
```

-	Layers:
	-	`sha256:9da0b3fffb06b598b8c17e331a4e70d4e6b54c5bfad5a40d4e88a16d3966ab41`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 2.1 MB (2142609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbfe360df232fd616240d3f8aae495b7a956d6a7383dcdf4dc8ae56cd7d319c2`  
		Last Modified: Tue, 13 Feb 2024 21:54:43 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2402; amd64

```console
$ docker pull julia@sha256:59930ae7595b5fdc16c9a293f0abc122d8fc364e7d8ce3e5c2a5f7e6756cc1b5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186661998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e44a2fb7920601877a5f2970aba1300712c4c313e9758624323a0d3ada1b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 30 Apr 2024 21:49:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Apr 2024 21:49:51 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 21:49:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Tue, 30 Apr 2024 21:49:52 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Tue, 30 Apr 2024 21:51:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 30 Apr 2024 21:51:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0162462ac8e21912c4dc6bc583bc0aa396ff310924c75020c1dd5d84b9444a`  
		Last Modified: Tue, 30 Apr 2024 21:51:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a01808be12ea6d8e666ac4e0ba27b4ed29bc28a6d6b79db67a1334deed40c4d`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727834c38ea41d07307df22346e629e1225460d20dc9c0644572832e69a5146b`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbea072db9d21283d89d47d81f570013db417eeb9bc2fb2b7c70b901b43eeb4a`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc8af169f1f4f0df080fe9e7c20110e16b37fc0e9e41064126570dd27140799`  
		Last Modified: Tue, 30 Apr 2024 21:51:55 GMT  
		Size: 187.3 MB (187281919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e494cdbacd2fb13126efb6e606c12c63a3c4c9995b6808dae3ecb156fc7715`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.5696; amd64

```console
$ docker pull julia@sha256:1fd5d053f986cc4e16156eae0bcc873db52486d330621c454076bda83b426743
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351712007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff815d1ebdd8b310ca35adac6da729cd9ed3fdd07216b6002724c818ab44bf51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 30 Apr 2024 21:49:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Apr 2024 21:49:53 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 21:49:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Tue, 30 Apr 2024 21:49:54 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Tue, 30 Apr 2024 21:53:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 30 Apr 2024 21:53:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7937ff6a70c7c1f270975873f4ffedbbf0f439123ad2798f0a541e5a9418916`  
		Last Modified: Tue, 30 Apr 2024 21:53:07 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849f8d4299df67a3ac9b7d00ee4f6677213eb5a2043d808a3d04cabb65936921`  
		Last Modified: Tue, 30 Apr 2024 21:53:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c305cac823cae094f060731eeb9516e95fc5085ce60320b5a028602968c14a91`  
		Last Modified: Tue, 30 Apr 2024 21:53:06 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48219fa751cb975067bfc46d789ae470beaf0dc93541b59bea6fd6a6031d27c`  
		Last Modified: Tue, 30 Apr 2024 21:53:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ca3c3645c1e6c43cc6cfa0c23df8956dbbae606775687bf89915ec7f3e273`  
		Last Modified: Tue, 30 Apr 2024 21:53:28 GMT  
		Size: 187.3 MB (187277506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74546cae5aa02d84606fc9021bdd9095dfc4b88f6b4a4dd1bcecafc8b4b39f9e`  
		Last Modified: Tue, 30 Apr 2024 21:53:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
