## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:df9b6e4cb05bb8b32b7f6b05c8f094b346e79ae4b43519c91542b0c434af598a
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
$ docker pull julia@sha256:ca55b7cba75dae6bc580ee3241b93aae3229d3f83d085a7c2f97e231a42cc2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342720766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cf4c5b83337c0575d6536087b9044663ef8f414926dd9c31303ba22dc68964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 17:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:45:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Feb 2026 17:45:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:45:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Feb 2026 17:45:01 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Thu, 05 Feb 2026 17:45:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Feb 2026 17:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 17:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:45:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1432c6dfddcd202404bbb94d95ca9783fadf4c3c8ec842df17a6450d5a7e4c1`  
		Last Modified: Thu, 05 Feb 2026 17:45:46 GMT  
		Size: 5.7 MB (5718013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca82b21999a70981ea576f11311f2b708f8b7e8b7dcd78cb1a7a2e4d762160b`  
		Last Modified: Thu, 05 Feb 2026 17:45:53 GMT  
		Size: 308.8 MB (308773893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344480c41ec23ce44c18b2ec2958b40dce046190f513e6b250d784ac426bc5c4`  
		Last Modified: Thu, 05 Feb 2026 17:45:46 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:4e835f35f30415499651617d87306f728bddf0edb3e4322a7ddfc07c4fbcee4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e9e5de14feba275d30bb6dc10d30e114a07f9163742f7bc683eece957c1254`

```dockerfile
```

-	Layers:
	-	`sha256:ea4919c3ac310a7b409695a70dbb55e995dfad5840bee95729497847bca6c87b`  
		Last Modified: Thu, 05 Feb 2026 17:45:46 GMT  
		Size: 2.6 MB (2568624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89580e0fc6133fac997834ec94ffbc0cdd9fe691f83e770cbf7810733f4271b`  
		Last Modified: Thu, 05 Feb 2026 17:45:46 GMT  
		Size: 16.3 KB (16318 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:faaee3dfae4c2ac67792104548b4ccbf85e24d1d4418987b2f2dbf0b4cdfdf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366408189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a55f94f888724717be4b69a420af4b917b3fedf0a8f8db70c725f53671447c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 17:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:44:45 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Feb 2026 17:44:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:44:45 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Feb 2026 17:44:45 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Thu, 05 Feb 2026 17:44:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Feb 2026 17:44:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 17:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:44:45 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a278b73cb1804d5b09e504fd4ba645ab653ece0340c0a95963598d30dabaae`  
		Last Modified: Thu, 05 Feb 2026 17:45:32 GMT  
		Size: 5.6 MB (5567854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6763a40da291cbc90ad225befd967bedfc196d1903a2be86d7f81591fb1ba11c`  
		Last Modified: Thu, 05 Feb 2026 17:45:38 GMT  
		Size: 332.7 MB (332732141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d5a0bb75cc89c45c4c6129b62a11cc2672ef7da56b49e5c6b81dbaa0498d7d`  
		Last Modified: Thu, 05 Feb 2026 17:45:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:69d4c4b4698d647691a0f534d1661df997fa490258efd1d75c82bcb0bc8c8137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc7b8c7ab0685e98e1cd68abbb91fd50591b9665d752aa5afa8a237d309b365`

```dockerfile
```

-	Layers:
	-	`sha256:07b96677e300a7009ae9600f210cd1fe7a671b2c8584338e15db93ad41d0ba9a`  
		Last Modified: Thu, 05 Feb 2026 17:45:32 GMT  
		Size: 2.6 MB (2568887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98bfe4a42cd20d6a65e410cf0902d6e22ff24c1b25acfa56024d239ef141a8da`  
		Last Modified: Thu, 05 Feb 2026 17:45:32 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:7ab406d995916b330b77395b77fce5130a6f7a698f29526ec25626fd12632c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278015494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d3fb17d79449d4007ac14d2125a12be5ba8680879b2ef9ae18628629312e43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 17:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 17:45:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Feb 2026 17:45:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:45:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Feb 2026 17:45:35 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Thu, 05 Feb 2026 17:45:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta2-linux-x86_64.tar.gz'; 			sha256='a12587225ccacf8988a3473535e73c7007223c5e3dba82ddce4efee2bf22db9a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta2-linux-i686.tar.gz'; 			sha256='ec17bf167ea51e7ffd7604e03c5c7fb8eb235e2cdf78f45a25cce8151cfd784c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta2-linux-aarch64.tar.gz'; 			sha256='2b0f8e396a0add65525daa038daadec3ee9f82b9ba02f09a4a59d6979202b932'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Feb 2026 17:45:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 17:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 17:45:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a759946b036ec349f0beeb2994cb18d1bf905fa1367bf428c7148ec6f5f028`  
		Last Modified: Thu, 05 Feb 2026 17:46:10 GMT  
		Size: 5.9 MB (5878793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185b09af466886688ae251590d5acb251ec2c4b6d3979fb6c069be820c35917`  
		Last Modified: Thu, 05 Feb 2026 17:46:14 GMT  
		Size: 242.9 MB (242926316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32fa5046a0e3a0c1227cc2ae3df8d042ebd8b870a20246fb3f749781c70c69d`  
		Last Modified: Thu, 05 Feb 2026 17:46:09 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:155f6d6e89ecff2c6f8a40d5d870ae9a6a30e8daf36bef3fa216e9c23468eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a898740a98a78585949bab98d6e4101b735a3b55088d4144b4383f66b8a9b2`

```dockerfile
```

-	Layers:
	-	`sha256:4edda32bb5454097ec4a999bcdca867f0a275e42a19f0527ae0dc35674cffdb9`  
		Last Modified: Thu, 05 Feb 2026 17:46:10 GMT  
		Size: 2.6 MB (2565776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457a408a16c3d1f487aa4c210a5401e27a50a62decbf556544af01d8aae9b349`  
		Last Modified: Thu, 05 Feb 2026 17:46:09 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
