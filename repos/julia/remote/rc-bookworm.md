## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:32b0e2a5f3fa00c5e8c9215d6240cfc77886b9389a0087053891a9923e581e3a
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
$ docker pull julia@sha256:03cabbff7c5be2dcd49d92a721ac580759432217ac306ae58a400258f68ee640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288594901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75a4f6eb4807bb2ee712cfc0d58c86615fa2350a0b0d96238269880f5c2772a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fd106feaa90a7effb645c4e2f3d002c41929edd0259ad2e73fac53f2bcc4b4`  
		Last Modified: Wed, 29 May 2024 23:01:25 GMT  
		Size: 5.5 MB (5515128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d9b4980b511ff4b8f209f9ff57e1cbc259552f9d224607646cfbc3f0269e3`  
		Last Modified: Wed, 29 May 2024 23:01:28 GMT  
		Size: 253.9 MB (253928988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86957464ac0974146a021c4ebf1ef686082f33c62db60b4758b855cda63d8874`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b41e1b6647af26fe4c47bec7b8b168a95d72420deb6fab5716443de7ad707d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54d674633d4762363a212275f15735af65b9c420598900c66625e919d30ebc2`

```dockerfile
```

-	Layers:
	-	`sha256:f4bf7af2d082a8fd0a8eca1fda5155c75bdd3fe9332f356a67c2557e7c283871`  
		Last Modified: Wed, 29 May 2024 23:01:25 GMT  
		Size: 2.4 MB (2413060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc0f928641100457e878ebfed4e4426da7281fa618c5add751adbf87255a7db4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 17.7 KB (17676 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6a3fe739caf64107a08f0175457e4601cf330d7570ab2d781e07d2bade4cc577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290151323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e294d0388b233a32ba5d10c6c8102f4e48997a5d18bee37e5dc7e80ce6a072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fa053fb67d67a437e7d881b9c7529188bc7f949e90f10cb2c511315b3c89ad`  
		Last Modified: Tue, 14 May 2024 17:32:52 GMT  
		Size: 5.3 MB (5339363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19972d68ea35d475f60c52d060cbf722e0846b4d96933aee5622aa2461fdb493`  
		Last Modified: Fri, 24 May 2024 15:19:01 GMT  
		Size: 255.6 MB (255632086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b87e7345c3a5a12f3d4dfab9dd92a93a7f2a4bac8abeb2131aa5d298957c6af`  
		Last Modified: Fri, 24 May 2024 15:18:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:dcbfe9bf20dc0222500ca8b7157f99d8d13327808b851768f1a2e998c131d71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a5e71e098ac2f4b351b2fd729e54c50a83b2d43a6d5cfafe1dcf1c4f5ea30e`

```dockerfile
```

-	Layers:
	-	`sha256:9023d4211a95b9f4686611c030f6bf98bd8eaf5bec8789be98bc375ae4d897b6`  
		Last Modified: Fri, 24 May 2024 15:18:56 GMT  
		Size: 2.4 MB (2413293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9cf8b2bbbd32e4f59e3349778af08ce8f08a2ae566317de41cde1c889c7486`  
		Last Modified: Fri, 24 May 2024 15:18:55 GMT  
		Size: 17.7 KB (17690 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:9dd936ceb3521d2a7852bfa61fca9a4ba2eaa05bdf19cc83053d1e834d8f2a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.0 MB (266984845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e10b14bf5503fe9db03ebf9de5b1d788cf91c42da996a26f7dd04c749d4baf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 29 May 2024 17:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 29 May 2024 17:59:24 GMT
ENV JULIA_VERSION=1.11.0-beta2
# Wed, 29 May 2024 17:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta2-linux-x86_64.tar.gz'; 			sha256='e92ae1cebd519180881770cc9ab903d39c49c6bcb9c8251861e6eac9acd566a6'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta2-linux-aarch64.tar.gz'; 			sha256='71f7c0135c3dae94c069b6ab391f8a4a05f857acea3f8d6da0352d00cb86d49b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta2-linux-i686.tar.gz'; 			sha256='9d1e9f8a03ab6396acfc3e4d4edcff68907b20c53f252da6ea4573a72c39e361'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta2-linux-ppc64le.tar.gz'; 			sha256='e7f9bbe1843760e52a57e0d502990af3abb189f5a20ed292ce5d00db1d003088'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 29 May 2024 17:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 17:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 17:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9588e9c80e65c716943da8619e72a8f5679070df7bce67340a049a73526197c8`  
		Last Modified: Wed, 29 May 2024 23:01:28 GMT  
		Size: 5.7 MB (5672120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4803467d8a500f56935727cd2b1c86668ede8f2ea05cd6011b505cfe86b38e2`  
		Last Modified: Wed, 29 May 2024 23:01:33 GMT  
		Size: 231.1 MB (231149712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510adad0358764b960b5e1c30de7898a1ba1161dd3a23029b6963a7bfc7f80a8`  
		Last Modified: Wed, 29 May 2024 23:01:28 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:77695c13445d461169c3ff89ef5ef5091982e18f2c6a15ceffe699000f9502bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3972a41b1973913483f23ab085543d651550030dc22877c8de585ea8f69d34a`

```dockerfile
```

-	Layers:
	-	`sha256:4f1e564d0886d63d4b8af74255c5f1a6416e4831fb9615cfa9c1811174d98372`  
		Last Modified: Wed, 29 May 2024 23:01:28 GMT  
		Size: 2.4 MB (2410142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cacbddf4d3fbc3849f447882deefdfc1f78150510868775a520d23deaf1cf778`  
		Last Modified: Wed, 29 May 2024 23:01:28 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f33c807ec34c5f8a6fa9697e9939f6a6fe2700e0ca9849a87ae90dc705e002b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 MB (283971456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a118985f4341807de5017b2e56bbda3b76256d301e448f83d0d668bbf634be7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 May 2024 13:40:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 May 2024 13:40:20 GMT
ENV JULIA_VERSION=1.11.0-beta1
# Thu, 23 May 2024 13:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-beta1-linux-x86_64.tar.gz'; 			sha256='43aeebbad319dc9153d3683c39bc2c07dd2d500817d6114e901eb590fd47c472'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-beta1-linux-aarch64.tar.gz'; 			sha256='9e2ce232e40d2e946440cbaa3fc3dd4a51033021bbef7fb5bc2ac62fff8e44fc'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-beta1-linux-i686.tar.gz'; 			sha256='966f9d461d6e854973895f8ad11ea62b38378d475479b58c8e792f6f50c6c026'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-beta1-linux-ppc64le.tar.gz'; 			sha256='7b3ecc6e001c80243e71b72594fba4f713cdd14abbc19d3d57d386dd1c252746'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 May 2024 13:40:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 13:40:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 13:40:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e3dfb42059f32c4dafe0538df9be69eab297a1e3043c2dce4da269ef34e06`  
		Last Modified: Tue, 14 May 2024 13:24:04 GMT  
		Size: 6.0 MB (6047044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346111c1db28164deb2836502066278281ebcd31c0f9f3b6440914709e6b4650`  
		Last Modified: Fri, 24 May 2024 15:08:24 GMT  
		Size: 244.8 MB (244782881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c7a6aa73b677b18375ff3dde173cc476fe6603abe815023216a340e59df0db`  
		Last Modified: Fri, 24 May 2024 15:08:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9a930c45bd7af4c87b2279e40f94c522dbee00f4b59ea38eac3db74c0c40c10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aabfa17740eb1f3f7a5b69412d7e4662bc8ea9b8717ada3ad9d41a4aacf46de`

```dockerfile
```

-	Layers:
	-	`sha256:4e4035262004ef3466b1ec0e5a3dc1b827401907b06a8086c6a6661eef3f98ee`  
		Last Modified: Fri, 24 May 2024 15:08:14 GMT  
		Size: 2.4 MB (2417479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5ca8dd5a2869a76c7d4e6ae9f59ec968dea3663da617d629360dead47742a8`  
		Last Modified: Fri, 24 May 2024 15:08:13 GMT  
		Size: 17.7 KB (17728 bytes)  
		MIME: application/vnd.in-toto+json
