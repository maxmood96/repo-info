## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:0f20c8055223cceb3e132d61f1d85328cfe1f82d3273c5dfaf55af4eca11eafd
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
$ docker pull julia@sha256:ba382321a19321b3c9ba276678b3814b7aebdd69b365aa1b7bac44f5beab7d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291957587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a786787632e4337753d31af1bc7921e2caa22181420278718d0e26d56c8d8c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1743b08a5934701887ee6dfde7cc4a310801aa63d609f2f18959aec95e2abc3b`  
		Last Modified: Wed, 10 Apr 2024 23:57:11 GMT  
		Size: 5.7 MB (5707965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfac2dac8f3d401a2208b5b67f134351669e5227b068fb3a2b534e46d31ee82c`  
		Last Modified: Wed, 10 Apr 2024 23:57:16 GMT  
		Size: 257.1 MB (257117896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830b0a11b310d40ed1b6e6a6e8beb15d4c6adee6fbc27dc21832b79582c94839`  
		Last Modified: Wed, 10 Apr 2024 23:57:11 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e8e8ccf735c21c8368140ffc6d4878b44d7c3720876a8368e924278105385d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472b12fae2b17328ac67aaec0f6e429deee05f19140a12e1e01562d89071bff2`

```dockerfile
```

-	Layers:
	-	`sha256:cdcd55cf781c6f5e9dcb47303466213bc1760a728f818a5d7dbd23226240fabc`  
		Last Modified: Wed, 10 Apr 2024 23:57:11 GMT  
		Size: 2.4 MB (2413957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190954513537853be9e72ac88d537946d137e3e43ce8e5318d681d00b2d3d21c`  
		Last Modified: Wed, 10 Apr 2024 23:57:11 GMT  
		Size: 18.9 KB (18914 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d38809a5170447c22e71919cbf02dec7410558cdb12b40e9a7391349fc8e33a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290326802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfc2f3f15b1338db6bb48d8e24230477f9240c160f86ed9060ab97296a379bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc2a70945b18a18ecc7929c1ec341812e2cdf8cdb6e7ba2322ae016299fff27`  
		Last Modified: Wed, 10 Apr 2024 16:32:06 GMT  
		Size: 5.5 MB (5533142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56246a4f21b1988a26bb7cfbcff1f4fa57e4169056725619de181cfb42906317`  
		Last Modified: Thu, 11 Apr 2024 10:26:24 GMT  
		Size: 255.6 MB (255631130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60902bdc8ace012673e3dc235b69f21ea8bcf4d52fb42a316217b3492359d51`  
		Last Modified: Thu, 11 Apr 2024 10:26:18 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1a8f4cd3b3f7522876a140d21d93a89c7785e507e9462b79177b47ef3c8cba80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3d6010bc43e8ea06f103e046e050204615a7bbf030c87bc6fa1726fbacaf4e`

```dockerfile
```

-	Layers:
	-	`sha256:6abb95c31ae1154cc9fe8c2e5bf78c98a810209849347f0e86c891cf15067218`  
		Last Modified: Thu, 11 Apr 2024 10:26:18 GMT  
		Size: 2.4 MB (2414190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c88848a8d0fbf1a8f2fe4c279a0084b3c0c5e78dbd874c16e6c298e34f94b39b`  
		Last Modified: Thu, 11 Apr 2024 10:26:18 GMT  
		Size: 18.8 KB (18762 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:aaee317df28b849d8105a323e7862f26296c58757112eec9d5cc18eabfb1477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270545123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0b5355d9277c80f727c887a52425a53543e068ebcc38627df6c7439c4bcfa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:11 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Wed, 10 Apr 2024 00:57:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847fad915e4de992ce2ff2b72d1959e87443c3c94ab83f6f7cae9e767067a85`  
		Last Modified: Wed, 10 Apr 2024 23:56:50 GMT  
		Size: 5.9 MB (5863333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ff7c7b7b2a2534026b9a0264725f719928d2556ec43f7d541d4b5c0ffb1da1`  
		Last Modified: Wed, 10 Apr 2024 23:56:56 GMT  
		Size: 234.5 MB (234534905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1837f7ab813f7eae56bd670c2a5d3dc302e3058de934b7e5d2dc0485e2e1000a`  
		Last Modified: Wed, 10 Apr 2024 23:56:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c78ad1c1d50727d26e533a258f3a6285edc77204c57dc7d51abc1f8fcd714254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ace71c27146966b77492b196321158c54fab0ebf72b5c1d22f94d92b308542`

```dockerfile
```

-	Layers:
	-	`sha256:3347ad45a741c6ce88e10e1a9e32b123b1573021230176924d1c0d976502ee70`  
		Last Modified: Wed, 10 Apr 2024 23:56:50 GMT  
		Size: 2.4 MB (2411039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a6fddf7dad82fbf489835dcc30a11bbf44117993db06f6c996d06c15a9fbad`  
		Last Modified: Wed, 10 Apr 2024 23:56:50 GMT  
		Size: 18.9 KB (18874 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:7c88b3a63797492466aae96265f2d69b7b6bc697cb1a0526cf7798e538cf52d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284149753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beaa5cb2181532fa48606fbc6d29437be1f1d34b7e3ac9e68ebcd903e7204ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:33 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
# Wed, 10 Apr 2024 01:26:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 10 Apr 2024 21:26:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 10 Apr 2024 21:26:13 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Wed, 10 Apr 2024 21:26:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-beta1","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-beta1?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Apr 2024 21:26:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Apr 2024 21:26:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b96ed25a10f7896c3ad5620aa31c084e86ad3405e615c048df790df0d494e`  
		Last Modified: Wed, 10 Apr 2024 19:16:23 GMT  
		Size: 6.2 MB (6239842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe7952f3fed2471a55b52f4f8d75c3b701d01bc4f2bd06258eb1f4c41719b20`  
		Last Modified: Thu, 11 Apr 2024 09:23:12 GMT  
		Size: 244.8 MB (244784705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54aeea280246f84aa6f8f1b72abd8bd55451f02e69aa10a5200d4b824210aeb`  
		Last Modified: Thu, 11 Apr 2024 09:23:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:668f67803fd40b15cb6886d98e5763c128b2e9568bb2452b0b51b1b2254dd38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2437176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625d7156e4723474bda1a6451d8f560d0fa6992a774526b99953f225aabadd61`

```dockerfile
```

-	Layers:
	-	`sha256:6967036dfed7e244aa8aa435ddb88787c14f1ffa9dcc0859aa6e6fc008720397`  
		Last Modified: Thu, 11 Apr 2024 09:23:06 GMT  
		Size: 2.4 MB (2418376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67217f9fff05d5be3e8a730d418877fb3ed115a903cfb69fa7a1619f85854df9`  
		Last Modified: Thu, 11 Apr 2024 09:23:06 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.in-toto+json
