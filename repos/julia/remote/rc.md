## `julia:rc`

```console
$ docker pull julia@sha256:3f6b7ac13f6df0ff4563845a55744b1bec0493df4335a63a4eb0c56c5916da30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:1fbeb798e80b9f00d0240c15be784122e15d07c91d0576d304a420eaaa316c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283364769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff91db8fca56647d1caf2f63ace93d67c41119723c6b4eb00e19ef23c90dc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 04 Mar 2024 21:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 04 Mar 2024 21:21:28 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Mon, 04 Mar 2024 21:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c8f08144ec2f1d4930dac19c884f840d985fd33fc70c2256a0fc8f0a85652056'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha1-linux-aarch64.tar.gz'; 			sha256='70f98026a210dfddd1a143145703ee6e2fb5eb9063a280e2d710eda0bb925d8d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha1-linux-i686.tar.gz'; 			sha256='511df786cf4e75d290bae6fcb2ab0d25c94482058690cb424934117993bac21c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha1-linux-ppc64le.tar.gz'; 			sha256='c731dd05ef3aaa9245dd860fb8ec2f3df65035107fcd1179b113584b13233f91'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Mar 2024 21:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Mar 2024 21:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e993ca4a8550076450f04fe5b82814dd5b207ce5fa7cd3dd4d831c918e37bec`  
		Last Modified: Tue, 05 Mar 2024 00:50:17 GMT  
		Size: 5.7 MB (5707905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3c614bf83d4662444921d7dd80c420979fdac880928b9db7d079677bda2561`  
		Last Modified: Tue, 05 Mar 2024 00:50:20 GMT  
		Size: 248.5 MB (248532404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7874401bf4f943e15603e0a208f62c92bbd2467ae0eb7852b4c3fde92da20a`  
		Last Modified: Tue, 05 Mar 2024 00:50:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:c9115a43ef91faadedb9d4bafb7cd17f198335724f20dd5639d736331b3ef10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2482782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcbde375e18a9a7931576c5891cdf52bae09fe1fcfb2326b6dd9c4e36e05c97`

```dockerfile
```

-	Layers:
	-	`sha256:5b1d5ac1380ef3257c61356f1919b2b97e3311f68b52b201ced3997ee9148781`  
		Last Modified: Tue, 05 Mar 2024 00:50:17 GMT  
		Size: 2.5 MB (2463849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8adf6ab37bb30d141d821b44c8beae20b219b683ff4c53ebb44f48322a6736dd`  
		Last Modified: Tue, 05 Mar 2024 00:50:17 GMT  
		Size: 18.9 KB (18933 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b934ddf749d170355f3f92cc63926c9418b7d84c9a504de9883a7dd42017983d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198881174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3cd44f11913a2bd0f54a07cc2d99bbd95c794aa09edf2b5d6b786ded6a3b45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 Dec 2023 21:28:57 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["bash"]
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 18 Dec 2023 21:28:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_VERSION=1.10.0-rc3
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc3-linux-x86_64.tar.gz'; 			sha256='cb68ef2ebff2cfd18c1cba2c1ad8f37e73685ae6a24dbc036dfc86b2e13e0a18'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc3-linux-aarch64.tar.gz'; 			sha256='dc0baea6e9a7a1ec608b641d0658f1621a471b602b13a0facb72e0b83ccc8e6d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc3-linux-i686.tar.gz'; 			sha256='ac6938aab1d824029bf60959f80c3da7bbb5660aa32e9e97a5f7269a5c5c3986'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-rc3-linux-ppc64le.tar.gz'; 			sha256='45a499f7de8fabe5321469d3912a1b9bcddc15b3ddcc6c1671a5754f36a0e2e9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc3?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6501a514e34255056533f9f676190a58e8605094f7bbf62c066f33e5e2013a7c`  
		Last Modified: Wed, 20 Dec 2023 10:12:45 GMT  
		Size: 5.5 MB (5533257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381836b385d64eaebcfd52e5ea8c228ee583380665d11cc3f2a5e6cf024868f0`  
		Last Modified: Wed, 20 Dec 2023 10:12:48 GMT  
		Size: 164.2 MB (164190274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba459915073f1aeafb46601e033fc7e4ea31de0fe07be32d3c106dee6ac055f`  
		Last Modified: Wed, 20 Dec 2023 10:12:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:4c31c522fbe14a526ac376ca7d9f786d41540d9c3084f59200f9f04bc255eeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876256faf2c553e268762bb53482e1fa58a8bf79aad89d03fe362dc36d9fa9ff`

```dockerfile
```

-	Layers:
	-	`sha256:9108c8af433a3c508b9c5c9888d1895212a6f1cb1c4b3c3d80d5d6322702a51b`  
		Last Modified: Wed, 20 Dec 2023 10:12:45 GMT  
		Size: 2.1 MB (2102396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbce9cbffcde90ed40091f565a7cfb5d657bbae522dd25486bca57ab0c4b783f`  
		Last Modified: Wed, 20 Dec 2023 10:12:44 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:bfa0ca5f18de7c4b19dd3b009f860ab2502a6a10f5c5213fd6f84d949164e03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192438898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4a73b47ea7779e4e0480cbb2f3288965ad0fd32bcefd6fa18216bbd713e809`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 Dec 2023 21:28:57 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["bash"]
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 18 Dec 2023 21:28:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_VERSION=1.10.0-rc3
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc3-linux-x86_64.tar.gz'; 			sha256='cb68ef2ebff2cfd18c1cba2c1ad8f37e73685ae6a24dbc036dfc86b2e13e0a18'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc3-linux-aarch64.tar.gz'; 			sha256='dc0baea6e9a7a1ec608b641d0658f1621a471b602b13a0facb72e0b83ccc8e6d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc3-linux-i686.tar.gz'; 			sha256='ac6938aab1d824029bf60959f80c3da7bbb5660aa32e9e97a5f7269a5c5c3986'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-rc3-linux-ppc64le.tar.gz'; 			sha256='45a499f7de8fabe5321469d3912a1b9bcddc15b3ddcc6c1671a5754f36a0e2e9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc3?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570efb79313b383c2f2fe18f56e4de718ea5b7b7f3c983d8b89db058155a1589`  
		Last Modified: Tue, 19 Dec 2023 03:47:56 GMT  
		Size: 5.9 MB (5862451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658d394c23609e9114e3f98eb52338c21e53eb7e41dd4e6378b9b6f48c38575b`  
		Last Modified: Tue, 19 Dec 2023 03:48:01 GMT  
		Size: 156.4 MB (156432214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7b4f78b60bbf59966eed71512ba1ba0e8c6db2ee02a6c247cd8653620b62ca`  
		Last Modified: Tue, 19 Dec 2023 03:47:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:247b952ee787577d687d0777b04939f1b5c980cbb09f9bb4673183270f1135ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31434b23b55747a575417fdc82a49fc1fc45fcf80d798093dc34bfbb0149bcd4`

```dockerfile
```

-	Layers:
	-	`sha256:6cfa17f8f458f24c7f3091545f8a5f0bce84f8be30aecea6f349aae300268e9e`  
		Last Modified: Tue, 19 Dec 2023 03:47:56 GMT  
		Size: 18.6 KB (18613 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; ppc64le

```console
$ docker pull julia@sha256:76d496c94b34bd23018ce3e69d0e60fc40e403483e0261d75d1403fe6c82c457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193264910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d2a5bb2bff6c8fe7a201a181749562256001c2dadce72a8ee07c57713e0db1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 18 Dec 2023 21:28:57 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Mon, 18 Dec 2023 21:28:57 GMT
CMD ["bash"]
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 18 Dec 2023 21:28:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 18 Dec 2023 21:28:57 GMT
ENV JULIA_VERSION=1.10.0-rc3
# Mon, 18 Dec 2023 21:28:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.0-rc3-linux-x86_64.tar.gz'; 			sha256='cb68ef2ebff2cfd18c1cba2c1ad8f37e73685ae6a24dbc036dfc86b2e13e0a18'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.0-rc3-linux-aarch64.tar.gz'; 			sha256='dc0baea6e9a7a1ec608b641d0658f1621a471b602b13a0facb72e0b83ccc8e6d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.0-rc3-linux-i686.tar.gz'; 			sha256='ac6938aab1d824029bf60959f80c3da7bbb5660aa32e9e97a5f7269a5c5c3986'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.0-rc3-linux-ppc64le.tar.gz'; 			sha256='45a499f7de8fabe5321469d3912a1b9bcddc15b3ddcc6c1671a5754f36a0e2e9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.0-rc3","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.0-rc3?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 18 Dec 2023 21:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Dec 2023 21:28:57 GMT
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
	-	`sha256:3e0aba37b5da6c21f5a738f1a2ba5aeee1c1a46bf5a9eebd3594c5d79c063683`  
		Last Modified: Wed, 20 Dec 2023 08:34:50 GMT  
		Size: 153.9 MB (153904739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec50fb7c378640fdaac6b4ad9cf181ffe7b13af8f4bcd6e6dc90b2f42b75ad51`  
		Last Modified: Wed, 20 Dec 2023 08:34:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:7f62df7a4371fe38f2eb2ffd35bdba4ba310344a1b4b0d36410b431078a594f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb3e0da51958786cac74d2ab466356f43d0bd30ca6f8d420d8ef13e55e2073c`

```dockerfile
```

-	Layers:
	-	`sha256:fb2b88e1830dd961fd0166923a1498dae54e3d852b7af42a94596b1121ccb1cb`  
		Last Modified: Wed, 20 Dec 2023 08:34:45 GMT  
		Size: 2.1 MB (2106582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d2f6b2cbd8be21efae37b33884c91d0f27b54b4873d30e8536cdadd63d0027`  
		Last Modified: Wed, 20 Dec 2023 08:34:45 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:9d761d11866209d1e3a2d0d9e6a0210d283ec342f8973bd2876c188fcb3485fe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207257959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06deef0d9fb6d025a04ae5a1e69755b17909f62291c54b6002b8113f3a17ff98`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Tue, 05 Mar 2024 00:49:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 00:49:25 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Tue, 05 Mar 2024 00:49:26 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha1-win64.exe
# Tue, 05 Mar 2024 00:49:26 GMT
ENV JULIA_SHA256=f7479a8164443bf5e96809dc11140755b0b3f3a1c5f23b7fb9a57404bb357f86
# Tue, 05 Mar 2024 00:51:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 05 Mar 2024 00:51:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3d5c4e8e9d5c68f14619c9473e7a0980a18a154b45bfd3c92116ec199db24d`  
		Last Modified: Tue, 05 Mar 2024 00:51:53 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f977e6ffeabc521e2e0331155beff62216cbe683056ffad1549019ca044843`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b2ac6af3f3bdd4b2c9e9856bf175bd2e01671e0bdd212aa497027dec26992d`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09733da4e960ac74550144ce5aa85f4d4323a20fde1a42251c94d176d5eeb09a`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d981cdb3c5dc9158ed6decdaf3bbbd826d79f03cddf626bbfd1369a683088`  
		Last Modified: Tue, 05 Mar 2024 00:52:28 GMT  
		Size: 296.6 MB (296597317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4523a317f402256d0545ddd207df63296f3cf089668bc63008bc5c3a0c8a47`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:cea660c15a848c7a7a58ba5045980dcc9a7582ab9f3b1c2b4b99281d54c80134
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377069053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beefb4e7e9413e7e8661a2e864e7beb812357840e4a7f6ddb149104ee81eb60f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Tue, 05 Mar 2024 00:49:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 00:49:44 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Tue, 05 Mar 2024 00:49:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha1-win64.exe
# Tue, 05 Mar 2024 00:49:46 GMT
ENV JULIA_SHA256=f7479a8164443bf5e96809dc11140755b0b3f3a1c5f23b7fb9a57404bb357f86
# Tue, 05 Mar 2024 00:54:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 05 Mar 2024 00:54:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba734caaf951fbcddcca1173f7c6d2a2c10b8c975120cfec4ad6184b8e23ae4e`  
		Last Modified: Tue, 05 Mar 2024 00:54:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5649c7870d40bb6f72231f37c29a3ff52c51d41d8be038eefe96f4862686258`  
		Last Modified: Tue, 05 Mar 2024 00:54:56 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840f5064ee99dec175caf6b7e45beb818bba3b7535a4bd30eb63df46eb2c4201`  
		Last Modified: Tue, 05 Mar 2024 00:54:56 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a2761a2c54e0edc097bf76fe50a847c085f75e9fe0352b270f0fae92d2b983`  
		Last Modified: Tue, 05 Mar 2024 00:54:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6236f37d5e1a6524073c927d96d621629aa1cd39fa45bc1bd3bff556770db114`  
		Last Modified: Tue, 05 Mar 2024 00:55:32 GMT  
		Size: 296.6 MB (296613796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a220b926ffdefcb7b34974ed1951d630142a590f5958977fbb830c6de807a49`  
		Last Modified: Tue, 05 Mar 2024 00:54:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
