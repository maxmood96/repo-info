## `julia:rc-trixie`

```console
$ docker pull julia@sha256:82a82636f1191e1ca8d3c344c27ff864cc9c247d3ea33cb75965fef87871f4a8
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
$ docker pull julia@sha256:5947cca876a6ad7539ad68d0c47ff05acc07bbfb8e5663b0553306e8badd4112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345431596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2895025573ac08f6eebd3e47d397e51bc335fba0a631ccb4511811f7e98f813f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:22:27 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 May 2026 19:22:27 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:22:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 May 2026 19:22:27 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 08 May 2026 19:22:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 May 2026 19:22:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:22:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:22:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77579b1922e22fca45b02d562a739a8fdc1f31e4302b9cbb605cb275292389`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 6.2 MB (6247090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad43f27e105c83a91b1af0035f72aa34b5ed58ec1722c036417e11787930ac`  
		Last Modified: Fri, 08 May 2026 19:23:18 GMT  
		Size: 309.4 MB (309403909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cf8fb8ed1de9c8434a1d064fbc6b814054ed8b8dd26b8d9b3700a9f36328c6`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:35debd6a3318a3a908942135753064690a2490c24f2f2b20335699847535b1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22122dfb87a07a4ab2abf246fcf3971067c63fe412f889d1e10c017cd579023b`

```dockerfile
```

-	Layers:
	-	`sha256:50715123b86412245456a12918f8867d42d8b393948fd2df9778e9ee1b246fcb`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 2.2 MB (2240907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca394b489c306211c4e555e5e6a71fe184a7781f2bb939b9ec905e303635a009`  
		Last Modified: Fri, 08 May 2026 19:23:12 GMT  
		Size: 17.2 KB (17161 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:64b0d075380aea85d630da69734082bb7216e96628c713d99391a57f3938ea0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370107055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838f69cf5aa9e0dae66034ba637d3b1bc3b846a2eb0fbe528615928a0f06d581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:20:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:21:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 May 2026 19:21:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:21:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 May 2026 19:21:29 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 08 May 2026 19:21:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 May 2026 19:21:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c326e4356863911ec57dcad175191cecc464fee161c1255190be6e61690a9f`  
		Last Modified: Fri, 08 May 2026 19:20:50 GMT  
		Size: 6.2 MB (6154403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2af28196db51d060c5f7e074e3ef8dd1f046cc129430e9c93077bf3b4c569`  
		Last Modified: Fri, 08 May 2026 19:22:29 GMT  
		Size: 333.8 MB (333808642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc84cff2f3e376b79c9b80129cb15c4a6ff5d9d58d201852895f1a0ffa15d9`  
		Last Modified: Fri, 08 May 2026 19:22:16 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2077e00cb826c86d2d2f41f8333fb4739983d102ad969358e1f5852f9f0b469a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a781e67ed9ebd6009b5c56f5905279491ce61bcca11fc263b538f3b093d2f`

```dockerfile
```

-	Layers:
	-	`sha256:5a600b153e3de53d31cba9f62f1af77ee9d6b8eb57c2db8aff3a8d426c07a84d`  
		Last Modified: Fri, 08 May 2026 19:22:16 GMT  
		Size: 2.2 MB (2241215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b274effb57ce273ffe68124573b0dfba47ae490fe4c4bc52b7897af79955e7`  
		Last Modified: Fri, 08 May 2026 19:22:16 GMT  
		Size: 17.3 KB (17302 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:46bde8d83d30acbaa6dfd306fa2708cc06e18458b4998e96129c79503dd849c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281059758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427f8998543b686f9cbfe7b1f73f042259297bf5131665f49ad0fd96615ba523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:17:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 May 2026 19:17:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:17:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 May 2026 19:17:09 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 08 May 2026 19:17:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 May 2026 19:17:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:17:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe42ffe56891d14b2608e8f39f2cee67e1711bd36ebdee81f8b34f5fdbba9d`  
		Last Modified: Fri, 08 May 2026 19:17:45 GMT  
		Size: 6.4 MB (6433784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77f4a3156539ddba1b70062a7842bce5ce4545f2359fea1dee1f7841b7e3f30`  
		Last Modified: Fri, 08 May 2026 19:17:50 GMT  
		Size: 243.3 MB (243329203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fd7737ea154031a99f811b1836de18ee32ef9c0640a091f6dd4586a7e352b3`  
		Last Modified: Fri, 08 May 2026 19:17:45 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:91f8391d3f6a9246e6bf9af55f88c7cf79d35fb608d3b17b9555b9a2e937aba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3aa380ae62e571d8ea2675e763c440b68475b0ddcc8cc0b6f1dd5e75e316f`

```dockerfile
```

-	Layers:
	-	`sha256:37a077a1a417912fc3cc666e42d3a80939e0aa7d036ff6187ffd719d3e0e9a05`  
		Last Modified: Fri, 08 May 2026 19:17:45 GMT  
		Size: 2.2 MB (2238042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:141c00b3f642460a275291ec8e827418277a3f161a6542c85419d4e1154ba447`  
		Last Modified: Fri, 08 May 2026 19:17:45 GMT  
		Size: 17.1 KB (17116 bytes)  
		MIME: application/vnd.in-toto+json
