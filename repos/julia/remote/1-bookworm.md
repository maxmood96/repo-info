## `julia:1-bookworm`

```console
$ docker pull julia@sha256:601337cecf732e0e6f49475835b11f9f449c23ea76325c8ab390f4f0f67b7404
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
$ docker pull julia@sha256:d9d70468f3678ab6363b7b2a6e514728e35e1c3b63fb0e2fe02975fa99d6111b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc41c6c261241c7f70c76caafe7c70bc0f6ef48e5cbad95c3cfcf31dc45900f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185fffc4501ca8fd1b87795c24188cefc3fb1c4ff76293a12810860031023ee`  
		Last Modified: Tue, 16 Sep 2025 22:18:41 GMT  
		Size: 5.7 MB (5716242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a879376869630edd50afe455fd18277621f2af1ebccea424a32f6ec0381d5`  
		Last Modified: Tue, 16 Sep 2025 22:19:17 GMT  
		Size: 288.8 MB (288788405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25337b9cf57e51c85291f962c0423066d94e8d36fe3f91e1215600846747b446`  
		Last Modified: Tue, 16 Sep 2025 17:59:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:af76a5870529021d3cbb07a531890774317dda228d540f198e068f25bc21f7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0456383f867427f9e1c7eecb601ba4226ce495910259042129e264f85d35bb`

```dockerfile
```

-	Layers:
	-	`sha256:436d306078ec4aaf23a8396edfbbf8ebf25498a22fbab15335a0e2f00a9ca77e`  
		Last Modified: Tue, 16 Sep 2025 20:02:47 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3198ee65f39629414f1a95c59f92c32bd1626ea5ae9db8ff3a80a36bb4def37`  
		Last Modified: Tue, 16 Sep 2025 20:02:48 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d41b1339c739500c4e0dd4c3174d105b913484da5b3079ee9bf7b4a1c4720a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86535b9cc37b04e15ec70f3426215bd90fa0679a1fd44d0b1e6bfbbeddec28db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06fecbea64e1c98b82579c5b252877b94d50415d3c0327f5eb9bc01e4d7b4d4`  
		Last Modified: Tue, 16 Sep 2025 17:06:00 GMT  
		Size: 5.6 MB (5567166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b338d05762859c3ad66bba9bbe15347fd8277ef2e4a617f61929de5470bac413`  
		Last Modified: Tue, 16 Sep 2025 17:08:44 GMT  
		Size: 304.6 MB (304646606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304f468458b63e3077d41ef4756c897f5ef4ee29bebda212f49452ba8ac11d68`  
		Last Modified: Tue, 16 Sep 2025 17:05:59 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:66247adc09a1727ca4c5b5bf3ba8e726998d6954cbbd75fc3434b3dacd9c502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b69a6f7c418581bea69b64088226088b913552886c25378a068797bf4fc9190`

```dockerfile
```

-	Layers:
	-	`sha256:27acf6e8aafe2ec2a4f095d5d779fceceadfec85b16843877f613cc1daeba00f`  
		Last Modified: Tue, 16 Sep 2025 20:02:52 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be49f03d1032b0142f6b03c7ed5391d9ccc88c0a22258a7968ec8c496ec4376`  
		Last Modified: Tue, 16 Sep 2025 20:02:53 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:7346201c78d03839a865d02c3c8e2f59b8503eaaae6cf714872401d7433d6ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be2adc30ee007891fa32f9e151656d745842359dbb5bf072bc365b26107a9bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923d6f27b6d77b52f1fc5af846a27266076e7b7e1ae8b7c4b890b33a94e056e3`  
		Last Modified: Tue, 16 Sep 2025 17:06:47 GMT  
		Size: 5.9 MB (5877990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682c840e8f60e98cca8144a317d1a3a0858db6abf909ca95026dc81dec9ddf41`  
		Last Modified: Wed, 17 Sep 2025 19:39:07 GMT  
		Size: 237.6 MB (237555798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3075cc9b848496570cc92655c3c0710cbce8e43a6562a39b20330bb4a3041dff`  
		Last Modified: Tue, 16 Sep 2025 17:06:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5e84d34b0fc52bbc5ff445ffd336394d65e4ec4a99983663ec015a7a36ac6e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f681334d0bf71745a64fd6022b0ff9ee745b43f89b484e54fe8be08220b49b`

```dockerfile
```

-	Layers:
	-	`sha256:ec3e394e3ffebaabff4f5ed85930c8bf84af91e510cdafd7feffa25049e0c5a9`  
		Last Modified: Tue, 16 Sep 2025 20:02:57 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0042876b356b892f9544d38dd64b48e9bc0398af168a0fa7102ba37a9a735740`  
		Last Modified: Tue, 16 Sep 2025 20:02:58 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:bfa70bdb6eb7d6ee1511a1ee88ff8c6d35dd25d7cc0db4ae8b4e58d66f70ff11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b726a4a58277d9a6ac5ff59f4ac40c98f1aa7fe44c5b3c1ffac73e2fa1a107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f36baca851773fd322007200d56d78ff08657f4f805d9a8e4066bd7f5bca137`  
		Last Modified: Tue, 16 Sep 2025 17:16:00 GMT  
		Size: 6.3 MB (6256350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1366e849743a70bfb103516ef4e5a046fc4302267d80e33af1627136300b1`  
		Last Modified: Tue, 16 Sep 2025 17:54:45 GMT  
		Size: 248.6 MB (248553766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab64f8bbfad8d9865cb43671f68d5d1416ecb05b99dfff394cde06d6036f1b3`  
		Last Modified: Tue, 16 Sep 2025 17:16:00 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98b420955e9a2664864ba9aaccb77fb14d8817d21c1a4734c64dc1c8c0f88d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efabd7be4e254a44f7e97a4c46d6bd5a0b752522a828c025011d3db1566b95a`

```dockerfile
```

-	Layers:
	-	`sha256:2ef4ea7b965f4f5f433690e255a6b23da8f9a210965061b1d8174d8e4344381b`  
		Last Modified: Tue, 16 Sep 2025 20:03:02 GMT  
		Size: 2.6 MB (2572214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c626f3241cc0dc8ea27f57a02ac60608e98f8841339b29b7dc1b99ad6ac7b721`  
		Last Modified: Tue, 16 Sep 2025 20:03:03 GMT  
		Size: 17.3 KB (17276 bytes)  
		MIME: application/vnd.in-toto+json
