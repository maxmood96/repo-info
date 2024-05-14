## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:adc887dcc3de95d4072917819de859904fdcee99f8d1ee0068c10c77bed86ef9
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
$ docker pull julia@sha256:df95a03d6be4dc85df19528ab4cbfc978c27308677de713af0aa0ffc5572fd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291783768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94c31986d693ace3070160a753c0ad743dfb8335fdf7e6958dcd88ef0c34dbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 21:26:13 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 10 Apr 2024 21:26:13 GMT
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
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a64d8285a042faa89919cf6b0ff7620b5f54afbd2839e6d81a02cc78055c21`  
		Last Modified: Wed, 24 Apr 2024 04:56:19 GMT  
		Size: 5.5 MB (5515102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692f75c4471526bf845dfd27ea05f24c45fa8a2a8312cf68f31688818b6729d8`  
		Last Modified: Wed, 24 Apr 2024 04:56:24 GMT  
		Size: 257.1 MB (257117812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442ed9266bf0b3895ceddd20bc6767b3076817d1410918b593950624847f5f00`  
		Last Modified: Wed, 24 Apr 2024 04:56:19 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9a3038033d783aee40cb909b66632a266b4e7b1fdbd36eebbbe0229d76b4ac97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2433005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662a4917bd2f38630d789dd1b0df2283c32af760d303e5fc0c21a2af66d6a728`

```dockerfile
```

-	Layers:
	-	`sha256:87111efd42ce5a58bef361994a41d64089aa8dff87707245fa7df6fac474043b`  
		Last Modified: Wed, 24 Apr 2024 04:56:19 GMT  
		Size: 2.4 MB (2414087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7ae69a695ea14b2b59a38ccbf7fe95c4f52b6765b883c861f2de5b0e28a3bb`  
		Last Modified: Wed, 24 Apr 2024 04:56:19 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:90d96262c6bd6a8410ee11e36010435d3c821afb9f0d1d5b91c624bf6196d931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290150800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5f99be0175aff9335b10f8fb7d482f9f7ac5fcb91fe92f1d19dbdad88436cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 21:26:13 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 10 Apr 2024 21:26:13 GMT
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51eba2041d7f36f97184723e7f3ea3756749f4d0321ba12afb498a4c9eed6ae`  
		Last Modified: Thu, 25 Apr 2024 07:26:42 GMT  
		Size: 5.3 MB (5339347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f2a7526aa3452a826f240d9b8cc7fb95dd74447b7f4032177559b8b684dc97`  
		Last Modified: Thu, 25 Apr 2024 07:26:47 GMT  
		Size: 255.6 MB (255631144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9c0c48aa7078ba0e930bfde66d53bfd5eec406796b97d54f12165770c9224a`  
		Last Modified: Thu, 25 Apr 2024 07:26:41 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7123c3a47bcc975c60780ed8e91c6bb6bb98db0231be3b34eb987e72b39850fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2433086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eecd79f8a618d2d8483b2041a5a93a9e1a540782fa5e2b4a5ba55c9cbb459ab`

```dockerfile
```

-	Layers:
	-	`sha256:88eb2219f748639c4df9e39068da9ebb10ec753848bf8ebbeaaaa3323f1d1528`  
		Last Modified: Thu, 25 Apr 2024 07:26:42 GMT  
		Size: 2.4 MB (2414320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c344c89d5663471822f404bc3cc39e5929d31b7f67607da19934280f2abbdf47`  
		Last Modified: Thu, 25 Apr 2024 07:26:41 GMT  
		Size: 18.8 KB (18766 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:7de71352a6e0ec33010c09d999b5eb9ce4f10bdc2c4f0699f3fee1f12a393d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270369928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d66ee8e24e651871d24fe563802e708d24c463894a4910296de5c0bebd3364`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 21:26:13 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Wed, 10 Apr 2024 21:26:13 GMT
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
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671402a8a0b687d79ba07fe71015177811471a4be11ba6bf041066194bf40dab`  
		Last Modified: Tue, 14 May 2024 01:54:10 GMT  
		Size: 5.7 MB (5672063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8f133c959e8cf38c4dad9f2163bb9aa6dc6800cf1d42168a893e8da2a9334f`  
		Last Modified: Tue, 14 May 2024 01:54:15 GMT  
		Size: 234.5 MB (234534857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80436fecc4c9bb0efad561d28baf2766dd246fcda4dc119ad9d92981e82a3ea5`  
		Last Modified: Tue, 14 May 2024 01:54:10 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a5157ff708a176ab1e2be043eb5f5ab6782522e01d88ca95da9c7e0ff7cd30a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5296b2e95c30282d167bb740ff9dcc12d772cecfd7245e5f50208127c35ad0`

```dockerfile
```

-	Layers:
	-	`sha256:591bad028ae0ff95fa980330a1388ecf2bec6def33aaeb4da01e78d849052706`  
		Last Modified: Tue, 14 May 2024 01:54:10 GMT  
		Size: 2.4 MB (2411169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5d3f56a91d6b369dafbf33574f9a1ca3fd278735228abb51363ab1c471d720`  
		Last Modified: Tue, 14 May 2024 01:54:10 GMT  
		Size: 18.9 KB (18878 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:4f44a70b4056e785918516077d52e980b93b8e72d3b541fe285dcf72c470f1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 MB (283973320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b14701bc104d31b6255c2dc353cdbfb18333eecad2727190aab1acdf48ff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Apr 2024 21:26:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 10 Apr 2024 21:26:13 GMT
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
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9168884d232cb41cb827526158c4c1a00a14bdc631054304c37506210cb72`  
		Last Modified: Thu, 25 Apr 2024 03:24:02 GMT  
		Size: 6.0 MB (6047078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bade72b1cecbb99c9df2549e2c91a37970088177769e14d455d9f02abdc42a`  
		Last Modified: Thu, 25 Apr 2024 03:24:08 GMT  
		Size: 244.8 MB (244784665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0bce3230a9ead3ab0dd8f8c2072e7e222a4491d6ed399fe4554436924a6bf6`  
		Last Modified: Thu, 25 Apr 2024 03:24:02 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:72ad1e3d06fdf1a21cbc12f0e7685f6b11bb64f74c9694e59c0121413f81faa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43ef069118600b47eb09ff8b67f96d363c7f7ab7a277072942faecf2e2b988a`

```dockerfile
```

-	Layers:
	-	`sha256:239aebf9ca1a6e8364ab22754cc23e6c2ea67f459b65df5a1f6773cd65b17d10`  
		Last Modified: Thu, 25 Apr 2024 03:24:02 GMT  
		Size: 2.4 MB (2418506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13c2c7a1b73c77437e4591f379ca23de898afa22e3b0627a1c57e0a41bc2789`  
		Last Modified: Thu, 25 Apr 2024 03:24:02 GMT  
		Size: 18.8 KB (18804 bytes)  
		MIME: application/vnd.in-toto+json
