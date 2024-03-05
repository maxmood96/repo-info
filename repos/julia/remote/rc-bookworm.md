## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:22ecac122005c44423c0c7c4411ae18c639259e219c3733841294eed3d0f717b
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

### `julia:rc-bookworm` - linux; amd64

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

### `julia:rc-bookworm` - unknown; unknown

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

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6fed723d857f92b16d1c4529337644a7e7558016c1f40e537a8366cf91902911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275784246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91b1836c5dd6fcc392f66453b6dc92842f5607088d9d2a95bf275b6a7a6a3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
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
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14e605bd6638a1976eeb8d1cde59556a1f77295bac46d1669a9e27e6cd0ad6`  
		Last Modified: Wed, 14 Feb 2024 00:40:29 GMT  
		Size: 5.5 MB (5533149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7321bfe20b0efb46d0df765c82d61d74dd86eca45f0f17ce850f029009fe4d3`  
		Last Modified: Tue, 05 Mar 2024 01:52:26 GMT  
		Size: 241.1 MB (241094361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63432f245ec8be03a2885507f7e3f074b0fca36c72e78f6716a6fce7f3fd0790`  
		Last Modified: Tue, 05 Mar 2024 01:52:21 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9cb362e2b14aaee1bf31a0f2c01f20e4790d087e1511ff27a8d852a9a56bd2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2482862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88226ca3e1c5c09141694afc51178ea16338cc8213d5c3629518974635811deb`

```dockerfile
```

-	Layers:
	-	`sha256:e0ee88b0bad367c527db9971ba9a4d7679b7b80c6d2b5684dc7ce8e7d6d75075`  
		Last Modified: Tue, 05 Mar 2024 01:52:22 GMT  
		Size: 2.5 MB (2464082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2583186685d6ae269d1622888f1455e2e86adc2fe49c28ca50b33c7521d0c10`  
		Last Modified: Tue, 05 Mar 2024 01:52:21 GMT  
		Size: 18.8 KB (18780 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:7d9089ca8a1e809364728044a05f67b7f31af662fdaaf8fdf89086660aa05425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266511786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc28dbc2257c5349ea5ed21fcd072a9da71b8f952e88f8f318e0549305fad00d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
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
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb551e11aba4b34b48f026ca1713b7d432131d88e232cd0bd4f6eab6ee46744`  
		Last Modified: Tue, 05 Mar 2024 00:50:26 GMT  
		Size: 5.9 MB (5863274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa52f68e6f3c561a9901e7009da1cc37a663b71931417d09f7938069735c230`  
		Last Modified: Tue, 05 Mar 2024 00:50:31 GMT  
		Size: 230.5 MB (230506334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c680792c0068b5eaf2ca290f5217911a23f699a3be5aecaaee87ec1279d749c6`  
		Last Modified: Tue, 05 Mar 2024 00:50:25 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:6aeb818947f095be139c230d3648d4c2bd0cb034be9285e1d21220dbae6f6547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5648b059a60f8604f5897f2ae61ddf0724cfddf608bcfeffbc86e043cc7bc0f`

```dockerfile
```

-	Layers:
	-	`sha256:e0e114ae57149c79de2c2777b9c23d736d5f2c5553bcacee8a4c2148d94ad34d`  
		Last Modified: Tue, 05 Mar 2024 00:50:26 GMT  
		Size: 2.5 MB (2460931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0283ed41e13bd87eed3eb486377ddb727a2dab39473d273d0be231862b30ae5a`  
		Last Modified: Tue, 05 Mar 2024 00:50:25 GMT  
		Size: 18.9 KB (18893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:76748d3f26258919d52c1683304be8cb3ecd2c50fcedaacb56c1d3534d12a334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280472468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541665caf914e5cf346d326b0c34f95ba1487b13c78bcf395d99c60dd07a05a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
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
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a48b566372cb4fa0fec129e803c39a28de529b9736fd03a42344641249c1fc`  
		Last Modified: Tue, 13 Feb 2024 21:54:44 GMT  
		Size: 6.2 MB (6239799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be588cf8cd90b014d52ee7217ef5c292ea9dc363317354e162086e67aac206cb`  
		Last Modified: Tue, 05 Mar 2024 02:21:40 GMT  
		Size: 241.1 MB (241113392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2df14f53f96cb571b1198fbe8d60e812406347c380bd68483e97ddd12ed684`  
		Last Modified: Tue, 05 Mar 2024 02:21:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:215fbde4ae31ccdd5d5ee5e5b7c28806608faf7d54faacf9dbd9b571182c8419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2487087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bee39c5518f3bde149854498c8a567edcdb4d6c0f4712150182c6fd2870e130`

```dockerfile
```

-	Layers:
	-	`sha256:6061541e83ad571324171e97dad92c5d56ead800c64abed55480d3ea12ae598c`  
		Last Modified: Tue, 05 Mar 2024 02:21:34 GMT  
		Size: 2.5 MB (2468268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69015bf820d249d3589bd03a1876a2280fff0eabf1be1abd8b8d8e921f7542fb`  
		Last Modified: Tue, 05 Mar 2024 02:21:34 GMT  
		Size: 18.8 KB (18819 bytes)  
		MIME: application/vnd.in-toto+json
