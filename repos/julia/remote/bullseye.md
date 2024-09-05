## `julia:bullseye`

```console
$ docker pull julia@sha256:76b6b6506322c4ee54eb87c137b5bae8f3c9262ef3ab6619db043dd1c521d93a
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
$ docker pull julia@sha256:4765ab77db40b9c5a5faaad440b7668e7611428e9848d6f874e54f90d8d98cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210263499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f75677ff627f9c104f84a70779aca361ec516ebf61cec0730cfd653ca2405ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423763e23ef554de148c4bdb6f21c99d8ac682a6ce592710762d2a8a3deb041`  
		Last Modified: Wed, 04 Sep 2024 23:10:19 GMT  
		Size: 2.4 MB (2426566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb394c6484a89bc027e33117b30674d1244e5d923ce229cf4bfcde7fd219074`  
		Last Modified: Wed, 04 Sep 2024 23:10:21 GMT  
		Size: 176.4 MB (176407886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b837dce30e135471a49460c4c71b5ffa0cde6ab87fc01214c17a9995da7cb39`  
		Last Modified: Wed, 04 Sep 2024 23:10:19 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:02de831224c74cbad8cec1fffc183d3f720c6b55633ff7d60422b4eaa52a3884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847582ef62d8468e29b1dfd92b7a3c6e9bec9ee722a9ef3c47151d31df80b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:460d983a3d621c8284bda7d9e40a02629d1559c4b27e114dfb37207bd4fde222`  
		Last Modified: Wed, 04 Sep 2024 23:10:19 GMT  
		Size: 2.7 MB (2704245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aabe4d5725e9581ee9189d3009524a3f270267a0043079a10fafcb51232f1b67`  
		Last Modified: Wed, 04 Sep 2024 23:10:19 GMT  
		Size: 17.0 KB (17024 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d8d78f485575b44d47a520ef507c99dd75a375b5d9288a00d988e99f2954019f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209721252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edd7ace446a1c1d25a236e9290703910e9c6bd900ce778b3e9ca804f543ae84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa630b71e57d93c6c4a298a32f8abf58c36a28a92b39609f86ee56a5c299803`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 2.4 MB (2415117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41a0df9c8c24e0da357311867e92a8fe28f5a53b916fc375d8bb178dec3b6fa`  
		Last Modified: Thu, 05 Sep 2024 12:25:02 GMT  
		Size: 177.2 MB (177231399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cf43178cfdab2ad464ee20edcc7595e0447fab093ffa05a12d739255150049`  
		Last Modified: Thu, 05 Sep 2024 12:24:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8ebc840316405f8a4652b9e58635210379303c5275d79d35cfb7b9b347446ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b020507b6aeed55bd1ff86a68bd2c9c142d9c7dab415fd6333cd05d093a92937`

```dockerfile
```

-	Layers:
	-	`sha256:fa19f86120a01b419296aa99f656f64d5fd2fa78a10912541f34bd81b845de1d`  
		Last Modified: Thu, 05 Sep 2024 12:24:58 GMT  
		Size: 2.7 MB (2703391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2c6fa0783c7396468ad5411cbd21693430f7d31cb1d6265243505911e780e1`  
		Last Modified: Thu, 05 Sep 2024 12:24:58 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:40c34f492da2f2fb4dbb0911321b1a6b2045eea2499b43ada0dd4e73d3970209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192749131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce83a03c4ed15f1453278227a25e309660c01b6d08b27cebec8e588d846df87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f4950f242e8a9e7e2819e85b8097ed36b6d80028b5790fc64b36e1e179f01c`  
		Last Modified: Thu, 05 Sep 2024 00:07:54 GMT  
		Size: 2.5 MB (2533031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55c6a796524b51df7e76e9da0a377f9a349f397e0bd1468e8bc47a3257c72d0`  
		Last Modified: Thu, 05 Sep 2024 00:07:58 GMT  
		Size: 157.8 MB (157802413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04b67ea03bdad41b9866e481a432ecaad2d6baf25ec16374fa46df68379c40`  
		Last Modified: Thu, 05 Sep 2024 00:07:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:def723caec0ee6b471982af14a7146337321e630d8ab431365044b3ce6e638a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6a7a2d874fdbf980f2d87435061f4c14840cc7e6f58ae1c5b34377ab134e1d`

```dockerfile
```

-	Layers:
	-	`sha256:1d42d2f7155a24d689928f625bd499254e788704fede3362257a208f317ef3df`  
		Last Modified: Thu, 05 Sep 2024 00:07:54 GMT  
		Size: 2.7 MB (2701343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f269c8d73c9038d9dac6ab44fbdc84753aac7cdffd8d76cbfeaf86ff6987e51`  
		Last Modified: Thu, 05 Sep 2024 00:07:54 GMT  
		Size: 17.0 KB (16992 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:3c27739e16834840fb2193206c17aea5f620c6a8560a6e2664bd2ad633032ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193068160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02be4a7b625e6de8c6e87e54c764383b27cafe79d73e6086b8b1c24d776a862`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbb0c0469be47f8494a9cc686d3a871114819d6faf484d40a9aa54c23b8c5c`  
		Last Modified: Thu, 05 Sep 2024 00:36:57 GMT  
		Size: 2.6 MB (2629989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf62b3f5fe5ba724e9885b9e1659ab34ccf3ebc23f87349695189ac132632f99`  
		Last Modified: Thu, 05 Sep 2024 00:40:25 GMT  
		Size: 155.1 MB (155138524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f254da90928bb7bf7261384318e1c7e405d05f75fe7859360aed07e3a24d85`  
		Last Modified: Thu, 05 Sep 2024 00:40:21 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f31c95ed79b7663880cd8c35ee0fb4db52b6593c335c3a491c59db227f2a342b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2724588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2a178d6968357334c0dea1cff0085f9e98066c25bc154405ae8777da55cfab`

```dockerfile
```

-	Layers:
	-	`sha256:52a2e67e9251e03cab13124fe1a6d3e61c6ca080ee7dfdc9d00d5f731fda5b43`  
		Last Modified: Thu, 05 Sep 2024 00:40:21 GMT  
		Size: 2.7 MB (2707524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b913f796efcc258e4d9598487f681a67ee57394c428b346455fbe157a48cee9`  
		Last Modified: Thu, 05 Sep 2024 00:40:21 GMT  
		Size: 17.1 KB (17064 bytes)  
		MIME: application/vnd.in-toto+json
