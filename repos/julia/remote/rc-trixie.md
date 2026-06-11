## `julia:rc-trixie`

```console
$ docker pull julia@sha256:b889b1b82ce1d093b87d170c183453fbed4eedd0feafef88d1155b7ad0165484
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
$ docker pull julia@sha256:74fc96481d197fcca8d44ab4122ca43f9f3911a954f6ca04097b750b55adf70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345438239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f04034b0a0eba50f32fdf676ee900ab2811714a1ce289bf500e47c0d127a63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:23:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:23:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:23:02 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Thu, 11 Jun 2026 00:23:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:23:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273286dfb09027c9950b00e0808656a132028531412b8305f2be2316e81c4d6c`  
		Last Modified: Thu, 11 Jun 2026 00:23:50 GMT  
		Size: 6.2 MB (6248412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebb85e8e6f0ed31c7ba072727e0d15aa1493811b840387b40a730268dd4537c`  
		Last Modified: Thu, 11 Jun 2026 00:23:56 GMT  
		Size: 309.4 MB (309404043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0f1d429e19be9aba6410d1fb0b7fd4ea30cef82db21bf3d2273323ba73e938`  
		Last Modified: Thu, 11 Jun 2026 00:23:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:9f581b87610cbb1283e0819b4ee52030a7fe050a502ab2c144c342852288a128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b74b09c81bd1d9c08583195c303053f94017974f0fdd2096efaea39877125f`

```dockerfile
```

-	Layers:
	-	`sha256:33c70a376ed56982a5676739dae7a627135117eef1d73fb9640b01db7020b577`  
		Last Modified: Thu, 11 Jun 2026 00:23:49 GMT  
		Size: 2.2 MB (2241075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903430cd833872a3cd7429675f0f0ecc5cdc2f19564e297b0d3da5b3e8ec07a9`  
		Last Modified: Thu, 11 Jun 2026 00:23:49 GMT  
		Size: 17.2 KB (17161 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:706679a3084b01013eb930ebd0a1c3feb750c8271e3ef9c99c4b71218eb24cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370113063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1029ec100a5741fd38111c64a6652c166ba231432f9a787fbb9fd7549f4c5ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:23:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:23:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:23:10 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Thu, 11 Jun 2026 00:23:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:23:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706f6c82b865dc631077d4090500e0aae4566c8593b9a035d484e36f0c48a706`  
		Last Modified: Thu, 11 Jun 2026 00:23:57 GMT  
		Size: 6.2 MB (6155422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecba678811bdf3c4f03e1a035da89f65a0a13534d2ab2d2b6b46ab608ff017c4`  
		Last Modified: Thu, 11 Jun 2026 00:24:04 GMT  
		Size: 333.8 MB (333808743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7404b60533818364f022ab568aa2092644ee141eae3d1cc91112db7df477767`  
		Last Modified: Thu, 11 Jun 2026 00:23:57 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1695669bffc14e941ddcaea2183b96d282d1e2f1493cae8602a04ce029f9fbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5ab401af02b5b3df1d7bf4761cfffb1905c757a54cea3772b503cb76d94b4f`

```dockerfile
```

-	Layers:
	-	`sha256:870c02cc23f3a14902d04c2d100308087012c4027ff48abd1669a6bcc7761a85`  
		Last Modified: Thu, 11 Jun 2026 00:23:56 GMT  
		Size: 2.2 MB (2241375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad1019d4e40b5e9405ef3430519a8510ad1d33e6f33564b1da7c9afa54532ad`  
		Last Modified: Thu, 11 Jun 2026 00:23:56 GMT  
		Size: 17.3 KB (17304 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-trixie` - linux; 386

```console
$ docker pull julia@sha256:ee01ea0120b8e38bebe5d510727042304b8bfd9405a2f793f65536ebc6efdcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281066579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac86bff1a03e453e2c06f525171865e55e3a3ed13977c207dc53736f15b9fe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:18:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:18:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:18:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:18:47 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Thu, 11 Jun 2026 00:18:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:18:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:18:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:18:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb98f3b6c82ae8d48964356cdb0bb14d3998e6b28e3c99109ff31dbb1046b56`  
		Last Modified: Thu, 11 Jun 2026 00:19:20 GMT  
		Size: 6.4 MB (6435900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac9fb9a8eb7e6385d8fbe61b22c6edcca6e60a2b4eb60b8c4df0d246ddcbe5f`  
		Last Modified: Thu, 11 Jun 2026 00:19:28 GMT  
		Size: 243.3 MB (243329114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd1c086f61df7c03409a981e7268d9af1fdf14e6382655de57b27f3473afb33`  
		Last Modified: Thu, 11 Jun 2026 00:19:20 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:c8445ec83c5265e0afe93955f14098c596f4feaf73428a3415c433b9b97269c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2822c002d3a7d61e1e557adc44c8d43542052cacc909652d3c0c206dcd39e9`

```dockerfile
```

-	Layers:
	-	`sha256:dbd595df39cd4665ce160db31b8975d500f543a0de156bc268ec2c83a8a05481`  
		Last Modified: Thu, 11 Jun 2026 00:19:20 GMT  
		Size: 2.2 MB (2238210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de81d18bbd4888c14b34223bcfdc84da04cf4fb6fa9c169525aa46f02753000`  
		Last Modified: Thu, 11 Jun 2026 00:19:20 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json
