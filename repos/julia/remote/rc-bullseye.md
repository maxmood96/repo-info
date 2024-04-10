## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:28e15400ab93a7758afe3ca8853e091369c4ed95e79a64dd7e60dedc3faca16a
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
$ docker pull julia@sha256:7a7cd6a9d5912857459954252cd5b3278f02c7476878326e91820d07473fe5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290454493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dce835b885eac5924d22c8168e6f712b506c183c7823635b79bfa3d01e5b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 19 Mar 2024 17:59:39 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a2ca4ae4e70293b89278e96ca564623de7b7866535904c9547c4b639e996ac`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 2.4 MB (2426517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e06b42fa733e2a088b83c22df514594615c668172196bbcf7c4aa9eb6d1ad57`  
		Last Modified: Wed, 10 Apr 2024 02:54:42 GMT  
		Size: 256.6 MB (256599866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9aee712115f7670901f79e77187c391df6f00c6b788a80cb25a0aaba50d6f0`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:e73eec13e633645acab67dfcc46f6ee3793972543799e06e3b5ae46db1beccfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1f0f78c67c7e95cc2608e47a09b83d537306db91be4dad6b6fd5c43f829926`

```dockerfile
```

-	Layers:
	-	`sha256:97bcbe82f39761e2ce4ab3dbfcb5acb3ef862c2da53a0a3652bc5c5da4eb7fd2`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 2.7 MB (2680971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba2ad33d186a7aa207194c2874e9db14e156c4bb54a484a55f672f8c7437eca`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 18.0 KB (18038 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2c504859e2557b2ef6b294923294c6e6b27407444d832fb27baded12d26b3e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287761612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4798ecc13b48cd489cecad86e232d7b00320c6b86efe90326410d637692342aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0227611e4e2f2ed1bc31e745947af460850a005d1306bd2e48a92d6e9d2e05a7`  
		Last Modified: Tue, 19 Mar 2024 22:53:34 GMT  
		Size: 2.4 MB (2415010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ab18103f28655d151c06fbbaa1004320c237d453ced640268830e74262e1a0`  
		Last Modified: Tue, 19 Mar 2024 22:53:39 GMT  
		Size: 255.3 MB (255275112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f48920d951b61114f21bcf45d58e7001aebef3a906ff1ca3efb5bcaa7cd89b`  
		Last Modified: Tue, 19 Mar 2024 22:53:33 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:029ae53ea4d47f28c2fe2c8ef7c7454c7d8a61ee4de289d096891f5dce0fffb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1550bb3a74658d53fa296488ce1a7bf2889b5c310d4d6be2f9fe341b3ad89522`

```dockerfile
```

-	Layers:
	-	`sha256:5bc27b95a360e7f6138ee6a2a94a947fd40086e9257ad6c5f9f702faa562384c`  
		Last Modified: Tue, 19 Mar 2024 22:53:33 GMT  
		Size: 2.7 MB (2730819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea45f6e0c5791f54a0e81af3a73f3ef905bd2fbf20ebb972a0bfc98a9692c41`  
		Last Modified: Tue, 19 Mar 2024 22:53:33 GMT  
		Size: 17.9 KB (17878 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:c4853ddbaa5d2229fb539028615184a8f14b4ca4ec902bdc2a2f5b1421a04540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269385854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d287cf8542f52c3114abf17cc054c4c6841db2a7349278204e4fa18056df5bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 19 Mar 2024 17:59:39 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd9f214927c86ccda5bf3e8cb0bec91a6f4caa5783f7bc864406425e49b32e`  
		Last Modified: Wed, 10 Apr 2024 01:59:35 GMT  
		Size: 2.5 MB (2533046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893e53ecc8b2f9b6fd2b3f3ddc9d487865475818017acb9187a14ac7179f18b0`  
		Last Modified: Wed, 10 Apr 2024 01:59:40 GMT  
		Size: 234.4 MB (234439019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad131b4645933d319a2d7cd783bc9d75c1c561dcceb36b256a0da81904e11f56`  
		Last Modified: Wed, 10 Apr 2024 01:59:35 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cb1f2f319ebb7954b338e3e34582c4b119c03fd3d8ce3dbb8a22b5f18730b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23258d2a28cf9ce58af5efadd1351d055c108e83d39661e7a9e0124aea518416`

```dockerfile
```

-	Layers:
	-	`sha256:1ecb6f3f9329be16d6bf119d9658c88bfc9aed92e538bc46aec0da3383593a6c`  
		Last Modified: Wed, 10 Apr 2024 01:59:35 GMT  
		Size: 2.7 MB (2678076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:742ac92dcb4333ce30cc01c332756443e79025ac033892fd557dd2cebe31a5c8`  
		Last Modified: Wed, 10 Apr 2024 01:59:35 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:9811e880d7c2ec025ddcca4c1f0e78d88e2acf33ce233d0dae48f52212a039d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282252536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2629398988deb73a9970f1d2eaa1543399b1ae9cf9ab3af2811bb38de08bf3cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bullseye"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e1fb7608c59d02dc41a5338305aede2caccd4fe0dd43bd288659af5ae8ffc`  
		Last Modified: Tue, 19 Mar 2024 23:15:21 GMT  
		Size: 2.6 MB (2630024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce4a5969b06e3cae97d2429abf293b1b51370ee00841a61606468aa387e1a7`  
		Last Modified: Tue, 19 Mar 2024 23:15:27 GMT  
		Size: 244.3 MB (244324132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e9f8eb4255de8dcd6fb9b1cab4ad2fcf6df7fe66e7674919e0d2881fe0a847`  
		Last Modified: Tue, 19 Mar 2024 23:15:20 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:16f0496d9ee81df7dddaa72f3dfe7fc1bced65a74b442df7e699ab73aa3b3143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5220a021b5cf05848eb0af7384360533b33b7af39708e800fadb604b580556`

```dockerfile
```

-	Layers:
	-	`sha256:688279ba8207ff483f6fb24fbbffd4d19d7eaa383612fb4b2e473bb64ba92432`  
		Last Modified: Tue, 19 Mar 2024 23:15:20 GMT  
		Size: 2.7 MB (2734993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4038f3a290df2e79e1abef0501d1478f13bc2670395fb7e2319fc72242b954`  
		Last Modified: Tue, 19 Mar 2024 23:15:20 GMT  
		Size: 18.1 KB (18072 bytes)  
		MIME: application/vnd.in-toto+json
