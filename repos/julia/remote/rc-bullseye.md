## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:1f546aff5cd923c329d91f4d49f51aee2d17de5e460bb75aba66d55cdc20bff8
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
$ docker pull julia@sha256:26a126a0320a6c62a94ef2aa2fd1b596b6e98d55f15ac1cc99ac127c8839227b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287587566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27099bff9ed1a779864783b6fa433c3f2243cefca9792dedc3e18247b5ed913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 May 2024 17:59:24 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Wed, 29 May 2024 17:59:24 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3dddab88486ca242615c8614a763f5c0ce2bc79f6e217066ec5953ea32d736`  
		Last Modified: Thu, 13 Jun 2024 18:29:28 GMT  
		Size: 2.2 MB (2223182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093008ea14e6b174055cf2f64c47f84981c03e9f49299b2fe986a9b9227a76ad`  
		Last Modified: Thu, 13 Jun 2024 18:29:34 GMT  
		Size: 253.9 MB (253929972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bb07fc04db4e70b817431eaaaf38465f0557dad790697bd82e4307cbd84f4b`  
		Last Modified: Thu, 13 Jun 2024 18:29:28 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:24578c6e3c7a833d75282e4364fe6b0debea8985c5d1066a83cab81d57a11315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4445a86bac3e762ba1ef71658d4c05202ac49289802c41393ecf8c9e5eef74ed`

```dockerfile
```

-	Layers:
	-	`sha256:56a2a6cefd4912b63be18b11c2a064c66ab4dd6d7c3502b2fbb8de022770b1c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:29 GMT  
		Size: 2.7 MB (2680131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d791bd2ceb9adccb0cbf5c40539bb2898f480cf5100220b61df243f91f53758`  
		Last Modified: Thu, 13 Jun 2024 18:29:28 GMT  
		Size: 16.8 KB (16831 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:39d869dccc542f41de2fd31f2acf4c4c4a04f8c5a98c82c10852a3a46580a184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283095774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ab91833ea6f0407a4258bf5e32a5b6dd496ec66a77f998534eb01cd3f1e832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f730fdf4762f907bb602a60a5c7437c3fdb7378dca6e8ed424ae0838e503b0`  
		Last Modified: Thu, 30 May 2024 11:47:32 GMT  
		Size: 2.2 MB (2210782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e869bf97452c74bb47494948180b0ea0a77bfbd4f880c88814bdc74ac9701661`  
		Last Modified: Thu, 30 May 2024 11:47:38 GMT  
		Size: 250.8 MB (250797710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a485606b5464716a680cd47b017c20d57ca387dc83966ecef87e2c7fe8da7c71`  
		Last Modified: Thu, 30 May 2024 11:47:31 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:60c2e8308a0a018a1384595f26d4b3635c440fa52dfc78da74346db7a0ac79f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6273021e28ecf65f322735b98ec3e71252e7734b89516fa1a1b17bcc8e4ee05a`

```dockerfile
```

-	Layers:
	-	`sha256:f808d5ccf932a8be6febc53425419adb33a0e5af35d404af51f64cbe9dc869f7`  
		Last Modified: Thu, 30 May 2024 11:47:32 GMT  
		Size: 2.7 MB (2680382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d619efb761c7070a39a1bb4fcfd53fb585cd610bcdf0a733c319d638b5b91c`  
		Last Modified: Thu, 30 May 2024 11:47:31 GMT  
		Size: 17.1 KB (17077 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:bdd9463c77263cde38caf6b75b0eed6c7edd506fa50d0740231be207848f24dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265904013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4f1fb9a1dd6e60076fb885b71fa89211a7f03b2c234fe06e4f030b9b1eef58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 29 May 2024 17:59:24 GMT
ADD file:ef80ad838dee1f170442a02f8d0808e624e7c317df766c49aec042c1f3ac4732 in / 
# Wed, 29 May 2024 17:59:24 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:71e749b27156c50e0706f9267afd1ca9fb38d6272a353964948602fb62336fd8`  
		Last Modified: Thu, 13 Jun 2024 00:44:08 GMT  
		Size: 32.4 MB (32424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e1cab57f8d61dd527a77a8955bb9b89dd9bf6df01c38d637d273de1c619539`  
		Last Modified: Thu, 13 Jun 2024 02:00:06 GMT  
		Size: 2.3 MB (2328956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9bcc968f590a03041f0a928327a4486f222d9cf7ff67dfe69d42fca3bcfb77`  
		Last Modified: Thu, 13 Jun 2024 02:00:11 GMT  
		Size: 231.2 MB (231150503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9712b92714ee4409fa0c8237666ebc74c54923eee0dc215b999290c57947ca6a`  
		Last Modified: Thu, 13 Jun 2024 02:00:06 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d9a4a76e8dbf97194edce92681e9cb10208da119c70a91313b80ae65aeead8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17e8fe20a056e57fca7a8f2522757947eeb594ced5855220ba967b756c1e9b3`

```dockerfile
```

-	Layers:
	-	`sha256:d7f383c9ebca67f09dda0e6493694a72f95089751b02518f3083236154e5ef56`  
		Last Modified: Thu, 13 Jun 2024 02:00:06 GMT  
		Size: 2.7 MB (2677234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b66808dba88c6020c5680f5332a3ca97a5eea925943114a0925d5a1934cbcd0`  
		Last Modified: Thu, 13 Jun 2024 02:00:06 GMT  
		Size: 16.8 KB (16805 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:7b4da651a338a5792831b148f975fa96ce925b9404ffb29aa7976498b2e3bc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.4 MB (279385813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6e86af663d02650790ede28f3cf2c01b4823411ec07010d8f74e3ad4d72ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70534c247f1ddb98d2d242165aa874c16f0224944feeb0cb2261c67853a7c9e2`  
		Last Modified: Thu, 30 May 2024 03:16:28 GMT  
		Size: 2.4 MB (2425589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1398bb66f6317389b0e558790fcf610ca7a2f0a983abef5bce582859c1ce371d`  
		Last Modified: Thu, 30 May 2024 03:16:34 GMT  
		Size: 241.6 MB (241648688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8210ccbbab6832834dca9f4292b5f6707dc8018bd09a5325696ce3880af0f1`  
		Last Modified: Thu, 30 May 2024 03:16:28 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:c83ac4c16809e7478c7175e284332f74ee8e971cdb110fb31bc6d519dd984cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2701337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b1f487d24127902613a542c6a41a6a64bfb70ab12bc2410203080b4323aaf8`

```dockerfile
```

-	Layers:
	-	`sha256:99aa47cab40fd9df3ddd8391a0848d7358cfe0b791adb2c04b827df60cdeef4d`  
		Last Modified: Thu, 30 May 2024 03:16:29 GMT  
		Size: 2.7 MB (2684521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d37228a79f2caaac1cd7dab17fbbe364d2d753ae9bcc14fa1ca7526c7855a50`  
		Last Modified: Thu, 30 May 2024 03:16:28 GMT  
		Size: 16.8 KB (16816 bytes)  
		MIME: application/vnd.in-toto+json
