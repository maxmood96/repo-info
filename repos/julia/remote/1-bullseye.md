## `julia:1-bullseye`

```console
$ docker pull julia@sha256:e5716b0af1f32b9bca623f25002e2503570d016e729eb9ce2f695a03008d8ac2
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

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:2e8168f5d3410efbdb25547c1a52516b9210f641bc488e73284f816f099ad72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182304407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788c896b32c3e5a85a99ed3a67b2206a7348516b792769dfbc2dc8d4d8a810ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["bash"]
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 24 Aug 2023 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e2ebbb13946e35da058566243bfdc7e386b08fc76f13d0d7e796919979afe2`  
		Last Modified: Wed, 01 Nov 2023 01:02:48 GMT  
		Size: 2.2 MB (2222798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852dd2045553cb9903c334fb6d598a2cbb2c1bcdc56ef4343351b9606c57f5ce`  
		Last Modified: Wed, 01 Nov 2023 01:02:57 GMT  
		Size: 148.7 MB (148663326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8faab2caa46d7c76ccc5f80b0dcc7efeba988e073608834ba6d4efb09351f6`  
		Last Modified: Wed, 01 Nov 2023 01:02:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:128c2a7ee667fde27ebee23cca30c120d7d9e58e9c79fb4e931c0fa030dc4512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b3a0ef2edfaa74442ac136663053e637f48921aa9f3d975abf0caa464d1ee9`

```dockerfile
```

-	Layers:
	-	`sha256:859039f68da468f4a5d2417977cdab32f74b259c44f2c30e7a38015769a26b28`  
		Last Modified: Wed, 01 Nov 2023 01:02:48 GMT  
		Size: 2.2 MB (2230350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e7f8d3f3885cc519540292e8dc0f7301208e5b1390ba9edd1f908182cb130f`  
		Last Modified: Wed, 01 Nov 2023 01:02:48 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:32a06c604899a402835a8acaf5bd0841475a59ca1f8389e6f4596bc634372e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175164307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4346ec18b9e5b3079e610022c521dc4a2ee1c8bba52e5baa1a3bc35bb2f58d08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["bash"]
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 24 Aug 2023 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc6a6591ea70d098f880a09b6a8d4ddbc69946d890b981eaae68df3a27d0870`  
		Last Modified: Fri, 20 Oct 2023 20:14:16 GMT  
		Size: 2.2 MB (2210559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ad1d311ab44749a099573bee164c987a8f28cd6cd1d03721d779df034f5142`  
		Last Modified: Fri, 20 Oct 2023 20:16:34 GMT  
		Size: 142.9 MB (142889291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e17ec0572a9ccfdc85acf69ff083caf350ca6003a79a481ec6eba1259fb20f`  
		Last Modified: Fri, 20 Oct 2023 20:16:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cb746fe3a7a0e434df929cca2a91f745d4adf93921e55496531048bf5e4c9f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6337e8f9490438b1340ae46a4c3558a183768c65895615b6c962b9ac0486ca33`

```dockerfile
```

-	Layers:
	-	`sha256:d9c055b329929544f08425395ddb7665cd4c5a92318272c52ccfd837cb5cf879`  
		Last Modified: Fri, 20 Oct 2023 20:16:26 GMT  
		Size: 2.2 MB (2230675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83dd76d01d819442e6ca1d29f327a22f79fa91097b05b20629bd4aacba21dec5`  
		Last Modified: Fri, 20 Oct 2023 20:16:25 GMT  
		Size: 17.0 KB (16953 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:915d4e2fe86456676f3464aa6d92de0ed10f3abd3b61a448364ff0cd9fbb2b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172130560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d98f458f78361515651758acf438ba324a4232eebd6b29701d03d6a6b73cb72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:67f223c9c48e525a23fb110e4c105d7128dcac0c10f32c38f98ea84a21d2bd00 in / 
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["bash"]
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 24 Aug 2023 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bc6810e8fe9346a3caaff984163b789d12b6964a15a2029e384143ca19fef5ad`  
		Last Modified: Wed, 01 Nov 2023 00:44:14 GMT  
		Size: 32.4 MB (32402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae7e8808d63f1dae8b3b1e10e0991622081959ea760bf237027d3f588eadc55`  
		Last Modified: Wed, 01 Nov 2023 02:08:26 GMT  
		Size: 2.3 MB (2328520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad2d5dbbda1127440942f261d3f01cef058509328591e1300521b2a01be51b`  
		Last Modified: Wed, 01 Nov 2023 02:08:37 GMT  
		Size: 137.4 MB (137398976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79aaaa102d5b48a2797cb303b62ede9c12d742e418703801ab717f4af7f85219`  
		Last Modified: Wed, 01 Nov 2023 02:08:26 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:27c35146faee2c4d71d5c286791d2423feead9d7f7422b252b3e7db67db41f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 KB (16863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549ea1d66b5402fe2bf3f25c70642dabe48ff8280729462ac4f2d545708fa4fe`

```dockerfile
```

-	Layers:
	-	`sha256:bf14794920fd2b050afc89b617cc91c71833b8fa111b3996e574bbc659914b8c`  
		Last Modified: Wed, 01 Nov 2023 02:08:26 GMT  
		Size: 16.9 KB (16863 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:edb3404ed938a34565d94912fbb2f69bc0af9379a729dc7239a6e8410cdebac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170722825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b173c2feec23ea5120e4dbdbe8f51e85693f37074ad27b64c56ceaf80165e14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["bash"]
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 24 Aug 2023 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 24 Aug 2023 23:59:15 GMT
ENV JULIA_VERSION=1.9.3
# Thu, 24 Aug 2023 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.3-linux-x86_64.tar.gz'; 			sha256='d76670cc9ba3e0fd4c1545dd3d00269c0694976a1176312795ebce1692d323d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.3-linux-aarch64.tar.gz'; 			sha256='55437879f6b98470d96c4048b922501b643dfffb8865abeb90c7333a83df7524'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.3-linux-i686.tar.gz'; 			sha256='e968d04a8b91e2bdcda307dd9dc26e7589b6c8f9598b2410856c95a706d84b10'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.9/julia-1.9.3-linux-ppc64le.tar.gz'; 			sha256='15bcf163813d9a561ef50c77d1135135455c85f2dbd27a910400332edb959dc4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 24 Aug 2023 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Aug 2023 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b12635ffca02cd73f6066a96e094570ce5cf849c42a93995b01ef11180417a6`  
		Last Modified: Fri, 20 Oct 2023 20:02:25 GMT  
		Size: 2.4 MB (2424847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c8953f1d13fbc981849166487451feb407055eff7643143f83d062dd961d47`  
		Last Modified: Fri, 20 Oct 2023 20:09:56 GMT  
		Size: 133.0 MB (133003891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed36667dbd7bc875f618a28ae058da8b0a4704e0c5601e81ec097c3a9bf4fb63`  
		Last Modified: Fri, 20 Oct 2023 20:09:49 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1cfc480ad6b944ca6b5ec1bd80629eeb5aaf92b8f6122cddbf2c1fad22c05a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2251836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a908217db713ad0112cdcc3a9052d0a58a22df9f426eb5e307e4b2ce6aa479e`

```dockerfile
```

-	Layers:
	-	`sha256:7e6542bfa62f355a1de390c32eaf02a41f2ac16d4feb2ce195ecbfcf93d373b9`  
		Last Modified: Fri, 20 Oct 2023 20:09:50 GMT  
		Size: 2.2 MB (2234853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a18f015c2faf5f54b02e63d4d8ecb83300ef73047ef2c4be603b163d137b074b`  
		Last Modified: Fri, 20 Oct 2023 20:09:49 GMT  
		Size: 17.0 KB (16983 bytes)  
		MIME: application/vnd.in-toto+json
