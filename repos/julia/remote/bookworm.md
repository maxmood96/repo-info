## `julia:bookworm`

```console
$ docker pull julia@sha256:1623eb4161dc20ee57bcf694e48cb16cfc2aed71507e79b2ff170a206ccd7803
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

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:a71c0a8fd7dbbcd99c9f1688690729d11bdea697e0d544b7226ab05df74b67c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323156888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1edfd591fde11a8eaae63a77315dcc7fd047b3800bbe03ce46abf424ba8a3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844af1b1ff2b946b7015251394b8d254e257527322e8f92ddf3dc77edf428a94`  
		Last Modified: Tue, 09 Sep 2025 06:37:06 GMT  
		Size: 5.7 MB (5716145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfe24a70a4e13c5e7869f484683f0dc4faec4de637809846140818c4c9ef49`  
		Last Modified: Tue, 09 Sep 2025 06:39:36 GMT  
		Size: 289.2 MB (289212026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac84c2359f8d18452c347e91968326b869f2465e917a8ccf25b4ed5b4bc87e8`  
		Last Modified: Mon, 08 Sep 2025 21:38:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:565009a5e0bd82dada374ff77384d006a8c74f03f66ead520cee5173273700f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2accd452d3a61715ee4f7670c354554a71032a7a8f21d31f5f76ae7daa1bc6f`

```dockerfile
```

-	Layers:
	-	`sha256:e4e988841c2dcb32d5d6562d10bb67fef7d2f3fb421d14ce958f2d88d8464afd`  
		Last Modified: Mon, 08 Sep 2025 23:02:42 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c68127f06c72af3bd67a09198a2fe3cb81aa3172dc925d10dbdc07a31f37342`  
		Last Modified: Mon, 08 Sep 2025 23:02:43 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e9eadd18cdaccee067e5eec3cdbff58e757af51e1f2a5cb1ab3559daee379bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338258489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d83ab429861e3822cb7bdd1c52d9276b0f7113a558c02312c7ba6aed4eaf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9ab5052254237ead345107271279337f3bdfbb18b6a2d5dc59747ea84aab90`  
		Last Modified: Tue, 09 Sep 2025 02:30:50 GMT  
		Size: 5.6 MB (5567123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ffae561750aa987ac605e878964598d914161cab25f227fb79878fa6095ec`  
		Last Modified: Mon, 08 Sep 2025 21:20:45 GMT  
		Size: 304.6 MB (304588898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6e03a787f690a428a01e9699edf4f7830a88e8222fa609de31ebd3bef35605`  
		Last Modified: Mon, 08 Sep 2025 22:02:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9c1d30dd31d34b526faef0ce72f4094d3e7a664fe6fe4cd76a7f6644b7448b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033d24a46177e824e903cc22736c935187c8a55ae1066942247f163ee3da137a`

```dockerfile
```

-	Layers:
	-	`sha256:c57efd5eb5a0b27f5bdce17ee312324a475dbb592bd86c41d17916214c573f4f`  
		Last Modified: Mon, 08 Sep 2025 23:02:48 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e165f45790a7fd33227de53994f9851d674ef62ddad32ae45fd3aa845ea5e5`  
		Last Modified: Mon, 08 Sep 2025 23:02:49 GMT  
		Size: 17.3 KB (17348 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:608053598bdb954b7a994092ff9dcf855a1bdd51f81da303449ac155f163012d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272777403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5100021e8cc23a9f8f7847a630ca6e2400b74d63cd9e6eb03f2284b38311a16d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec47e88145f35f5c113f880370e19edb42468a47ed3f7d1811dc41556b8d5c0`  
		Last Modified: Tue, 09 Sep 2025 02:49:22 GMT  
		Size: 5.9 MB (5877977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bb2eb795e7f1f6bd2a556d41b2fdafc2652aeda006fdca5efd39d91d364ce6`  
		Last Modified: Tue, 09 Sep 2025 19:11:22 GMT  
		Size: 237.7 MB (237689424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae022827daae6240aca6fea321143fbde2f44166798f53e749dd3157c81e01`  
		Last Modified: Mon, 08 Sep 2025 21:18:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3ab7e3edc27fa92fcf131b77641e3c235b94ae9ce09f95093d1f8af10789223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7447a159a83d56a4adc05edfb47c62e6adc0e26322445d6bf89cfd1f10502a9`

```dockerfile
```

-	Layers:
	-	`sha256:e7b4f76df35561e5b4cd22db9be7a01da187e9f1dcb4a62ccbc1f98629efabaa`  
		Last Modified: Mon, 08 Sep 2025 23:02:53 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdc488ca55b4842de649e36e7e114ca82aba6614564b76e8e330d5130590163b`  
		Last Modified: Mon, 08 Sep 2025 23:02:54 GMT  
		Size: 17.2 KB (17195 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:51c0c20b00c7294b18a0c3a2538462fe50dd9ad476700661e40fdfaabed7fbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286921897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331720d121cc6f63bedb15dde6d6840f8a2aaa3ce2774ca2a02a74b96a61aedb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 10 Jul 2025 17:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 10 Jul 2025 17:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 10 Jul 2025 17:59:19 GMT
ENV JULIA_VERSION=1.11.6
# Thu, 10 Jul 2025 17:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.6-linux-x86_64.tar.gz'; 			sha256='e99e52e2029d845097c68f2372d836186f0eb3fb897a9dde0bdf9ee9250d03d5'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.6-linux-aarch64.tar.gz'; 			sha256='c2c5cdce017cacadaccb7d22aa070f549e4e87c4bb10f15853170ddcb50bf5f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.6-linux-i686.tar.gz'; 			sha256='910fa8fd8a2e7dbf44b96ac3207e2b50744661215d10d4828f9df1bb5606d69c'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.6-linux-ppc64le.tar.gz'; 			sha256='2fe08eb776b6eb76e7f75cab2ba09befc45ff2d69a88d062aae10a9d8fe99c11'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Jul 2025 17:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jul 2025 17:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a74f79402d7019510ab7ad3578e8e831a0757be39b02b9d6e1d17ce54e9971`  
		Last Modified: Tue, 09 Sep 2025 01:23:57 GMT  
		Size: 6.3 MB (6256304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f6b75b10f865d4ba71177d7de07d8d943b7cc4b14ce582eb2f0656d20e0055`  
		Last Modified: Mon, 08 Sep 2025 21:49:45 GMT  
		Size: 248.6 MB (248596462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de00d33693f9dc602d67dc596de98456a2c53d3b8389f1dabfa9af438352149c`  
		Last Modified: Mon, 08 Sep 2025 22:16:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e57832a9305f6082f87635dec74b119dc321b2ccc3a0d04820d0fa0d805814c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c153cbaa37f955a8f98a27cdf07d4e3a6e871b789a4cdc19e5467a2bf90fc627`

```dockerfile
```

-	Layers:
	-	`sha256:f008341567fc24ca8ed6c625eb88839e6f91b505fa767f635edc9b90825424a8`  
		Last Modified: Mon, 08 Sep 2025 23:02:58 GMT  
		Size: 2.6 MB (2572214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d55b9a98c7204151ee6449e5928b93afc60b6dc5b26c551e9540c6b0b0e7f5`  
		Last Modified: Mon, 08 Sep 2025 23:02:59 GMT  
		Size: 17.3 KB (17276 bytes)  
		MIME: application/vnd.in-toto+json
