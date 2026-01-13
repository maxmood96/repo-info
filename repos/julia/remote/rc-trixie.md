## `julia:rc-trixie`

```console
$ docker pull julia@sha256:11cf40c310f8ee5bb33a854ed155c1a834bb577d8cf71638fce1ac451604fe22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-trixie` - linux; amd64

```console
$ docker pull julia@sha256:f1b1cd24979025371be317353d0d9071e9b549583d2b13783cbafd40b8d4e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342732091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890dff1fcd3df41639bbb9e3963311ccb58da0cc8fa8437b1f4c3bbfb5e5f399`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:23:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:23:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:23:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:23:01 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 13 Jan 2026 01:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:23:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:23:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:23:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddc565fb6a843513bb73bf64c3582ace063a3ecace19e9873d2b79646fb5d4f`  
		Last Modified: Tue, 13 Jan 2026 01:24:00 GMT  
		Size: 6.2 MB (6243805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bef83973c64d23f56a6007743eb5a2f7fd296bf363607ca82dc42312cced64b`  
		Last Modified: Tue, 13 Jan 2026 01:24:07 GMT  
		Size: 306.7 MB (306714231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39a73a7cf527ac8310b33a0b2759a62e665becdbd9fd9f5504b50f06c7f75a1`  
		Last Modified: Tue, 13 Jan 2026 01:23:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:09ddfe37c3d15662be7b01f77aa888e616d522833e7559517528c7b4c74692bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c9243bf5bb5f7faca820514dc6078bb776d92fd4a4a5ecefdea489574d46e2`

```dockerfile
```

-	Layers:
	-	`sha256:252a3e5031ea9d0a912662d2e6d2ba3a4c18f1dc04ae50cc7369d7ccddbd2338`  
		Last Modified: Tue, 13 Jan 2026 06:04:31 GMT  
		Size: 2.2 MB (2240881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e762d6799f54e9613121b25b6b7800dca98c68ca6316939feb86136f3bd5323`  
		Last Modified: Tue, 13 Jan 2026 06:04:32 GMT  
		Size: 17.2 KB (17205 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:86e7c43594e781879dcd8884c17e9a8c48d3dd89d2cf65ae870c1c4b025be251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (365998589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b251b9cf4a7e0a343e1335ebf584d1a3c4ad0a86365b2c403abe5836b012172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:23:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:23:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:23:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:23:07 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 13 Jan 2026 01:23:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:23:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:23:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:23:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e95377b83aabbd6f763ef195c9ee324786366766e1fea57cae26bc07d34ebe`  
		Last Modified: Tue, 13 Jan 2026 01:24:11 GMT  
		Size: 6.2 MB (6152121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f01a99ea345ed4be623092657ad4264eb370e8f4a762b95a89cf18f05e8a0a4`  
		Last Modified: Tue, 13 Jan 2026 01:24:18 GMT  
		Size: 329.7 MB (329712057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46306c283e5f7e3067f6d1ac7e8628e94ccdf96480d7131f9a96cddf1441b176`  
		Last Modified: Tue, 13 Jan 2026 01:24:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:4212b5eb776e8dec1517bfac31d990867442f90351dfb513422a8178da33f91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef482a269f84e7e0ae1f4262cf07b547e9cbf7ba8a550a26edae8b12b9d78fd`

```dockerfile
```

-	Layers:
	-	`sha256:4d6853c555d343b6f13d745a180a0596c22e79978330ffa39d0d0f369f6511d7`  
		Last Modified: Tue, 13 Jan 2026 03:05:39 GMT  
		Size: 2.2 MB (2241189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4cb16601127735ed2347799c075393a4e18afa34a4eb83cab32308fd13061f3`  
		Last Modified: Tue, 13 Jan 2026 03:05:40 GMT  
		Size: 17.3 KB (17347 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:cbba2638d46c50bcc4063316597bb2efc4240f0fafdb2e6004125e2675c37f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280237949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4e9a0c1a80d11e274315a2ffce74e7555dce4f250a4a8398a19ec584ff462c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:19:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:19:49 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 13 Jan 2026 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b50e9209c4344785009a67dd1a03fbb52287f46bc444ad8fa5e83c10550848`  
		Last Modified: Tue, 13 Jan 2026 01:20:31 GMT  
		Size: 6.4 MB (6429228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1322b2d2fd8dac3ddcc8a4d29920ca36a82a41c9562898fb28f8d6750dcfde30`  
		Last Modified: Tue, 13 Jan 2026 01:20:41 GMT  
		Size: 242.5 MB (242519875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05b0a1f278ed7c2d943193d46dd2747524187b75f4f415c553ce9cc38c9635d`  
		Last Modified: Tue, 13 Jan 2026 01:20:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:8732778092558756ca57d8a3a277ccdda1d0ee506c85f8536333bb87b0b7228d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7e866ae907163d312aab1d98249f0731f1a0ff8687033ba97bd517cd4b7490`

```dockerfile
```

-	Layers:
	-	`sha256:6d3dbe67e56b99df05ca104ad2e935b69c61674182e1c9cbd9afaf96f7dcae36`  
		Last Modified: Tue, 13 Jan 2026 03:05:44 GMT  
		Size: 2.2 MB (2238016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf3094a7c365babdecbcea18e2c48882b20acbb0d6be00a5eceacbeab4d5861`  
		Last Modified: Tue, 13 Jan 2026 03:05:45 GMT  
		Size: 17.2 KB (17161 bytes)  
		MIME: application/vnd.in-toto+json
