## `julia:1-bookworm`

```console
$ docker pull julia@sha256:e542599ea83cddc5274ddf59ffc5f1d9e0cbe402e027c1f5f09c8f2922de6187
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

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:f3a26460de3d9150bd92834f861acc4179db300b092ec6fb4fe95e732703e4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205910486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ca5a478b9804111a77c7357052a1b1ccd495cca987b90bdca51d83b5ec5bb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
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
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310cf02ca32ac07452b6ccd3bced5afe95edf19882ba29ba5effa2c1904f6fec`  
		Last Modified: Fri, 12 Jan 2024 00:22:29 GMT  
		Size: 5.7 MB (5707818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9637c9c4ecfca46dbe4d52e79d0119c9881ad47288804b398620d0694a9e77da`  
		Last Modified: Fri, 12 Jan 2024 00:22:33 GMT  
		Size: 171.1 MB (171076378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715e74b090ab6aa3d74e6af29e6fc4193ff00ee8ee8fecc1c999d2921f4e38b`  
		Last Modified: Fri, 12 Jan 2024 00:22:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f07607bfbd8ad25da9ef064759ebc9197d39af8df886f4d6cba0325a14339b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1b2120041fc6ae79f940f4f4f6ac2fe4c73ce41c84311f0c5be5d905e5e230`

```dockerfile
```

-	Layers:
	-	`sha256:43ee8d5647b58c25cce90e9bb57a851d2d6ff1f3afc760dbac890844f92e7a76`  
		Last Modified: Fri, 12 Jan 2024 00:22:29 GMT  
		Size: 2.1 MB (2102613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e15b59632229216202af49f0a07a9f19b769189899cb78c103b4ff14e9dca0`  
		Last Modified: Fri, 12 Jan 2024 00:22:29 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:32698ac6928e4c91458503563c503cd66defc9cff78187271cbb79f4e7b853ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199068971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e830cc5bf90dba6810744f43e99e6c36e929a67d275eecddbb80a385428bf8aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
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
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f7cf52433138a2c47328aa19fa42f3a59d4affebe7880a1d2a6c74dea502d6`  
		Last Modified: Fri, 12 Jan 2024 08:45:41 GMT  
		Size: 5.5 MB (5532911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6730ed89cdff38e7f11457e27247a425069e5c3859bc05434c8b60d2be7747`  
		Last Modified: Fri, 12 Jan 2024 08:45:45 GMT  
		Size: 164.4 MB (164378353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a13a01be8466f4e93f0f4014bb77a24d866a1935aad49241aaf4a96672b8e1`  
		Last Modified: Fri, 12 Jan 2024 08:45:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8e93abd24f8ee770df38eb06c24d8e3a27d401e35e96dcbf99fabd6541d77ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1efcba94ee93190b065aac35b6998447e1fff30c8d2b4dd9eadb418268d7a3`

```dockerfile
```

-	Layers:
	-	`sha256:fe0992275b8b4ca946221edfe6d2727aae4e9ec30d39dd1248f6f3f285a46e73`  
		Last Modified: Fri, 12 Jan 2024 08:45:41 GMT  
		Size: 2.1 MB (2102956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd0bfe4eda24a01f0fdfc31b3de3ba72ae6ce9f677f422fbe84e7f3abf7a5775`  
		Last Modified: Fri, 12 Jan 2024 08:45:40 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:515b50db5346df05728c46e30c0a4c3a374ef99bef9986bb4e4b6692e564d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192477740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e830ee49a13c3b51b58e184ddb7e3d5024a5ae85c4dca0ec269c501ab697bbfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Dec 2023 21:02:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
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
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b27c98a9b5cfe6e3956fbc449a8395a7a8aaa26db72df8f513a2a964ba1585`  
		Last Modified: Fri, 12 Jan 2024 00:22:32 GMT  
		Size: 5.9 MB (5863062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec8d0fe7daf9fe63dc4ebe462657047ca858d706bd8ea8c31b686a24c85dd68`  
		Last Modified: Fri, 12 Jan 2024 00:22:36 GMT  
		Size: 156.5 MB (156470437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f750d44352d97aa3dc2bd9284ed8f9d3f092c3c3eb51d1e210676025a615b34`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bcd6d6f3b1e42b3e8685832c4a87aeb7fb895d6064de6dd3a2811ca6e6394a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83204b8501e886b565f01d8a294161513c09312a73ce7949868a2f3270b87e5`

```dockerfile
```

-	Layers:
	-	`sha256:2fba536a6acd195a67fb67774ecfa9124a60467d243a7360e540496c5d5521cc`  
		Last Modified: Fri, 12 Jan 2024 00:22:32 GMT  
		Size: 2.1 MB (2099791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626f1ac07a5e56514580f20c195c258ffb02223b289ca5224b2a4187ffc00294`  
		Last Modified: Fri, 12 Jan 2024 00:22:31 GMT  
		Size: 19.3 KB (19305 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:325ac0a3f417aec8945bbaf81465a510eebcce5dbd022162ce31586ce3200cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193350014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6cad9262ce3dd21576120a43d0a40b78f99dd3b027741bc2d178a07f3a9ae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
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
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bae7f9e69e4afa463380685caadff4edaa3055e97bf026ab11cd5cb6cd879`  
		Last Modified: Wed, 20 Dec 2023 08:34:45 GMT  
		Size: 6.2 MB (6239245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6980b716c2bb2b223400e27f927e5375f5fda99d9f9c703c99bd0bebf15694e`  
		Last Modified: Wed, 27 Dec 2023 22:14:31 GMT  
		Size: 154.0 MB (153989838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31dbd48963269970cc5d4ace06aa9b9a1a0031e7a8a99c3f9afdb83b242c18`  
		Last Modified: Wed, 27 Dec 2023 22:14:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7c1d68cb143f0fa9969a727c314eb0737252fa03f54c15be249fba178aecd86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2126403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f383bcc582d395f397ac9a667cff169204c2891f193b5bb5c1170031f2227d6`

```dockerfile
```

-	Layers:
	-	`sha256:c8cda625aaf8a89cc229badfbaed37ee2b7921f97457d3e8957e2809f9836357`  
		Last Modified: Wed, 27 Dec 2023 22:14:27 GMT  
		Size: 2.1 MB (2107150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8959dfcc6581e8f98546084ed4389cbfee9ae5ee7d9f886dbaafcea488d1249`  
		Last Modified: Wed, 27 Dec 2023 22:14:26 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json
