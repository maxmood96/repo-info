## `julia:1-bookworm`

```console
$ docker pull julia@sha256:cd4ccbd43e2baeddd45c208a2f6703cc76212d38ad0328c1f8e1a07eadb0e80e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:72dd5dcea2af512583924e6c7773a43881f19f38084159d1be244922f1797884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323769205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48d2934b4aa4d18709f180d0a3c7504717934152bdab1424975923746c89c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Thu, 08 Jan 2026 19:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:04:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 08 Jan 2026 19:04:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:04:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 08 Jan 2026 19:04:29 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 08 Jan 2026 19:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Jan 2026 19:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jan 2026 19:04:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648fc7fc079142c391b2b6869e1160c6171968d973cdfd83c22010af842c8fc3`  
		Last Modified: Thu, 08 Jan 2026 19:05:49 GMT  
		Size: 5.7 MB (5716385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abd5e63431ab1440254f8567bcf203a78107af180cd63744981b342e4788b8d`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 289.8 MB (289824029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bd07ac5abdcb546fa58eebdf02d5382bbf93956cc0900c25ff8167eec5ffe`  
		Last Modified: Thu, 08 Jan 2026 19:05:49 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:11ff0f3dd2322dee46f513dd0f929c905deb5d08a229e7f18fa6fab9b94f4120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ee7e2e19b6bb3f1d85eb541169c9e8935dc4b3c7662cba1e477751f7fab1f`

```dockerfile
```

-	Layers:
	-	`sha256:3473c5c1c693a8f98ace833b81e7a66af7fdd2770ad92b7d5e5d002ec073cbf8`  
		Last Modified: Thu, 08 Jan 2026 21:02:58 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2faa79fe6e6fbf376b9a024644495bd570405a2d5771cb21275704edd8050f54`  
		Last Modified: Thu, 08 Jan 2026 21:02:59 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9fcef9c906d9afe28fc6422dae2b51ab795cafbba7aa3e949cbdfbbd2b5f3625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344942117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa76e6baa3d1ebd21fb9338c60d69ffcf2ce39c3f6e99304a81d4202393dfe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Thu, 08 Jan 2026 19:05:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:05:33 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 08 Jan 2026 19:05:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:05:33 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 08 Jan 2026 19:05:33 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:05:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 08 Jan 2026 19:05:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Jan 2026 19:05:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jan 2026 19:05:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4c068c7011ce46fa06ca69866656d6539a78b536404eac59574f66214a4673`  
		Last Modified: Thu, 08 Jan 2026 19:06:41 GMT  
		Size: 5.6 MB (5567039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fa9c295ce3c6b8141dcb8cad058e322cfce326dd4177d39769606b0a4d52ae`  
		Last Modified: Thu, 08 Jan 2026 19:07:11 GMT  
		Size: 311.3 MB (311272498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc8bfdc4cf3c613881ef9a129024df965f3b1bb548660654a1069b5e917c8e9`  
		Last Modified: Thu, 08 Jan 2026 19:06:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f08d1c7d9ed1614819126c4c7027928bc7216ff87be636a454f31b8f26dc0874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4cba7b4962e9232919bc2b2eb6d71309dad1c8d52a62b29d1a3bbf6692cc6c`

```dockerfile
```

-	Layers:
	-	`sha256:973a3635029668a02550bd93b2258c59689f9972987e1836e8fb8ef547ef141f`  
		Last Modified: Thu, 08 Jan 2026 21:03:03 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b51191426b2fddf8e1539b1eac82b5bfe2787445ec9359b3e6ef7f77ac728a56`  
		Last Modified: Thu, 08 Jan 2026 21:03:04 GMT  
		Size: 16.7 KB (16664 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:4c5631cdbbe8968055a00023024f940c9a704018fa6caddb0897e18686b215e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266295043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dd0b80661e251615daa0f5df2ff06e34a93150e189263c5b494bc46de1dd4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Thu, 08 Jan 2026 19:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:04:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 08 Jan 2026 19:04:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:04:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 08 Jan 2026 19:04:35 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:04:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 08 Jan 2026 19:04:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Jan 2026 19:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jan 2026 19:04:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2271d90223d57644af0cdca201ad553d48f7f958e6d1c8b02075e4fa3f9457`  
		Last Modified: Thu, 08 Jan 2026 19:05:30 GMT  
		Size: 5.9 MB (5878041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9fe8e2f0e16281683837e6579ad6bbde6f7e353c2cfc38141f884588ff7a29`  
		Last Modified: Thu, 08 Jan 2026 19:05:45 GMT  
		Size: 231.2 MB (231206860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400579237af6724769abacbf897b81cd2141ce7f923fb1c8584ae05904cceb28`  
		Last Modified: Thu, 08 Jan 2026 19:05:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2cc9d993256b22b642a120a1970b81688ed7c901652b78593cca97b46df146ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e0cb9b0ea992dc1a0e7c0d653b0cacc4a25415ece1142736426ec02763ce4a`

```dockerfile
```

-	Layers:
	-	`sha256:83d9a59220f5d745ee285857d6c490aaaa5e560d263844ddf75c9b0113769339`  
		Last Modified: Thu, 08 Jan 2026 21:03:09 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:695d1ea00e3c8f88b1b164b180958b5a6a6edbe2dfc272c905de694d4d486df4`  
		Last Modified: Thu, 08 Jan 2026 21:03:09 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
