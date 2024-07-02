## `julia:bullseye`

```console
$ docker pull julia@sha256:3817a1af8ace163b44aa85a8efb5c2fef91d234e565f7b456a70f0de8a1974df
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
$ docker pull julia@sha256:134c640e94749fddb62d336984586048dba5c4beea2809b13015853b1f3c5b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.1 MB (210071731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cf941a76eea2cc076676e7204db72c00f07ba32b11d2bc9b294c17212dea95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aadb389c2f3f2702468486bdd7483b576e8cc4fae1b80c34215b2f9ab91b4f`  
		Last Modified: Tue, 02 Jul 2024 03:04:00 GMT  
		Size: 2.4 MB (2426488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7c38540a36de31a54cec9348d200b23a2014d0141e66609ede43aa25f72d75`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 176.2 MB (176222586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d93f1b780241dee98afd123f7a00e74c121331efc36170362f142cb5a0b4a3`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:af6b8d0a1c6e08bd8159bb08097f64c30f75723e875614934a24f5bad5ac7a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a823c9db6d4fce52ada82207d65c4353acb91edaf95890f903dca7c09a7cb39c`

```dockerfile
```

-	Layers:
	-	`sha256:9ca1cbe9c641c4939c44dcc898e9a5e239d455bd7499de03e8896f09fa858559`  
		Last Modified: Tue, 02 Jul 2024 03:04:00 GMT  
		Size: 2.7 MB (2681423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2489e0e22bfb932ebe33c5f713e5f18210c17ead3c2c2279e5007abba35801b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 17.0 KB (17023 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:0fa1587f1514efa60df23dce366d2a25bc1e0564cbae77c9cd254038ac63c6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210598961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a9fe2694037256b1a8f795edc687bb9149ca31cb00a73dc15bd41a3d7c6043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9afea3b5dcd6ad873b75be34809049755bf189c270ab1e5bc0e35d4458518`  
		Last Modified: Thu, 13 Jun 2024 19:21:27 GMT  
		Size: 2.2 MB (2210839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd84ff59f7540299fe41695869e27e42b386e145ff9ae49aa6d5be597b7c6c0b`  
		Last Modified: Thu, 13 Jun 2024 19:23:41 GMT  
		Size: 178.3 MB (178300776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf78b2ced919392195d870c35bc5f3f1fed591935265cb95b1ca7e2d5259f4e`  
		Last Modified: Thu, 13 Jun 2024 19:23:37 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4dedd5ff081fb56810a5deb8b86b7ae77c190780098e88129f855401087dd813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bbe3fb75cb940527e1fb0c001568a1040dbe6863cd5c5e3c54028b77dd91ef`

```dockerfile
```

-	Layers:
	-	`sha256:3187929cfac1d60d54f5ae8f0a8b16e184c85f48f8481e87b6285d4f2e1403ca`  
		Last Modified: Thu, 13 Jun 2024 19:23:37 GMT  
		Size: 2.7 MB (2680673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b6d37414e50f55b4c67b7bd4d5440635cebdf52654dd68c013348fb296681b0`  
		Last Modified: Thu, 13 Jun 2024 19:23:36 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:1928261d5b8a12960a6fe1cb067d7f068af66254db3a920cd5f7e93b477cf877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192511712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76e4c1db3512d1b29411ece563182c2e09f527b4ebd4574ddb88915d9493749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5411a2f7675e74f0952f295a54c37cbe30681551723a18c9bd363fb2371037df`  
		Last Modified: Tue, 02 Jul 2024 03:03:57 GMT  
		Size: 2.5 MB (2533023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95cd0fc5e0b4f492e06db2f0ca75497c0e873af1e2d0d68c4c834693bca6c1`  
		Last Modified: Tue, 02 Jul 2024 03:04:00 GMT  
		Size: 157.6 MB (157569867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68cf7d03a61245dc5bfc4fa0c3dbc134434c3e5d9c45f1a2c309c383926a44e`  
		Last Modified: Tue, 02 Jul 2024 03:03:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d443b21740ec7b270292b94df5ca93a5b11983f7b0daf90d00c685a00ad24f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bddc43875234dd25c95cc11b3a7deea0102381fe4ecf02d1df862a566dd241c`

```dockerfile
```

-	Layers:
	-	`sha256:348f7419cca174e39ca40638102e747de07db40f5a3654b73cf297e27fe77d1a`  
		Last Modified: Tue, 02 Jul 2024 03:03:57 GMT  
		Size: 2.7 MB (2678521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5a90a2c1ecf48259a8890a75e97521870fa5ea9d42d80cdfb2e9b9c79a5306`  
		Last Modified: Tue, 02 Jul 2024 03:03:57 GMT  
		Size: 17.0 KB (16993 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:e28bf50af97922cca551dc09b30422907d712b63df3f2c6b4c3d263d67325146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192868195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3cffd33ad564ca02620f033341448513abee96399842b3561ff57c670a6f97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20600bddf485a5aa02c8d368967cf1fa8aaa3619438dd3864b4acc0050e917b2`  
		Last Modified: Fri, 14 Jun 2024 00:43:45 GMT  
		Size: 2.4 MB (2425639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812232f6a07c69d58840f90f5176bec9b5722d3dc8bf470610a4c226b346049`  
		Last Modified: Fri, 14 Jun 2024 00:47:10 GMT  
		Size: 155.1 MB (155130881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4feca97a7617864b23b611165ca2bf2a75c3d2f11035a9561a1224fa3109601e`  
		Last Modified: Fri, 14 Jun 2024 00:47:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:409ab98710645a7ecc48396379faf74bf62e0aba0a6974222b9a783e29a1b9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deee79f7a2098b4e6a27f0605d7c6b57bc3a7b67f5f8438916167bed51c952f`

```dockerfile
```

-	Layers:
	-	`sha256:995ad253352fe45ff03204d71f0adec7c2bdd865e65c8050da6797ec8e150b68`  
		Last Modified: Fri, 14 Jun 2024 00:47:06 GMT  
		Size: 2.7 MB (2684806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5cbe65d10aafba4da16894412da5b78e59aa4650da8700c7a174a508d0d2e9`  
		Last Modified: Fri, 14 Jun 2024 00:47:05 GMT  
		Size: 17.1 KB (17064 bytes)  
		MIME: application/vnd.in-toto+json
