## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:c4fb867a4e5d6cbb4f2cb86d182250d955f71a3f787613c0cb17a62b9a60c1f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:4788917a1d372e40cd3061025d30279dc4f8200dd12a533af10219036809af47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334178345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99aa3bd2739b5596a40dd2cdc8df34eeaeaa9398e362b25a5e14a81d83d90f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7efa7f19b13fc5f35884f0dd46d745f0ea684f89351944adfbf9addc467fb71`  
		Last Modified: Fri, 04 Apr 2025 20:38:57 GMT  
		Size: 2.2 MB (2222634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314257dd8fb88a48c908a963e1f15657bf1c6d1b8cb1a11b60594a4c3197483b`  
		Last Modified: Fri, 04 Apr 2025 20:39:02 GMT  
		Size: 301.7 MB (301701505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2659aa180591f1b4b14f8b4e9b29b5c5d2275181f1d0f95dbeaded231a13fb83`  
		Last Modified: Fri, 04 Apr 2025 20:38:57 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:c3074278146a2d4f1f41ccc893b52f08bcf76bffb3f9b55bdf6935e9b0a9468f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697ff77e31bb4de5f157428e1b535823adda4d082406387ddfde6f5fe0f20910`

```dockerfile
```

-	Layers:
	-	`sha256:14f09cc91bf13d9318e01452617c269a33241b857d9f18e86c40d46ec0bff7ef`  
		Last Modified: Fri, 04 Apr 2025 20:38:57 GMT  
		Size: 2.7 MB (2712302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7617854cf1fcdc662fce2e7a6cb20931afdb0d496f7dd7269a59e8eebbbd043d`  
		Last Modified: Fri, 04 Apr 2025 20:38:57 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:19bb130a0364b3052f159b9c5a325908967659c00317c0ea6f230b78acd98ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.3 MB (354318783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0235498a0936c975c8ec3e9ca2c8e222dcb6a9cb82ccefb53187699552d046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac554a221e97d13facdef50750e5ce351349ffdc50e3b04dc22222b54c238d6c`  
		Last Modified: Fri, 04 Apr 2025 20:40:26 GMT  
		Size: 2.2 MB (2210297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c82f26aff963ff8420205d0732e6947f8004fd351770c2f3723a5598a174bad`  
		Last Modified: Fri, 04 Apr 2025 20:40:32 GMT  
		Size: 323.4 MB (323362191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a63c4b5eb0c1f074fe40719884e82a48cc0fa507ebd4f0bf9622fdbddf809d`  
		Last Modified: Fri, 04 Apr 2025 20:40:25 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:26f7a0f421cbf75c64bb8fb9a19b20639871b2bdc7429fc6d82c19ec5b16225f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd062416c496e2e8df149f0c6c90ed1ace4f1f59af6eda6ce03c51fcd554619f`

```dockerfile
```

-	Layers:
	-	`sha256:3e7d98cd8bb0c0aaea8dc8af34f0ebba268b66115df12c2ad0f6dc8fd2c8d517`  
		Last Modified: Fri, 04 Apr 2025 20:40:25 GMT  
		Size: 2.7 MB (2712553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06134da68afa3f8ae1e82123a4534bf271ccd3d2c726750be18d09540da12ae`  
		Last Modified: Fri, 04 Apr 2025 20:40:25 GMT  
		Size: 16.5 KB (16484 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:5a0a364156bb69b51f56ca9b3b8e408d776afbaa76cdf26f2e7a01a1f7d5ea31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274072086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd93a2a7e887941e3da9930dddf035151a13d60491fa9641d2c268b931df06d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67f9e1e2bb85666a75916fcdc72a04dc736de2fe0f2d2b89833ffc32b18c7a`  
		Last Modified: Fri, 04 Apr 2025 21:08:55 GMT  
		Size: 2.3 MB (2328089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48fd44faf9c63c16583b64e8e9e7f119411394cfec04e0a75965f86d620102a`  
		Last Modified: Fri, 04 Apr 2025 21:09:00 GMT  
		Size: 240.6 MB (240563287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1088d30d13cbafce74113e31f2a57538c99fab34961733b01a8a21d5ce363b8`  
		Last Modified: Fri, 04 Apr 2025 21:08:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:ec6ba4bf426965c68e712ca8bbaf05ca1c4e92be3955478ca4652b36ab6d09b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df27d246ba0cd68c2829dd8e49a8085e6756733aded6dd00808cd459101aa2b7`

```dockerfile
```

-	Layers:
	-	`sha256:c7db14ad822054220f59353f6ecb2c27d5c434f2f0896ca2fb71ce03c1f29610`  
		Last Modified: Fri, 04 Apr 2025 21:08:55 GMT  
		Size: 2.7 MB (2709406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0681fc9ad4addca43d7213cab2a71bf2e9e6f99d4c4d802e81035c99c1a0af1`  
		Last Modified: Fri, 04 Apr 2025 21:08:54 GMT  
		Size: 16.3 KB (16348 bytes)  
		MIME: application/vnd.in-toto+json
