## `julia:bullseye`

```console
$ docker pull julia@sha256:7e31beb387fd40a2423a09708c2f2a205e41fcbb4c9d56f6e0a6588df5a7ad2a
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

### `julia:bullseye` - unknown; unknown

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

### `julia:bullseye` - linux; arm64 variant v8

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

### `julia:bullseye` - unknown; unknown

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

### `julia:bullseye` - linux; 386

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

### `julia:bullseye` - unknown; unknown

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

### `julia:bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:c9651e2ceabaeaac2be6e3ea3d287edc24d4b55549e0499949f8a2739ee2a302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170722866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e68af52f79628bd21286668a8a2da380b34e017f5ab074408a55743de15950`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
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
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18b73091125f2b78d22b50ccf4901ba0daac56dcf2d60f317040a844f84eba1`  
		Last Modified: Wed, 01 Nov 2023 15:26:58 GMT  
		Size: 2.4 MB (2424869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e39547a5b8aa08a5071258e67d05493bc11c3ec9ca3fb0c480d0fbcb568693`  
		Last Modified: Thu, 02 Nov 2023 00:46:00 GMT  
		Size: 133.0 MB (133003819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bbcbbb523d81d050adfb965966eeca45388b0e166429c1d94f6d9d627cc75d`  
		Last Modified: Thu, 02 Nov 2023 00:45:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d5d35ba5781d7feaaee98d44c4ac17e12c1e8c28b50f71f3fc4f883017caba8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2251836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574f5f32a268775218380c27c34b7abf48b7b08a3863bc9308036b7be148cd0f`

```dockerfile
```

-	Layers:
	-	`sha256:62c5d935509220eea292e929583f6202069410372141aa54cc2ef9897a3bdd2b`  
		Last Modified: Thu, 02 Nov 2023 00:45:54 GMT  
		Size: 2.2 MB (2234853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbd95869aac35e35c9fc130cb2aa20ec75d9ea8516e262e07e8f733acc2ae39`  
		Last Modified: Thu, 02 Nov 2023 00:45:54 GMT  
		Size: 17.0 KB (16983 bytes)  
		MIME: application/vnd.in-toto+json
