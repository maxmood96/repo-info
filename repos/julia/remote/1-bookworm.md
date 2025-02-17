## `julia:1-bookworm`

```console
$ docker pull julia@sha256:9a3828a03b1dd1cf67694ebb0202cd4ea8c304f3f452db729740873007524573
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
$ docker pull julia@sha256:114283193b251fc9ae3f17ed798a2e164356854704f370b21e89aef41f46ea18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302230906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cb41bc308d52bc59475587ba0a1f291e9f506ce8cce6f9d9775067159300ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039888be22b758bba9c7379295cffd633e58335768c0a405050c5ebae310ab35`  
		Last Modified: Tue, 04 Feb 2025 08:05:38 GMT  
		Size: 5.7 MB (5713127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4694607a6cbaead9f6d82c2efb45ce58ed40e112e602f40178e52499919c58d7`  
		Last Modified: Tue, 04 Feb 2025 09:04:53 GMT  
		Size: 268.3 MB (268305107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db043d709d9b2cd97087be40d1434ddd2bbb8c8e507054e9e976b91dfcb77236`  
		Last Modified: Tue, 04 Feb 2025 06:05:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b30b413bd07ade10ff8127d12cd4ccf9ee677365dd29bc1aa9a4ea9d0876349d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726720f5a7eba4e7a17af1502ede613e15f895136c4abbe771ef7f0fb3cba301`

```dockerfile
```

-	Layers:
	-	`sha256:b7f3589c0788c11b4145ba2689836ca15c2ca14e02bc7d7a6d373d2273d5a37b`  
		Last Modified: Thu, 13 Feb 2025 03:02:19 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a925c1b8c07e8eb89a4298ebadf891de0b747a297bc360010508e42f861ad0`  
		Last Modified: Mon, 10 Feb 2025 04:20:04 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ce3761f056cf40d8c41e2b7cb5b20e98bb2151d79db0b3b0378db76688805aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317513340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d3588affb01e42ab045f54dd6dd275f44b30ccbe9abd1bef643c0f5884dfdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2f4421ccb063ed16c0fb0786483f927616d371875d7b28425c159b5156c10c`  
		Last Modified: Tue, 04 Feb 2025 10:31:31 GMT  
		Size: 5.5 MB (5538021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a43fb6c4a4645763cf20f523aae5a0a05dd9bea275c48641fb8204f2f1a4d1`  
		Last Modified: Wed, 05 Feb 2025 05:12:08 GMT  
		Size: 283.9 MB (283934070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258d873fab663f42b8b74e501e3fcb13557405d887e11f2eea4fe0ef0108457a`  
		Last Modified: Thu, 06 Feb 2025 05:34:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8e8a60a4a9537c03136cb53ffc032d6e24c3f79f038c705bd68fad93c7d61ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dfc49edb8a0ce92b36348d8747eae9a4b461468a960bc6c5bf6069059bc4ad`

```dockerfile
```

-	Layers:
	-	`sha256:ea995f1a810511067e2a6541bffa89dcddc2eb6583b98ebf1326051dc0c2256b`  
		Last Modified: Thu, 13 Feb 2025 03:02:22 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289c10cc35ac5bed54f70e77fdb8a1672d4fcc83e4870a7e5a578287e27b66c1`  
		Last Modified: Thu, 13 Feb 2025 03:02:22 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b2a8393fe49179a42a754ef53bd254d8b82ff9c68904e83c7f153e45d1493be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252974992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b784583013bdc5d9cf1b950ecdfceeee02a987a67dbbad23f466753395d4640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fdfb500bbf50405f53f91b2c1c12ce42d3953d5c01dd880e155fe000663d2b`  
		Last Modified: Mon, 10 Feb 2025 04:20:32 GMT  
		Size: 5.9 MB (5871960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88aacd9905391ccd9691a278eb65bcc011f7d7315fd4d7d1ec7332e352ebc09`  
		Last Modified: Wed, 12 Feb 2025 02:38:11 GMT  
		Size: 217.9 MB (217915207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9277b903a146a2f3302b7329ad9829289fd80546a19de2ccdbc34f47f16c57c`  
		Last Modified: Wed, 05 Feb 2025 14:11:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:16f6a8d24fe6fd13b31755f37965c3e011fd4385de774566c8921845e6c4073d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3678ce367e79baf2b6a2c9701a1068aad3a7fe5e3cdf27857b9f0c969f5df3f4`

```dockerfile
```

-	Layers:
	-	`sha256:981f6197b2d3b1fbfa4c33c97fa6769513296320119c0bbc4c3d08ded2fd81b7`  
		Last Modified: Mon, 10 Feb 2025 04:20:48 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bbf0dc7390d401ef555bcbee7c4cdd1beeb6a46cf22829ac026c2a484c8765b`  
		Last Modified: Thu, 13 Feb 2025 03:02:24 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:55293406d50d978dadf820afdad24fd657e40e626e7076675bc647b7223d97bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266849099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185a36382aa9e37ed4fb240307a9a53e92c955bde9f9126ab0333cc0d4b4f1db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7a5bf1ccc96a19a04374a3d914a8e2aa9ba3316226692ec4898b63e4061023`  
		Last Modified: Mon, 10 Feb 2025 04:20:53 GMT  
		Size: 6.2 MB (6249348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e996eef731ef8a5bfc8b5512789f25d1b414fe19942e65c864438aa768b9a6d8`  
		Last Modified: Mon, 10 Feb 2025 04:21:02 GMT  
		Size: 228.6 MB (228554602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc1dccd0b4a2b08c138ca562febba5a59611cae842c586d9d7d74c67fe14206`  
		Last Modified: Mon, 17 Feb 2025 04:20:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c681a5e4872ce67306213c2e909fd3b40e0898ab011ccf6f969691ac93538bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3768f07d1a32a050fd9c620c5dc53036fd17ca402e01c7552f85a427c9074ca8`

```dockerfile
```

-	Layers:
	-	`sha256:4c77d7cf4e09792447441cea26091d84f23c9fc09ff5e5ddaa4aa2df372b23a9`  
		Last Modified: Mon, 10 Feb 2025 04:21:15 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3759bcf7da912ff456b3478abb864f315164a1d8aa0a0fb307f1c0aa7a9ac24f`  
		Last Modified: Mon, 10 Feb 2025 04:21:14 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json
