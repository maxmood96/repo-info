## `julia:bullseye`

```console
$ docker pull julia@sha256:80d8d5b54d9372a14030baf5416737035355c95f813daefcad0ecac8324df524
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
$ docker pull julia@sha256:89b0252e81fcee8a8295a302dfbd5333ebf5fc9b2bbcbf21dd0dd432df83bd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290953918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5e3b2a9d92441caccba1899fdfadb95145c7b3454af5d79cc49eef8a2b12dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1678fe3cd4a658f476437fee9e77b0c2086786926a90c07b083d0343a3675d34`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.4 MB (2426579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13bf3dac7e14a600162ea26186e3f4f9e2eb67b797a698ca137e9bda78be3095`  
		Last Modified: Thu, 17 Oct 2024 01:21:34 GMT  
		Size: 257.1 MB (257098167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24eeabef1fc4078b2230b57296e3885ca5a8abe902842a963d54dd9229da645`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:67cb263e6e9c5a8df2d07f56530084b32aa0fa18b9f54e1c70633d08ee81508f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e7a2b55d44957d73538f15728c85350a58a54b6670423e772b5052af5b609b`

```dockerfile
```

-	Layers:
	-	`sha256:e404b3ce366a6055b639f0e587f8f22d969c64c22ecac08b317416e03980c296`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 2.7 MB (2703232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cca66d1ab6aee6b83ad8e00220188da64a51b78924668d3a5d499b22c95b52`  
		Last Modified: Thu, 17 Oct 2024 01:21:31 GMT  
		Size: 17.1 KB (17061 bytes)  
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
$ docker pull julia@sha256:3670a732c97cffad25985d92fbb803b9b874eca1f6e26a4f56d8a77c91c1deea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269605951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb8f95ee66c50d9e825aedeb3254da01eaa7c893aec91624b016ac95a35fe7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD file:05098c6b0b4cfde8b4ffadc861fc7668bbf1779983d50b6be61989e6378fc17b in / 
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0aff79075c186716daeb376e46e89131aa14f0dc2bd8f794bd04d72494cb4693`  
		Last Modified: Thu, 17 Oct 2024 00:43:15 GMT  
		Size: 32.4 MB (32413830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b630321cf786277448e0f7aea94f99fc611feec697422839581d6ba78b0f4`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.5 MB (2533097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a25ec52f239ad17072bdbca92923baca090ca0beb325e15e8b38ec0d9a07bb6`  
		Last Modified: Thu, 17 Oct 2024 01:14:41 GMT  
		Size: 234.7 MB (234658656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacaf77ce79d2cad5f10ebb5c0a2cf0132caef0f18a13b0397f5419a1b104dae`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:801107f4fb9fa1d75ece047478ee52a0cde10e3e985cb4235e707647835d9385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a242ec47f9cd91c5c05a334d40ffb11921f23481e6fca0e70c18cee75e1be40`

```dockerfile
```

-	Layers:
	-	`sha256:2a3f27893e3c035da08f3858e8b8d9e3d748d8c2d2a8354fba0c038570df9fc1`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 2.7 MB (2700330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c148b1faeb4d330bc4cb1657a099ca6c996d5624aa2a62d3c3945b9e70e713`  
		Last Modified: Thu, 17 Oct 2024 01:14:36 GMT  
		Size: 17.0 KB (17031 bytes)  
		MIME: application/vnd.in-toto+json
