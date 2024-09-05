## `julia:rc-bullseye`

```console
$ docker pull julia@sha256:ea414ced7a9404fa27dcd1735403469f454376ade98f18ba59bd0108926ffd55
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
$ docker pull julia@sha256:1b7248cbb6d7c132c9bb4badec3b37774390d819fbd89f87bbd297bfbd421986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (289043580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114f028ba672a81f998737d11dda4f87e345f525c409fdea2d38c3f38b931872`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184d357a9739b741df758ab3f1d6f55f2b9cccd9c41168f9d3d9af19c543a3e1`  
		Last Modified: Wed, 04 Sep 2024 23:10:46 GMT  
		Size: 2.4 MB (2426590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efdcba7735263a389baa917c10d08062a6006a8e6b99716c4523676099f5b39`  
		Last Modified: Wed, 04 Sep 2024 23:10:49 GMT  
		Size: 255.2 MB (255187940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3240991f61474505fec8b418e1ef7b9e7faf3bafbb28afe2239720a6d06219a6`  
		Last Modified: Wed, 04 Sep 2024 23:10:46 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:3c182a61db2a5b8719820d15071ac29f816ae19c93c6df1147f266d9a8cea89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0f8be76ac33ad746d64995b53d889f7e10319093eaf7f2f9923a9a467e07db`

```dockerfile
```

-	Layers:
	-	`sha256:ef3528c63723010ca66396f7c7c4035e3966066ca1cf31f561916f14ff5a82ca`  
		Last Modified: Wed, 04 Sep 2024 23:10:46 GMT  
		Size: 2.7 MB (2702845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7731066025a81d9a56ac4e921270d270550a8a0a405856994ef0401ef29ad84`  
		Last Modified: Wed, 04 Sep 2024 23:10:46 GMT  
		Size: 16.8 KB (16801 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e6ff1215e453ebea51e0ab9330fa95e535f1ae256201247fe9ea7eeee74d7b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.9 MB (285918965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce11e6e2b53b057ca16db33dfc9b1420a25ac9f72fe13d8f6e0248dff91a393`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa630b71e57d93c6c4a298a32f8abf58c36a28a92b39609f86ee56a5c299803`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 2.4 MB (2415117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820d4fa50588fdd9f70ddc85b2cdb4fb77e6938ae21ed0c34bbb8ad7db3f16b5`  
		Last Modified: Thu, 05 Sep 2024 12:22:48 GMT  
		Size: 253.4 MB (253429110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec59ded0e9682bb6b3c1a8bf8ab2dbd9371a8ee3506172e2c2c853693f697aa`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b08c03340f645cd23f7cef2e544576c8916a72a19baf4938d52e7fe006a0ed62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f402739348440a551f0e292ac8a605d414dfe1cf68c9160b9dc2878baf3141f1`

```dockerfile
```

-	Layers:
	-	`sha256:e3b4491894623dc9ff05affc4fc2f703b4ff2828f5b4b8f5c8c7bf8ddd333233`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 2.7 MB (2703095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7422b2ee823d968f6b8d4e9af7e7574bf8f0bf268f5af2fb4f1c4f246246b249`  
		Last Modified: Thu, 05 Sep 2024 12:22:42 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; 386

```console
$ docker pull julia@sha256:bcfe5d371cdd6f180b7f7e99089b82209c9393e0a086cea88192dc55348b4970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268932567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9896ec531bcac619cdd78bb48432f1edfc462a1b8f190e001ab28ce40218786b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f79d896d903469e0718f8b24e3f1c8061715fad06c33430cb0ff5c0f21c25a6`  
		Last Modified: Thu, 05 Sep 2024 00:08:13 GMT  
		Size: 2.5 MB (2533023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d9be22e22bab0a715017ac5a8b071821553d7c43c2237e16c4020bdf82035`  
		Last Modified: Thu, 05 Sep 2024 00:08:18 GMT  
		Size: 234.0 MB (233985859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad71696be123dbea08ed67d359ad7ed927e244c65809ee595e2a178880639c28`  
		Last Modified: Thu, 05 Sep 2024 00:08:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:338136f208db1c7786f714ecc633a5fe2a993e195c48558f7b2552d6356dbfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bcabc7d1d12936642129a6dcdd5e7d72b56acf1bde8f105381434caff9c6c6`

```dockerfile
```

-	Layers:
	-	`sha256:963b7cb23e9419d41c23492c051eb92e0e818b7689bf2c6ae1bbf0ba58961872`  
		Last Modified: Thu, 05 Sep 2024 00:08:13 GMT  
		Size: 2.7 MB (2699948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66be69868540ea4b02f6ef569617cbae6122bba581af673bf0d5a09e42f716a3`  
		Last Modified: Thu, 05 Sep 2024 00:08:13 GMT  
		Size: 16.8 KB (16775 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bullseye` - linux; ppc64le

```console
$ docker pull julia@sha256:8326ce7a337af167755f2a1f4aba0a905ada04f0a7c7d85b10d02e42f01609a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281938259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311684e8df932918ff285bd478fd6c506976de08f05e53f6d18e33fcbaa43c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 27 Aug 2024 05:59:17 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["bash"]
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 27 Aug 2024 05:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 27 Aug 2024 05:59:17 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Tue, 27 Aug 2024 05:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc3-linux-x86_64.tar.gz'; 			sha256='fc7e199ac4921a83150c2863425b203196436d12d8dc73054aeba5ad8a5d7d72'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc3-linux-aarch64.tar.gz'; 			sha256='5aff7e677a45dc7cf65c9ac7f2e6182083304e883a4ce33ab2d701915730c21d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc3-linux-i686.tar.gz'; 			sha256='4ca88a186b4b920c5693af8a5f36c2600c50e8442e84187bc6a3070eca785c28'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc3-linux-ppc64le.tar.gz'; 			sha256='f9a47e6bdfeff25b4df8b9e1b702e9a54da4248de13e927566505ee7dd5d4f05'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Aug 2024 05:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Aug 2024 05:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbb0c0469be47f8494a9cc686d3a871114819d6faf484d40a9aa54c23b8c5c`  
		Last Modified: Thu, 05 Sep 2024 00:36:57 GMT  
		Size: 2.6 MB (2629989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09625c2a2dae391bc1f387ba7da27f20d32e8ffd535b5af135a675626439ab8`  
		Last Modified: Thu, 05 Sep 2024 00:37:06 GMT  
		Size: 244.0 MB (244008622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a0182ad5d05c8ef8285defc1783794fab53c7843d0eb73dc91f5e37a9fc4f`  
		Last Modified: Thu, 05 Sep 2024 00:36:57 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1c720488fd2a7decacc28646f4eeb990b45d101993422355d2d7cb8661b48e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2724069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b335aefc249ba2bf92013cde05af33105f4205ff9bd9a3b9abb54b6c34596b4e`

```dockerfile
```

-	Layers:
	-	`sha256:bf06a3e009ddb331eaffcc4ee81d9b046881bd9c2253e07d155977376ef4a48e`  
		Last Modified: Thu, 05 Sep 2024 00:36:58 GMT  
		Size: 2.7 MB (2707234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc30210a4c154526eba6fe99700f77fb9ffc444a5cd72b12fdbe38e7d09b2b7`  
		Last Modified: Thu, 05 Sep 2024 00:36:57 GMT  
		Size: 16.8 KB (16835 bytes)  
		MIME: application/vnd.in-toto+json
