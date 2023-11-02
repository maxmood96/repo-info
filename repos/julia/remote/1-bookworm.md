## `julia:1-bookworm`

```console
$ docker pull julia@sha256:d057878caec56c5165036d489e3d563e5d51d04fc8d3d0cb4408ea9dbe661946
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
$ docker pull julia@sha256:884cfd22f8a5ccc1d07b2507faa840e2184ee01efa47377b77cab73ced0bfc98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183327779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7f598e99badd9b6d21cc66745a7b88de63512ec655b13caed6561fc52ba35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
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
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419cb484bd81151e4dd190982c3ac70a85c6791871787077e075f6da85d75c84`  
		Last Modified: Wed, 01 Nov 2023 01:02:45 GMT  
		Size: 5.5 MB (5513924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3245fde346ac8a5e89d93ce7165c875704384f76e762f494ea9bd08f6489e20`  
		Last Modified: Wed, 01 Nov 2023 01:02:52 GMT  
		Size: 148.7 MB (148663649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826feb43ad90107655afc23b44274634a0ae6793eaacdeb1081de8f555ccc2e5`  
		Last Modified: Wed, 01 Nov 2023 01:02:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f32c6620e123677ee89c0673ed667e3c248d1e63b39bda767ef1ec281dfa2631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae9ea01714a17144b8afe968ac7ccd24b44a34bd587f9289149dc2ac9105ad3`

```dockerfile
```

-	Layers:
	-	`sha256:a837ed0fb28b9bf9a071b0c2eea562d77f815b6e7a571716d56181e76aa9d043`  
		Last Modified: Wed, 01 Nov 2023 01:02:45 GMT  
		Size: 2.1 MB (2101478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c76df2fcefc71441041d54c2ca73521040739549f8fee2106d86bb5f484291`  
		Last Modified: Wed, 01 Nov 2023 01:02:44 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d2c4a2d3f48871baa2511e1dd44038b3e8b9097643a91c968953dbec4bea561d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177406956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73543d9afddeefdc0876c80d29e0e88a45060c6f17a8e1166012df6f3b531f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
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
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc0860576145b9aba41c89910507f1614704d3d427324ef415d234c50c70a1`  
		Last Modified: Fri, 20 Oct 2023 20:13:02 GMT  
		Size: 5.3 MB (5338906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e124dcfd6e489f20e28f8d23917c1d4d07223541ceaa45d0e365107d3e529f34`  
		Last Modified: Fri, 20 Oct 2023 20:15:31 GMT  
		Size: 142.9 MB (142888396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7a105cdd28c7043a72b05fc3a4a71450383b41e39620253ce57087a181aca`  
		Last Modified: Fri, 20 Oct 2023 20:15:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:cb97d17261e260f4bd5468cf5ea8eff57bc82438166084a2903fd19bebab9f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a7784087edb0b0a86d445259b891b9682b17bb7b7675d026bacdb1290dbc9f`

```dockerfile
```

-	Layers:
	-	`sha256:206d56c0916f487a6671e0b42c957af90102b3ae8612ba249de346bdddf5d8ec`  
		Last Modified: Fri, 20 Oct 2023 20:15:22 GMT  
		Size: 2.1 MB (2101821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda6b0fad33e5356a023ed54420c89fc1f1a9d5e7553ef6237d56047ec6eca2c`  
		Last Modified: Fri, 20 Oct 2023 20:15:21 GMT  
		Size: 18.1 KB (18127 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:58df9c6bf385cfb0ec6adc94162fff76f6dbc60b82aecbb02f4bf779956818d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173232410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7d7265ee80c33b0f84c0e3546f3dc5b5fd32492bd3205f159763089c6c41e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:0c94521fdd9c0a4fdeeb9aad23e68cd053fba0dcd7c3af550aefa79377816e31 in / 
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
	-	`sha256:98bdfce9af831c2a0d0bfcca812d0039cd1666986550f552b4b4c625bd5aa31c`  
		Last Modified: Wed, 01 Nov 2023 00:43:26 GMT  
		Size: 30.2 MB (30164042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb122e39c7f5bf8ec6e960e91357915a696111feafc56b6ca7f19aa46286b45c`  
		Last Modified: Wed, 01 Nov 2023 02:08:14 GMT  
		Size: 5.7 MB (5669502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d05a1f080437c3e9315c339a4891046c9c1c772ca8defdd6713c4c09520cd4`  
		Last Modified: Wed, 01 Nov 2023 02:08:21 GMT  
		Size: 137.4 MB (137398497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5888462e9c1f5623ba6c0b58ec172d17bc41002a9124a4a75421bf60d55d0b`  
		Last Modified: Wed, 01 Nov 2023 02:08:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:4d1d6f7bf41d80d03903fa24770ef318047974dec58b14dc303526167316fc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8c1983791ea94219ab4bc72fd88866170a6faf138df143a4032fb0e4c27398`

```dockerfile
```

-	Layers:
	-	`sha256:87f5cd6d2a7bac3dc7ad6d47b6e25731cdc2945bb8c7f81a3a4ae7a741c4d0cc`  
		Last Modified: Wed, 01 Nov 2023 02:08:13 GMT  
		Size: 18.0 KB (18010 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:25e599d39410d2174596cbe42a778ecc33ebf4e57ef008cb8a8e1d0acccf5060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172192283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b41b596ac2fa2d0b26adc74bf1e124b1f7dc2a46b9b5093a34b241453fa4c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 24 Aug 2023 23:59:15 GMT
ADD file:f36d600ab8508979b5763875a75f35555fa0a83d2656cbcdfa50978c6ae97353 in / 
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
	-	`sha256:e56c8f20d7d119ff87eb044f21bfd5a4b30bf8436fc5fac12871095a6bd1517c`  
		Last Modified: Wed, 01 Nov 2023 00:26:10 GMT  
		Size: 33.1 MB (33141482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731fefc00fefcf2648725a405996c24f3f813cefde0845d8a9540eb613b297f1`  
		Last Modified: Wed, 01 Nov 2023 13:51:05 GMT  
		Size: 6.0 MB (6045806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b61f5cfe1705734bd5139c1bdce4fc8ca58857eb886d83cfb35cc780f7c725`  
		Last Modified: Thu, 02 Nov 2023 00:41:22 GMT  
		Size: 133.0 MB (133004626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3141b67e2ea410e840a168dd4946c21b0baa941b742fb809a6bd0ce1b0e893f6`  
		Last Modified: Thu, 02 Nov 2023 00:41:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:905d19a5845d98c65d24d03366442ced28f9fe3667d62d65d7c5c9d380603e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182b4d605367012747ee485eadbaac2beeaa509f6dd8568cb5b4960f0e4b48b2`

```dockerfile
```

-	Layers:
	-	`sha256:67591b5fab7a6cca0bf087c86d93314d4f524aef3eb496c3f68dc20e04b9899e`  
		Last Modified: Thu, 02 Nov 2023 00:41:15 GMT  
		Size: 2.1 MB (2106015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f97950ea37cde4d2fed271c03bb6a409835d4235dadd5990f5c80cae4c5680`  
		Last Modified: Thu, 02 Nov 2023 00:41:14 GMT  
		Size: 18.2 KB (18173 bytes)  
		MIME: application/vnd.in-toto+json
