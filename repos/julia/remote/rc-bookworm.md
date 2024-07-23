## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:2e7ef3d4f3a8ccd7a7c68fe09d14e04524c33e22a4817395ec22172be5efa4cc
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
$ docker pull julia@sha256:e248836794ce02a3d401165b1839c614dba82e29e9b95ea216c1e1299cbdf319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288410504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf61456345b6c0e04d33116783e3fa412e28fac306087a54c0af2511cdf1d512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b5771f4fb24bec49cef28b688dd6753cadd532b9d16bf7d90d1ecc12b37f4a`  
		Last Modified: Tue, 23 Jul 2024 07:15:16 GMT  
		Size: 5.7 MB (5711035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf6e399b84b6c95b9fb73e7593968d6ddc0b544e06d10b5aabd5bd154b311a9`  
		Last Modified: Tue, 23 Jul 2024 07:15:21 GMT  
		Size: 253.6 MB (253572814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1247b918f11e4c9241b8efaa2dd1ab232b8ed8237a6478a92c1d91be6b0024d5`  
		Last Modified: Tue, 23 Jul 2024 07:15:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e5a1a65b9d3da327d74cc5a025d212630526d4feddd823f0424c905ec3a05d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e44156075bcbc56bae8133e4d240cb50d5382fed01aac5385fd6df429f904f`

```dockerfile
```

-	Layers:
	-	`sha256:825e4e8411bc055474986e747dc3cb87df9a6b4f11bd146b89ac519888501f8b`  
		Last Modified: Tue, 23 Jul 2024 07:15:16 GMT  
		Size: 2.4 MB (2435044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ddb8b24ea9d99dfebbe47382c726befc8ce238974fc17a7b712ec2f9154444`  
		Last Modified: Tue, 23 Jul 2024 07:15:16 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7c141af2e6a495f293b1f045cef57aae0d6a47dc391f130389ac60fed28b7df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286767719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20679f5c1dd9503603728a3ff308c5170620ae66eee2f79d7a69efd888f092f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37493fa9d7c09883d911c2af05afdde26fd161359c14cf034cc9a7a7c0972720`  
		Last Modified: Tue, 23 Jul 2024 18:17:07 GMT  
		Size: 5.5 MB (5535885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0da2b640ff3704ecbcddd917ce36812ad1c056b8bdef8cd533bebb3d545b8`  
		Last Modified: Tue, 23 Jul 2024 18:17:12 GMT  
		Size: 252.1 MB (252074892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffdc1157adfbac463005fbefdfca7505a4d64d47e3ece72e3887c63bf255ed4`  
		Last Modified: Tue, 23 Jul 2024 18:17:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:4066da3d913eca5eba508b4cc2f1c5bc25a856eb48d6afbc667b9bb9254528da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6628ac61c0ab06032ae0428743b99310f7d29d38aaabc52e507052772afbe55`

```dockerfile
```

-	Layers:
	-	`sha256:7c6d682c326a8745eebceebe8b716a43d7d401e8ad5ae2ac126f93a368ef0d14`  
		Last Modified: Tue, 23 Jul 2024 18:17:07 GMT  
		Size: 2.4 MB (2435342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be325098ac46a3ce5f73020559e9164752c81cffe832c4e28b4df49e93bde704`  
		Last Modified: Tue, 23 Jul 2024 18:17:07 GMT  
		Size: 18.0 KB (18024 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:554e7bec8ea83d529545e9ce4da8bd02116cc7c9a4d4a8a73eac4045c6e533bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267292186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95573e321af192f1d620251f128a4ef275cc806d5fee995dcfac6288375b85c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8626b41ede939dd6c7a187de99b70d675c101cd6b6bbf5e14c84e0f7a3cc50b7`  
		Last Modified: Tue, 23 Jul 2024 06:15:33 GMT  
		Size: 5.9 MB (5867524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8325fc5649ac8972f5b4a56d04c6e5f9b74aa6dd9e70dfeccb05dbb9169868e8`  
		Last Modified: Tue, 23 Jul 2024 06:15:39 GMT  
		Size: 231.3 MB (231279983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d69cf9fe0c36728072ca68fa21cc402fab78fc8fd9bb62abfa4ba5ef420d9`  
		Last Modified: Tue, 23 Jul 2024 06:15:33 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7e0bc0d629cb951d90999c5cdf1562c999cebf79065d2b6fde871793b8326343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e311d9364fa2c66bf0cb4680ea923136e17b61c25699db977497fd438c7a00f`

```dockerfile
```

-	Layers:
	-	`sha256:d3450626d0c65fbde0402255f4550995f634c056eb5709f3a008702c3340b2e1`  
		Last Modified: Tue, 23 Jul 2024 06:15:33 GMT  
		Size: 2.4 MB (2432126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6376bb8cac9be0ce59004cb71544e54b847a41d3b34c3194104171a436047830`  
		Last Modified: Tue, 23 Jul 2024 06:15:33 GMT  
		Size: 17.6 KB (17650 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:b9d120bb85cbd6236f4e87f4f46ee3d4ef8ace668b790227d4a2b6c5cd8b81e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280948692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e17a72188c53e40947e38094f4cc45fcb8338696e013ed0f8ec2f5ee6082bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Jun 2024 17:59:16 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["bash"]
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Jun 2024 17:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Jun 2024 17:59:16 GMT
ENV JULIA_VERSION=1.11.0-rc1
# Wed, 26 Jun 2024 17:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-rc1-linux-x86_64.tar.gz'; 			sha256='d9d7ca81087185abbb8a375c41f734deea6ea26aef2dc40d99467f8c5c7cc8d6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-rc1-linux-aarch64.tar.gz'; 			sha256='192e6c92969a84b8f76e113286b81b166fe04a7c5ff6c6b44a73e494c9f7f3a5'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-rc1-linux-i686.tar.gz'; 			sha256='546aed60e6b6e5e5568562f299ddf1987d01f369f0243db0b8694ee83ced9809'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-rc1-linux-ppc64le.tar.gz'; 			sha256='79870070dfc7b283691199da017f5db9dc86a8ed2260acfbb34f7e12fa9af8be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 26 Jun 2024 17:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 17:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b21959807f2dcf24aabe6f0d1e03fdac442b5dacef6b1882329b1a39f88d5`  
		Last Modified: Tue, 23 Jul 2024 17:26:19 GMT  
		Size: 6.2 MB (6245948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2c5547f823911e3de9c0eccf6af19e74acc6bc1e1af8722662e17a568a1c0b`  
		Last Modified: Tue, 23 Jul 2024 17:26:24 GMT  
		Size: 241.6 MB (241580100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae86a43df7bd18a0d5bcae594002a198ac3fc43484ce0b9ac248283ae8ddfcd`  
		Last Modified: Tue, 23 Jul 2024 17:26:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7a84c80e56abaafa5ae8876a59f98672cc1b4718c37d2c597d03c05517bb7d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7398f3a6fba3f4f9d1fab3c703c2902f8b13c304a18910268ff309b5ebf0f6`

```dockerfile
```

-	Layers:
	-	`sha256:9a6469f0c13f67ab66819072e9bd369780ac72689dee72cf4085b43948c054ac`  
		Last Modified: Tue, 23 Jul 2024 17:26:19 GMT  
		Size: 2.4 MB (2439463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc247bea57521f14d2493421cd2a1843d02575ecfed20d351905dd8ed353621`  
		Last Modified: Tue, 23 Jul 2024 17:26:18 GMT  
		Size: 17.7 KB (17743 bytes)  
		MIME: application/vnd.in-toto+json
