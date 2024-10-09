## `julia:bullseye`

```console
$ docker pull julia@sha256:0ead6a1b95a86885b371febe6eaa67bf599880e2b2cd3de34a9505813573af2b
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
$ docker pull julia@sha256:3189c0222570ec54eb4b841eae57a8608fd4f9ec9edd9a14540b9260c3d869fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6adb1c4e29da9b0db77b49b12f3cdb86f4f558956365c7771e2a14b295f6586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc211be43b941cc7bed9c1efe4f919b0601f547a5fbc6f0bbe1b8930e3b3334`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.4 MB (2426612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e659bb993041a09a231b20ad74957f1dde65addfb857777ed82f84c9a1aa99`  
		Last Modified: Wed, 09 Oct 2024 00:03:03 GMT  
		Size: 256.7 MB (256678724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c341be1dadb8314f2ddf31ee83f2f36b8aa832c9c7b2a11fe3b318cc28923`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:407e6865ec77aca6a2bb36eade6869492617a14c97461edbf242afd4194875e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf33dc5e61d7a2e38b5e593bc6c8a4d730fc4afcb3d523fda249792389b253c`

```dockerfile
```

-	Layers:
	-	`sha256:b00a888b1404f60813abf79309d0552a2a223ce66b295536956ef4a21a9c99c3`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.7 MB (2703142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bb48a49b1dce446afd847293b802c912383b7812811d80f1b3e222e4313b7b`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 17.0 KB (17029 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6e86a4843cca3beda39d329bceeca3b5a3f6c09e5a504828c325910aee5405b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285978592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f01c62f4afb077d528b72f5d1d2c0cdce1d15d33801743e7a5e7e62b0365e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a4c652dcb6e4589d9a0cc32c529a61a75e3f76b625e79053438c20d0f5d31`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.4 MB (2415138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edec0316fb8e0d5486508662dc676444bc4c8fdbc3f497dc4808fa9aa532e2e5`  
		Last Modified: Wed, 09 Oct 2024 00:12:36 GMT  
		Size: 253.5 MB (253487922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139c1c9276db7fa9a352b42b7e7a31b711f27329b6345cfd6ad74d105ffa769`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:75e0c340627d366e6e5d1b9007eb26a19d0b4ab609f921e75fd87f5395add5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd034322e6a91416242cbcc74a1c3cd03f9dc8325878df0abcef1846fd37003`

```dockerfile
```

-	Layers:
	-	`sha256:76e7c1b9e2823e50b79fe6130a733e6d9ff612cbd555a988cca8f5ac2d6d8c0c`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.7 MB (2703404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca20bf39129cc8626302ab268628257409909617223ad1a750d02864b0969af7`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 17.1 KB (17141 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:0be92a1464ae33a39b49ad6b69480f175f53ae755cd895b7e22785b18a632a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269413890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd33baadc292686a52f75034d4e79563db36fb012b51c2b454b593e49899689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c033560c807a67a65f22752c592cf61e48562e82d93642b101c86db6d67871`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.5 MB (2533016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a852befa831645253114ea7ea017a3f866d8cdae0f620077cf54c8e3b95819b`  
		Last Modified: Wed, 09 Oct 2024 00:02:57 GMT  
		Size: 234.5 MB (234467000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779f8328d72cd1cef3fe44a19e3033fbd3cc72502986798dabda96cc9a126`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1f754a87e8efc2c9e954363d3bdc622afa0149a1d3c3b5bbfbc297d39334c504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1dc590891a313455cf48d8bcb99d1adae6b3929815eb94acb4f373e3b2210f`

```dockerfile
```

-	Layers:
	-	`sha256:50a9335a97f4f82d99f4890789ee44b8848bfe0f1839001c62935973b7f14532`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.7 MB (2700240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10ac5795d098541e486a8c4c1d254f83cccbbc32b4df6dcbc14b1c599c55446`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json
