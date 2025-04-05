## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:9e976219621405408bcebe517ae775735ae7e8028d50b9e363ee4d0d30d18c70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:028439657b99aba34e3541b295b2b5d06dd3ba74067f8230ec945ce865a47e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335619519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fee5331e4a73775f484a50e5d33a50a03ec7c55f82dd66c3f70e7086402471`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729f26174c5bda19d241a2cf32f754292c82edcb761e9a210aefe007fd67e929`  
		Last Modified: Fri, 04 Apr 2025 20:38:51 GMT  
		Size: 5.7 MB (5713365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda54e6ab4c583a33d877d9cf8877a366c33071923f384ce750ce49d820607a4`  
		Last Modified: Fri, 04 Apr 2025 20:38:55 GMT  
		Size: 301.7 MB (301700917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546df215da5f6a8e708414e3eed240c6cc52a4a24e3902c6b24bac4d42c0c9df`  
		Last Modified: Fri, 04 Apr 2025 20:38:51 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d2f8ca33056925e9be2197a1a51c97fbf9bf1dba698044ce717e98739074f45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66278b12f89bd7cdeca3165ecb6d56ab9f39744f5666689b0e62f696b385ef63`

```dockerfile
```

-	Layers:
	-	`sha256:3fe19572df3b40b1b0d51e01599d34349688a709b1f9340abda21a084068b3ff`  
		Last Modified: Fri, 04 Apr 2025 20:38:51 GMT  
		Size: 2.4 MB (2444946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8052d9bbd1bd372a4b8ee61e03d52dcbc49263c7fc27100a67e4e228404fe019`  
		Last Modified: Fri, 04 Apr 2025 20:38:51 GMT  
		Size: 17.3 KB (17271 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7e6eb4121f8fb0f3a8f5e7f33849e9bc0ad6c19d5143bb7ec478d6dbcaf7366a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.9 MB (356945726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d15de336a1560224c624cf018637bfe39db54c50ae37eab3d6cf482f012869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f964432604bb8a18407e752ca960521527f757adf65396cfd76b0bf020158ea`  
		Last Modified: Fri, 04 Apr 2025 20:38:44 GMT  
		Size: 5.5 MB (5538332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1cfe9435d11ef475d14a416e93bdca10a55ff5708ff9c99222e752ce4d143e`  
		Last Modified: Fri, 04 Apr 2025 20:38:51 GMT  
		Size: 323.4 MB (323362983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936f2e9fc24a75a9f515ceaa0c24bfb81460111dc95fb4dc516a9c6f217c6d2b`  
		Last Modified: Fri, 04 Apr 2025 20:38:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:04620ebf5cb43bf458d06b71b5ca2415f0639fb616fdfe89f4216d8f81ab1018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d3baf27fb4fb771df02aee4d4d63e7da46781639bb2a0548bf610ff6d0b570`

```dockerfile
```

-	Layers:
	-	`sha256:550b7409ccefcb68086ba83353af242ce887b1a78570bc57e04f1035e82cfe92`  
		Last Modified: Fri, 04 Apr 2025 20:38:44 GMT  
		Size: 2.4 MB (2445245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24c6c8ac96030800f736055b22a9b856849cd44b51f96ed26244a8f841a1576`  
		Last Modified: Fri, 04 Apr 2025 20:38:46 GMT  
		Size: 17.4 KB (17414 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:69677ffc67539bd6f0461d1f39907f77872ffcd13e76366af9e49a5b7a562644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275625896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad70c1aa83675572094838807a729e7b4d024d930d6336383093d2254a790f9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92662e1f7f893888e7c59f5b450c2ed5a397efe94850aadbb53a8c2226029ee`  
		Last Modified: Fri, 04 Apr 2025 20:38:41 GMT  
		Size: 5.9 MB (5872265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b722713a3bdaf706cbc005bbb810f324cdcdaa04729aeab1e23c0bb480bfd51`  
		Last Modified: Fri, 04 Apr 2025 20:38:46 GMT  
		Size: 240.6 MB (240563733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b45dfe5c872ed9891de4ebf514182adbe39e6f8c5da7698f0cad5a8feac4c58`  
		Last Modified: Fri, 04 Apr 2025 20:38:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:31618b871a2d71300e381c893d1f649ebdb45a914a4af4feba5229c70e2a5e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d781664995ca53bbf373394ebbcedcb1a856c2ceb1616950b9ef133b3d12669`

```dockerfile
```

-	Layers:
	-	`sha256:2acbbf16ca1d527467ee599b9228f380493643fedfce2a2754724cd569dd2ce3`  
		Last Modified: Fri, 04 Apr 2025 20:38:41 GMT  
		Size: 2.4 MB (2442029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebd0ccf6d8019216dbed0ea8a89a8593c0648da3eae7a0b12a37ff247605fbb`  
		Last Modified: Fri, 04 Apr 2025 20:38:41 GMT  
		Size: 17.2 KB (17227 bytes)  
		MIME: application/vnd.in-toto+json
