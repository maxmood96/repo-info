## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:3b76fad63b5af508cef14263b60c13d51373d9ec6a3126dad6817a212c8a46cd
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
$ docker pull julia@sha256:3e7b860f5f1db844e2bc93dbedd4c6f96663b8c52c25a16f8c7c1d102bbb3c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287587487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab18323f6a57b47fd66a1ca8b4f2ba36e68e775f006d9db8e94b8eb2bb77827`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f496d3788734415954d688e6c3935b3be5ea2d0c5350d4e38f9743cf8b1d48`  
		Last Modified: Wed, 29 May 2024 23:01:30 GMT  
		Size: 2.2 MB (2223195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa99aa50f36d2b62d526c3720fdeff7cc5b26d84b838f6d55924a1b981028d`  
		Last Modified: Wed, 29 May 2024 23:01:34 GMT  
		Size: 253.9 MB (253929986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14fb8e9969c18ff8825995b09603bcf3c6da49a06800ed0f1a3ee0d9101f08`  
		Last Modified: Wed, 29 May 2024 23:01:30 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:c8158ce2d52e854aa7f4e435981d088a6c580186acea8ad2ca0f138340692dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc30a10048a7e22f48c938855a4ee31f741f2a3882d2277dcd6cdacbc471514`

```dockerfile
```

-	Layers:
	-	`sha256:d735bcb4c24dad166199e4d7322aaeae9de3b83680ef7a1ac8aa371d63b3d72d`  
		Last Modified: Wed, 29 May 2024 23:01:30 GMT  
		Size: 2.7 MB (2680132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b954c44ec96c8da94c1cc8217d9949b0417b18b0024a94f4fd5b2fbb004c0b17`  
		Last Modified: Wed, 29 May 2024 23:01:30 GMT  
		Size: 16.8 KB (16782 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:640f8d888b0aae86314221f0a8d3b0058fc8e8f57d8287359dc0c190a7d5f68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287928913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b118e85ef0af5dcf2c1d629a12d9123d09b0341162fffa08e11106a5f448f1e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897c1e111b67daa80cabbb9efbcdda65fc08c835692e6d76dc59e22093a19ce1`  
		Last Modified: Tue, 14 May 2024 17:34:13 GMT  
		Size: 2.2 MB (2210820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcff68b6fc8f5b00cfa8ad5e085c53e5d5a071d371ea4fefd6d09e60b377203e`  
		Last Modified: Fri, 24 May 2024 15:20:27 GMT  
		Size: 255.6 MB (255630811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdc6d425c6e866f068e87ee4d6670afe5ead415ec093d2df600af1ad256ac91`  
		Last Modified: Fri, 24 May 2024 15:20:21 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:92d9f82aa2915acc54ef24fafd04337e0fe03388badf87b2e98cc6a56e464cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2697137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1e86082e0f4ab3eae08e27078d286a9d6eb8d16ab520085c10181e868548ec`

```dockerfile
```

-	Layers:
	-	`sha256:5363de0cfb66436846f818606a84e914192a369220e514261e8514f9fc8eb7fd`  
		Last Modified: Fri, 24 May 2024 15:20:22 GMT  
		Size: 2.7 MB (2680347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f89332795c6a380e49bb0db55abac9e23f122752006f6515f9a0484111b2b5e`  
		Last Modified: Fri, 24 May 2024 15:20:21 GMT  
		Size: 16.8 KB (16790 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:7cc4272b88e277aefd903440185873edd1f2b180e7fbde1152322d312a0f3988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265903954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6562bad0cb148fb51e1c113480f23919a24cf6ddb02422901e93e109d1a94092`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
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
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf65b6ce7c72c2ed2743c6a0bf52813cbaa7cc01f3b0756f908963a65dc2ec`  
		Last Modified: Wed, 29 May 2024 23:01:29 GMT  
		Size: 2.3 MB (2329008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8435ef5788cdc207a67ba020160be0d5078799ae68545f9755a930f4aa066d32`  
		Last Modified: Wed, 29 May 2024 23:01:36 GMT  
		Size: 231.2 MB (231150528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7fc78c82ce72a4e6bc63c59711ef4fe28b8966e9ee61d75f863410d9a7d027`  
		Last Modified: Wed, 29 May 2024 23:01:29 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2d17178184f75c0a36794d190956d67fe6de9362a31d7251d9edc061fef5aebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d75139acdfcde0513891e9ab5e0462dabb935063f1398b395b78b15ce5527e2`

```dockerfile
```

-	Layers:
	-	`sha256:921c14297e135ffe31b87c01682f54221d80365027c47f108cf8a1b51b13f0b5`  
		Last Modified: Wed, 29 May 2024 23:01:29 GMT  
		Size: 2.7 MB (2677235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c967116a543641ffbbab461d8b259edaef7c5b42f53e214378a7afb4332c4add`  
		Last Modified: Wed, 29 May 2024 23:01:29 GMT  
		Size: 16.8 KB (16756 bytes)  
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
