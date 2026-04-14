## `julia:1-bookworm`

```console
$ docker pull julia@sha256:1f55bb010c86ff0bd86b11563c7b8b98400ca4c356160e1506ad2ea6b5e898bb
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
$ docker pull julia@sha256:24e599263b1153f684242ee01221912d836c9e573ec81f2a7e570d79b0c8f659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327513292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c914c965df03d54c7544eaca8108dee7cea55aa757da89ff14e6845a4174c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 23:39:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 23:39:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 13 Apr 2026 23:39:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Apr 2026 23:39:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 13 Apr 2026 23:39:34 GMT
ENV JULIA_VERSION=1.12.6
# Mon, 13 Apr 2026 23:39:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 13 Apr 2026 23:39:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Apr 2026 23:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Apr 2026 23:39:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f7e2ec67659e4298f13a25bf25a38aeb8b699c02d5e43a62fca14140854b70`  
		Last Modified: Mon, 13 Apr 2026 23:40:19 GMT  
		Size: 5.7 MB (5718751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4e4b5804e08ed2eac3fbe778956d5adc84cd93bbd7b3d5c2fc1f7c9132f117`  
		Last Modified: Mon, 13 Apr 2026 23:40:26 GMT  
		Size: 293.6 MB (293557841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab111c1fa0489d140105b68e259a8ee3070018a82604701399284888ed0328c`  
		Last Modified: Mon, 13 Apr 2026 23:40:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:878e343805f4fabcab655b6cc39cd2da7d8459341c56096d91c124a374ad048a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf7503ad2ed65a10523d7bafe88935b74a92a18ea8d31f10e242a57e4f0a1c3`

```dockerfile
```

-	Layers:
	-	`sha256:0e2a0865110482ae2088454d7aed1d8c0716e7f7fac44fa494db36694a7a965c`  
		Last Modified: Mon, 13 Apr 2026 23:40:19 GMT  
		Size: 2.6 MB (2567696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a2982c53386224af7fef517bc2d776d969891cedf0c09bd7d35e13e4133793`  
		Last Modified: Mon, 13 Apr 2026 23:40:18 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b42f694f6d5d56d2f237d50a2f2f5136d09476ac43336cd7cb1c358bdb07258e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347943975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c7d32ca5519e3c19bd5b0f1802c75c7622895e96a2d0d38d4c08ca0dfb4a01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 23:52:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 23:52:45 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 13 Apr 2026 23:52:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Apr 2026 23:52:45 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 13 Apr 2026 23:52:45 GMT
ENV JULIA_VERSION=1.12.6
# Mon, 13 Apr 2026 23:52:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.6-linux-x86_64.tar.gz'; 			sha256='bbabf3bef19421a9dbd24a767d807606ab85e444323b5a1c73ffe293fa3d079a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.6-linux-i686.tar.gz'; 			sha256='2ab43d56adfe96c7b0b9ddab0e049f54f49df24049ec8b482c26737c42af28cd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.6-linux-aarch64.tar.gz'; 			sha256='029b93b857bd0ffd627f9a8580d3bbaa63daf008d7b7aed02fbceb8fd57c4899'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 13 Apr 2026 23:52:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 13 Apr 2026 23:52:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Apr 2026 23:52:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30df06202da529fb3050c9ea4baecf28fe2634a66824cc7c27657eb185e47d6b`  
		Last Modified: Mon, 13 Apr 2026 23:53:32 GMT  
		Size: 5.6 MB (5568691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee5c2a6345c92041c2f9e822597ee8d8320a6dd65d4de156ab4ee8b44758d09`  
		Last Modified: Mon, 13 Apr 2026 23:53:37 GMT  
		Size: 314.3 MB (314258746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a521cd6affd4341c889783ef529b99835b8b8a6c378eb36fbd249f9d3d60e`  
		Last Modified: Mon, 13 Apr 2026 23:53:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c697f049ad02559c35344480bf689f44faff6f40daca20eae5be5ab49d07f450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeed860fe8905af822b62ed32561b5540817e0eab03b9d82b3d475f89efe112f`

```dockerfile
```

-	Layers:
	-	`sha256:ce65ed674ff7d0566f9df73350fc7825c6e4239c3a0164282437ef1e97f26a67`  
		Last Modified: Mon, 13 Apr 2026 23:53:31 GMT  
		Size: 2.6 MB (2567971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826b7e6d0a581624237fa078028df5bc10410f68aca80a55dbe36baf26de08ca`  
		Last Modified: Mon, 13 Apr 2026 23:53:31 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:9199c949fa64e71ab98476abca98106a8a0b16607d01678eedd30cab117e0fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266282667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a3eeafd89bed89cdf88adf747cf657693f5dfce8ef424b45e9820b7152a2b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 07 Apr 2026 01:18:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:18:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 07 Apr 2026 01:18:09 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 07 Apr 2026 01:18:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 07 Apr 2026 01:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:18:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc68e999e64389764d88ef7baedb7a612a448f0182971195994993253f8fdaa9`  
		Last Modified: Tue, 07 Apr 2026 01:18:41 GMT  
		Size: 5.9 MB (5878855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc61dab2ef6e5e3bd3cef4d96f329b6d7a974cc3e7376e62e98919aa2b56a63e`  
		Last Modified: Tue, 07 Apr 2026 01:18:46 GMT  
		Size: 231.2 MB (231181675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033110fd7e62e5086d82a00df47960aef2449238754fa2c569a53262db30b977`  
		Last Modified: Tue, 07 Apr 2026 01:18:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:eab379c95ea49918488df0af51c7bc22bd4e6f1b652aabd75d75a880224c8ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b508e278e39b2783fbcb05f3589106ab521dc233fdeb051527fd247e33b5a4f0`

```dockerfile
```

-	Layers:
	-	`sha256:3319ed3f61899c451c234cf710b32234faba247106f5abc2f27e95f2442cc337`  
		Last Modified: Tue, 07 Apr 2026 01:18:40 GMT  
		Size: 2.6 MB (2564843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0409ffccda9ecbd7b1b5e7bf1031b4bc27c0ec0c724364272b18e8c5e50bb5a9`  
		Last Modified: Tue, 07 Apr 2026 01:18:40 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
