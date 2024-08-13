## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:564a08bde3a95df0649fbeaeecbf18447d07d6a0b1761802800b8cd756ce4d1a
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

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:5034077c3d36f730452e2960746e891a3ac464861b3e290fc7b4787208b35e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286966744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb7fa0c35d09a16255011104dfe22d542b6c92c32e8864357432eeadddb5946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Jul 2024 17:59:17 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38f84472323b2419694b5c13595bce6f0f13d14a095a82707ccb4ce4e0b8ab9`  
		Last Modified: Tue, 13 Aug 2024 01:19:31 GMT  
		Size: 2.4 MB (2426491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fe87473b3e8ed80c53ab0663e5a02e586d2c2fa850718f1382c511bcd547ac`  
		Last Modified: Tue, 13 Aug 2024 01:19:35 GMT  
		Size: 253.1 MB (253111595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc2d764a2d1fec25e41a83a1a41be5ec1f32c755dbbe6b2a7e8ed1f6d06f1dd`  
		Last Modified: Tue, 13 Aug 2024 01:19:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4ee19a7f729a110f968bc95c01340fb479f4f1afe0519ca5bb2fa2d9c677948e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376a988415e99c439ab2e11a84d9e106a5a7d2c8cf0d9db8f2156d76b60b23b8`

```dockerfile
```

-	Layers:
	-	`sha256:83f2ff7d6ffd9a87db1ba00e255d665c33890ee694bbffa69ada626be52983e2`  
		Last Modified: Tue, 13 Aug 2024 01:19:32 GMT  
		Size: 2.7 MB (2702845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b8538c55e6a525b862b8e8c245dd9bf0a73a856dbb1eff7a5f8b1a1d9f2d6f`  
		Last Modified: Tue, 13 Aug 2024 01:19:31 GMT  
		Size: 16.8 KB (16801 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:044fa8e3f6bc2d0a57349c12580b8fe73d36c9e20dcd43e634e46e92c53d06f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282533456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768eec80d9622999ff5ffc17041a6d5d7133295dcfb2f7174bf665563249397a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Jul 2024 17:59:17 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543b5afde6a56d8ee552ec3409306e3a0444e5688fe8cf378fcac907793b6c94`  
		Last Modified: Tue, 13 Aug 2024 07:26:51 GMT  
		Size: 2.4 MB (2415050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0f500c61af7f665d26a80c3bb4bdd16d550f99ea5bd57159577d67dda52b34`  
		Last Modified: Tue, 13 Aug 2024 07:26:55 GMT  
		Size: 250.0 MB (250041952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e1e811e58d4d9b500f9cd7e724b828da401ef0d9124c9e81fb7dccbaafdad1`  
		Last Modified: Tue, 13 Aug 2024 07:26:50 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:759ec27112537825455d038369a20660d37b7df5e68978d39a8fbb3cda736fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7275422949509daca3b5ba386d903cab9627382e0077e343d225fe6dadd23be5`

```dockerfile
```

-	Layers:
	-	`sha256:f3a9c77d0b281609df344404fabf92f5cef70eb5d8b347f1a0b5137c32cbea7d`  
		Last Modified: Tue, 13 Aug 2024 07:26:51 GMT  
		Size: 2.7 MB (2703095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee5af01b2c1c6504211b503fe567920f886e3038fa255297bac86eb6d95cdd7`  
		Last Modified: Tue, 13 Aug 2024 07:26:50 GMT  
		Size: 17.1 KB (17098 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:9de9cc48ea241fd783f70e530f85df508814e6b130353039c7627013fae90315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265841046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d82bea3e1925795a5749d639770bb43711ab9dfd7164818e96537251f470ddb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Jul 2024 17:59:17 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa7e5b7d09462d5afbba2b9f501d52b4bf83f9310c74b72dc499391b3d3abc7`  
		Last Modified: Tue, 13 Aug 2024 01:19:21 GMT  
		Size: 2.5 MB (2533012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86ed9ce4638bb13dfc6bea09241dfa52cde942d451a6c2ea03cfde50ed16404`  
		Last Modified: Tue, 13 Aug 2024 01:19:26 GMT  
		Size: 230.9 MB (230893880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e041f2fc22c2b0c719ba38fadca51a122c874afd59cfa5e51816940a27f3a07`  
		Last Modified: Tue, 13 Aug 2024 01:19:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:725d58aa2d29ca9cc6f5320f170c3ece7b6e7fab274d36a2589e0bebda7ba9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abcb87423d6af1350696965e01707985a3a911da6f7ce75dff9c5a2b215808c`

```dockerfile
```

-	Layers:
	-	`sha256:01fa53d39e7bc23fa916ae42bf992a8ee39b5fc30b9d2d094251c9815bf0bef5`  
		Last Modified: Tue, 13 Aug 2024 01:19:21 GMT  
		Size: 2.7 MB (2699948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce4722eb737d185044cf53b847165748e1332c51cad94a54172237f60e07399`  
		Last Modified: Tue, 13 Aug 2024 01:19:21 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:d6aa1dcb83dc673c21c661281df3755e8abca38937459891f149b4bc075e3573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278932568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6304cc1a4991ddbcf6ffa745c296d1f60c80ea811f526ae4716b9654ae3e787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Jul 2024 17:59:17 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Jul 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Jul 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc2
# Mon, 29 Jul 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc2-linux-x86_64.tar.gz'; 			sha256='7416f969669761e3507ebb7b505075ca234a1785b438304c2b016f5ee00058ea'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc2-linux-aarch64.tar.gz'; 			sha256='947f48e9bf65217782b33be4ce0a9e4c07b5101121871da954c230bb63db9ab0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc2-linux-i686.tar.gz'; 			sha256='611428bdc5bef1e96f6a86ee5064ef0e22e3612891b8a27e7a129742dad4fe97'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc2-linux-ppc64le.tar.gz'; 			sha256='3ccbc68c091e6f52a490aeaac46ec24d528e1a41f4b817b7c715111dff169bbe'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427a257c7b9086c831b18098d98940024fc9b4238af8b26e852099e510cad1b`  
		Last Modified: Tue, 13 Aug 2024 06:54:17 GMT  
		Size: 2.6 MB (2629937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f4c594a807b248f628dfb521028f2d887c8128d77c866c3f7011800c4af99`  
		Last Modified: Tue, 13 Aug 2024 06:54:23 GMT  
		Size: 241.0 MB (240997131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aa63279d77999e6f8b82d1d80accc9f777b97316d30a82ac3586b92017bd5b`  
		Last Modified: Tue, 13 Aug 2024 06:54:17 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:adc02e8c3c4339165b1c7c0a9c5873dc38cfc0ef402dc30a69667da3fa4c3e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2724069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e667d6e904633acbace5ac2b0f835174965471d2026cfcbd0133f6af4c269443`

```dockerfile
```

-	Layers:
	-	`sha256:f7e2928b874fcfc6adac0fd2fa8e5b959bc7423aaaeedba4f1e7d532d94b687d`  
		Last Modified: Tue, 13 Aug 2024 06:54:17 GMT  
		Size: 2.7 MB (2707234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c3910e9d816a97fe18ed6fd977f98be03a37eff69e8ebe11294c90468823a8f`  
		Last Modified: Tue, 13 Aug 2024 06:54:17 GMT  
		Size: 16.8 KB (16835 bytes)  
		MIME: application/vnd.in-toto+json
