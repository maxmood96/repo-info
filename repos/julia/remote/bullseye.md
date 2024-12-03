## `julia:bullseye`

```console
$ docker pull julia@sha256:32b171825c642b18f3c12f1ee4c902a18d4d843b508347d7caa0039944e99604
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:0642d48c0d63fb78a423f8c26caa5c7293c7b3eb12186fddb2b6c6ba7413498f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfe48d89e02e4d7e6751780501d407fb9b4a68aa38cbc3ae72c1c77e9fee807`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72224fac3591a3f525c696689c52503a746c4ad547ba8f708a936a2a63962ab8`  
		Last Modified: Tue, 03 Dec 2024 15:33:52 GMT  
		Size: 2.2 MB (2222693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a61d81b54e769741e314a04623e794c9bebedc5e036ec0a82d3357189dc6f01`  
		Last Modified: Tue, 03 Dec 2024 15:33:57 GMT  
		Size: 288.5 MB (288487965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b6684c4aee8b45b577d6bd0f6ebea9c2805028d74ce3d8cea7996aec5b63d`  
		Last Modified: Tue, 03 Dec 2024 15:33:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:c80dcbd18f5aa39ac4db1cd13aeb8b44194b96860d1830e699d07f1e05fd26e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2769c23cd6172d465a5aa6599477fa2d9b2ac578f597336b86303dde630db7ae`

```dockerfile
```

-	Layers:
	-	`sha256:0c9ac2c41f19b325c780a49ab07fb1ed3f36190b69e2acf459803c439ec9d1e8`  
		Last Modified: Tue, 03 Dec 2024 15:33:52 GMT  
		Size: 2.7 MB (2715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4928833bb89eba86cbf14888cae730d0af6c7df2d09419313fa779ab3e8434`  
		Last Modified: Tue, 03 Dec 2024 15:33:52 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ba4cc6afb604f47b6aecae0707ae372f2daf7551887d2b6edf83dbedf3baf8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2925dad29f90af08799e4d36b6c7bdf52096d097607ea8973f5553e501254c61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7406cccb6a8da5b8107a16bee062c164ce21d4ebcc8216c7411ed76062d26e8`  
		Last Modified: Tue, 03 Dec 2024 16:18:03 GMT  
		Size: 303.7 MB (303658753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0c655483c497ed8681b389fb443531439375e2547f95a5dffad485c04591e`  
		Last Modified: Tue, 03 Dec 2024 16:17:56 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:dc30efccab9206461cf466449c7b26c3670726d9d276dcd6f48ee8b09522c120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107f6fe7d91957e097d76b2d58babab8163b81db795f8c8d4a309a6f4dab6be9`

```dockerfile
```

-	Layers:
	-	`sha256:22408e65d9f3655757cc327079878b50224f5b663d9b5ef98f2b82204b593679`  
		Last Modified: Tue, 03 Dec 2024 16:17:57 GMT  
		Size: 2.7 MB (2715422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a594def911dfaf3d944908cac8168cb59d4e01ebda4ea60f6e357a363cc159`  
		Last Modified: Tue, 03 Dec 2024 16:17:56 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:9b8757c787dabb7941367d61f0e082ee18857ecc72009b41aa056d2efb5b0067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f5defcbd298cdf6c425951e22ca822d07315cee387136a53a9c596d886348c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682c93ab78ec970fd7409692d15cb2229580e2ce49042fc80a870214aab02cc4`  
		Last Modified: Tue, 03 Dec 2024 15:33:46 GMT  
		Size: 2.3 MB (2328074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b53202900f8714abc2f98070e5fdb4c670eecba054d4aba7d71327ccccfafe4`  
		Last Modified: Tue, 03 Dec 2024 15:33:51 GMT  
		Size: 237.1 MB (237136276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb550c241f84365dd2587c4e7666676acf25fca298554963d8c29695a9c4c57`  
		Last Modified: Tue, 03 Dec 2024 15:33:46 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:a680d3b270181e24228a99e4cea48915fd9bc956b0b2fcdfdc1449b11d6ecfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfe8c304f754c7f2518035390064f149ccce905a2d609053d5fd03acba36f7f`

```dockerfile
```

-	Layers:
	-	`sha256:54822834a22ca6b5bda374096b7be9fc78a82890270c83a29b70c044ddadec19`  
		Last Modified: Tue, 03 Dec 2024 15:33:46 GMT  
		Size: 2.7 MB (2712258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a95ac5968934f0e54453c9f82255067cdd891a1617ae867e3ea223f425e119`  
		Last Modified: Tue, 03 Dec 2024 15:33:46 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json
