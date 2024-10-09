<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10.5`](#julia1105)
-	[`julia:1.10.5-bookworm`](#julia1105-bookworm)
-	[`julia:1.10.5-bullseye`](#julia1105-bullseye)
-	[`julia:1.10.5-windowsservercore`](#julia1105-windowsservercore)
-	[`julia:1.10.5-windowsservercore-1809`](#julia1105-windowsservercore-1809)
-	[`julia:1.10.5-windowsservercore-ltsc2022`](#julia1105-windowsservercore-ltsc2022)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11.0`](#julia1110)
-	[`julia:1.11.0-bookworm`](#julia1110-bookworm)
-	[`julia:1.11.0-bullseye`](#julia1110-bullseye)
-	[`julia:1.11.0-windowsservercore`](#julia1110-windowsservercore)
-	[`julia:1.11.0-windowsservercore-1809`](#julia1110-windowsservercore-1809)
-	[`julia:1.11.0-windowsservercore-ltsc2022`](#julia1110-windowsservercore-ltsc2022)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:953dea6eb7d5f820c621b14f661055d436ece5d21aef78de937fcab7e76196dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:7f1ea30c44d54a9e6c62826464004386a34f5d23c86d8a21804539f695ee7777
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
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:0ead6a1b95a86885b371febe6eaa67bf599880e2b2cd3de34a9505813573af2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:3189c0222570ec54eb4b841eae57a8608fd4f9ec9edd9a14540b9260c3d869fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6adb1c4e29da9b0db77b49b12f3cdb86f4f558956365c7771e2a14b295f6586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc211be43b941cc7bed9c1efe4f919b0601f547a5fbc6f0bbe1b8930e3b3334`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.4 MB (2426612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e659bb993041a09a231b20ad74957f1dde65addfb857777ed82f84c9a1aa99`  
		Last Modified: Wed, 09 Oct 2024 00:03:03 GMT  
		Size: 256.7 MB (256678724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c341be1dadb8314f2ddf31ee83f2f36b8aa832c9c7b2a11fe3b318cc28923`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:407e6865ec77aca6a2bb36eade6869492617a14c97461edbf242afd4194875e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf33dc5e61d7a2e38b5e593bc6c8a4d730fc4afcb3d523fda249792389b253c`

```dockerfile
```

-	Layers:
	-	`sha256:b00a888b1404f60813abf79309d0552a2a223ce66b295536956ef4a21a9c99c3`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.7 MB (2703142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bb48a49b1dce446afd847293b802c912383b7812811d80f1b3e222e4313b7b`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 17.0 KB (17029 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6e86a4843cca3beda39d329bceeca3b5a3f6c09e5a504828c325910aee5405b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285978592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f01c62f4afb077d528b72f5d1d2c0cdce1d15d33801743e7a5e7e62b0365e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a4c652dcb6e4589d9a0cc32c529a61a75e3f76b625e79053438c20d0f5d31`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.4 MB (2415138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edec0316fb8e0d5486508662dc676444bc4c8fdbc3f497dc4808fa9aa532e2e5`  
		Last Modified: Wed, 09 Oct 2024 00:12:36 GMT  
		Size: 253.5 MB (253487922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139c1c9276db7fa9a352b42b7e7a31b711f27329b6345cfd6ad74d105ffa769`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:75e0c340627d366e6e5d1b9007eb26a19d0b4ab609f921e75fd87f5395add5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd034322e6a91416242cbcc74a1c3cd03f9dc8325878df0abcef1846fd37003`

```dockerfile
```

-	Layers:
	-	`sha256:76e7c1b9e2823e50b79fe6130a733e6d9ff612cbd555a988cca8f5ac2d6d8c0c`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.7 MB (2703404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca20bf39129cc8626302ab268628257409909617223ad1a750d02864b0969af7`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 17.1 KB (17141 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:0be92a1464ae33a39b49ad6b69480f175f53ae755cd895b7e22785b18a632a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269413890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd33baadc292686a52f75034d4e79563db36fb012b51c2b454b593e49899689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c033560c807a67a65f22752c592cf61e48562e82d93642b101c86db6d67871`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.5 MB (2533016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a852befa831645253114ea7ea017a3f866d8cdae0f620077cf54c8e3b95819b`  
		Last Modified: Wed, 09 Oct 2024 00:02:57 GMT  
		Size: 234.5 MB (234467000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779f8328d72cd1cef3fe44a19e3033fbd3cc72502986798dabda96cc9a126`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1f754a87e8efc2c9e954363d3bdc622afa0149a1d3c3b5bbfbc297d39334c504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1dc590891a313455cf48d8bcb99d1adae6b3929815eb94acb4f373e3b2210f`

```dockerfile
```

-	Layers:
	-	`sha256:50a9335a97f4f82d99f4890789ee44b8848bfe0f1839001c62935973b7f14532`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.7 MB (2700240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10ac5795d098541e486a8c4c1d254f83cccbbc32b4df6dcbc14b1c599c55446`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:03c2584e54f7aec302ff3cf53455330392404ef88c83cd549449795ac55fea4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:4a1f6ea76a93a9b8956d5547a0869e9dbd4dc51de6d7e31b90906b5be035ec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc91138b8da18073cb65f800c851fd992881d9c0f177b10b20e7a0de12a92032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:b544097f9505726044eeea7d4ea64e886988db30f1ea21cb2522fd5005ae3e12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:f5b1927364c8bffee5822ba13667ca9e51f9923bd0fe33215d127551c06ca10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211247606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fe4756b7a451031d820120512cd66f08934250e4a9bcd0d9ba6f0e3828a165`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc6f44de6d0b704148b6bdf5cba037de7a43d64f5b5d4da4d8f23c7188990fa`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 5.7 MB (5712600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7134ce0f20e64a1c3bb8470ad7d72d78d14e84453ef931b3fa65b758e22231a0`  
		Last Modified: Fri, 27 Sep 2024 06:02:34 GMT  
		Size: 176.4 MB (176408361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258737ac35d22de0c0259d455441f0470dcb22df8f601561b874e68c02cead8e`  
		Last Modified: Fri, 27 Sep 2024 06:02:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:ff64efb663ff246078ce57c834e04c4968af4e63c0bae3314e614365a66e4672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae1a822bf2e640bf56997bf9ef7be7e2fafeeadb60613d1b793aa8b2c4f2053`

```dockerfile
```

-	Layers:
	-	`sha256:3619fc12db3a39c2a6585f87e26f0eaf0f5d7cd02cef0254cb885ec6a44add28`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 2.4 MB (2436737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b717e6747a6123300be6310eab9da09c48bf55afea4ee6a911f5d062acb54d43`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:21af0b797d4a18faef30cf721c98237115a90696640fe096edbfe828e9fec0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211925150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9296e0673b7953e84ab99026dbd77c95a63e7f50448f5b34646faaf4b3c5421`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf2cffac6bd44b0b139097cfe17e7b533b5a86fbffff9abfa0e088d1424142`  
		Last Modified: Fri, 27 Sep 2024 15:11:45 GMT  
		Size: 5.5 MB (5537204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241f999fe6317b6fb7daba481b6a7e7efc2178fc5c001ac3fbb8b259579bbb9`  
		Last Modified: Fri, 27 Sep 2024 15:14:29 GMT  
		Size: 177.2 MB (177231207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01158d4865186a9702739cd5cc69c9135ca0147f74a8178f83a6181ca14c99b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:ea16c3897f9dc8694b4a2629303a1bd1e9ff9c97d03da3274700f7b3414fdbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c898ae3a2f7c7c4be36b93d49880ce320cb4e9fd994bb2170d93c4d015e3d770`

```dockerfile
```

-	Layers:
	-	`sha256:9a70940517463f9332eda6f96174abaaa9888881e5802bb2be6ee83f579e032b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de7911dac3f6c11ec918dc086613e4a6d64f4f7194799a21e17071000ea5815`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 18.6 KB (18551 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:7f685fd0579c82e39f8f69bd3f2296d04afad594e2cf55a9701890515083616d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193816907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2155d9e2a0ff50655807a4faf3e4e403a0e90354494d2dbb3418b59a41a24d61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6223d248229dfac9f186a38958d0a6e92ea66920b20244f4f0bea36966a792`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 5.9 MB (5870471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660ffa6dccab120bd3667f6a32b461ae5528e92619c0074aa0e9e1dc137fe7f1`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 157.8 MB (157801853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b6a44c9f899c316b7e95a07ac6bdfb215e1c72550994ddaaa9c2f9e7f40fca`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:f6de79dc38320c97ea2c42c3b65953e6a1a30a1941370f65a24198b3536b6f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2451952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571df0fe87f29308420db7c8dac17210f5d98ae220667064c5e5eee9b8db6c3c`

```dockerfile
```

-	Layers:
	-	`sha256:922e6c24fac187deb8a3e592f9efa717103e5c33e6e42abf16e55d4e17e969e6`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 2.4 MB (2433809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4443a0afcd6cbee2d8984ef0d21623a7ecd12248b3b797d52b06c5b0de2c626`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 18.1 KB (18143 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:c3b36251da8d8c83cd217ac18130443a408548b8279d48154b1ee5014dd3a017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194508544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caa96bb80d430d9ed73663a3157346c2bdc86886c0ac16018affb09091a11ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d3f769447612a058b5c1c08f3172f0d9bb6db33422cef0d87b8ccac68c7fe3`  
		Last Modified: Fri, 27 Sep 2024 20:02:37 GMT  
		Size: 6.2 MB (6247915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8186a32770a1bf5e203bfd3ba49128632a5751f3c4f508a6fdf425b068a2787c`  
		Last Modified: Fri, 27 Sep 2024 20:05:11 GMT  
		Size: 155.1 MB (155138095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0166efa8f09f9d34637aa2d0452a81f5e2ef041a151bddefdd9abf4e607ea07`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:8b0832ee68678287a64245a7ec53b51f6ba74729b3b5c5c91f4299e6a78dbf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56864e26ded220a222e9cca8194cb8f2d10551c9a8a63782dbcce17bfba0978`

```dockerfile
```

-	Layers:
	-	`sha256:0460486f592911556e960f36da455b683b06d88a1ae8e0da55527dc7a23ea0b7`  
		Last Modified: Fri, 27 Sep 2024 20:05:07 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99edf4d20db000565a77363e73a5b6708ebf73999ebcdc62af58e827f0b797b2`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:f5b7a5d89a776a52654df6cdc2f453acb0a23d7d3f255995341b08e613c20fea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650770905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffaed81f3ddd0160dee4292b8760a00b15daa2284e6d7550809db7b474c8ff5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:06 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98c3a27050e21570df353f32e34737975c167124ff93b0aabcbcfebd6da02f`  
		Last Modified: Wed, 11 Sep 2024 00:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779194b4faf7d90e8b8103b561f6ca5fc3682a86eccd8e31a15cce8b5fee36f1`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74dec76cb2ab6e6ac2c4ca4f74778e51672e33cc296fabb2173e734ea3c1b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009491f9c893e7c5a3253f95583d0ecd8184a6454de6070a5a7cc1a89f17693`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcefd18a962d106ad9c0fc49b9dc5212671fb25eed18744837eb00e4fcab7b70`  
		Last Modified: Wed, 11 Sep 2024 00:03:40 GMT  
		Size: 188.6 MB (188572040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aaa1274fe7b347c3a0a7e742d9ae6fd44bd035eb50e3a1fe113217abc7989b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:2cab9a25c9d3bfe25aeaa95a6834b1c3b556983fc27d9c56ea4e75489090a653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908828121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214453b717c0ff79e61203d426a7f28735e6f86956dbcf4d5a519a3091f8ad79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:45 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e87ce4def28983a85a8feae259f722a11d49bc0b84d749b7e34913356dc95`  
		Last Modified: Wed, 11 Sep 2024 00:03:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953baccfb54d37992b9fb3999ffc13b8a8df9ec38a24cb180f50bda01624d623`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02261425b7f2c15a5ebc1110304f56df360da36ddad112dd5d9bcec1c672ec`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b4bdfffdbadfef9b29758beba56c09132c973f2416598b7bfbf95bc8e5f16`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab808b08890c898b38424587225b2749d4ee9161eabd606f013d23fef083d93`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 188.6 MB (188553269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d806365baa294ec32907681acaf995fb87ae4e5e5eca5c0117dd2f6ca50b`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:8013e5265728e9b176257bd9db73e52fcbabbfb22db66c384110d7acdf631186
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

### `julia:1.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:f5b1927364c8bffee5822ba13667ca9e51f9923bd0fe33215d127551c06ca10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211247606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fe4756b7a451031d820120512cd66f08934250e4a9bcd0d9ba6f0e3828a165`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc6f44de6d0b704148b6bdf5cba037de7a43d64f5b5d4da4d8f23c7188990fa`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 5.7 MB (5712600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7134ce0f20e64a1c3bb8470ad7d72d78d14e84453ef931b3fa65b758e22231a0`  
		Last Modified: Fri, 27 Sep 2024 06:02:34 GMT  
		Size: 176.4 MB (176408361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258737ac35d22de0c0259d455441f0470dcb22df8f601561b874e68c02cead8e`  
		Last Modified: Fri, 27 Sep 2024 06:02:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:ff64efb663ff246078ce57c834e04c4968af4e63c0bae3314e614365a66e4672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae1a822bf2e640bf56997bf9ef7be7e2fafeeadb60613d1b793aa8b2c4f2053`

```dockerfile
```

-	Layers:
	-	`sha256:3619fc12db3a39c2a6585f87e26f0eaf0f5d7cd02cef0254cb885ec6a44add28`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 2.4 MB (2436737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b717e6747a6123300be6310eab9da09c48bf55afea4ee6a911f5d062acb54d43`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:21af0b797d4a18faef30cf721c98237115a90696640fe096edbfe828e9fec0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211925150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9296e0673b7953e84ab99026dbd77c95a63e7f50448f5b34646faaf4b3c5421`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf2cffac6bd44b0b139097cfe17e7b533b5a86fbffff9abfa0e088d1424142`  
		Last Modified: Fri, 27 Sep 2024 15:11:45 GMT  
		Size: 5.5 MB (5537204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241f999fe6317b6fb7daba481b6a7e7efc2178fc5c001ac3fbb8b259579bbb9`  
		Last Modified: Fri, 27 Sep 2024 15:14:29 GMT  
		Size: 177.2 MB (177231207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01158d4865186a9702739cd5cc69c9135ca0147f74a8178f83a6181ca14c99b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:ea16c3897f9dc8694b4a2629303a1bd1e9ff9c97d03da3274700f7b3414fdbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c898ae3a2f7c7c4be36b93d49880ce320cb4e9fd994bb2170d93c4d015e3d770`

```dockerfile
```

-	Layers:
	-	`sha256:9a70940517463f9332eda6f96174abaaa9888881e5802bb2be6ee83f579e032b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de7911dac3f6c11ec918dc086613e4a6d64f4f7194799a21e17071000ea5815`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 18.6 KB (18551 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:7f685fd0579c82e39f8f69bd3f2296d04afad594e2cf55a9701890515083616d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193816907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2155d9e2a0ff50655807a4faf3e4e403a0e90354494d2dbb3418b59a41a24d61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6223d248229dfac9f186a38958d0a6e92ea66920b20244f4f0bea36966a792`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 5.9 MB (5870471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660ffa6dccab120bd3667f6a32b461ae5528e92619c0074aa0e9e1dc137fe7f1`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 157.8 MB (157801853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b6a44c9f899c316b7e95a07ac6bdfb215e1c72550994ddaaa9c2f9e7f40fca`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f6de79dc38320c97ea2c42c3b65953e6a1a30a1941370f65a24198b3536b6f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2451952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571df0fe87f29308420db7c8dac17210f5d98ae220667064c5e5eee9b8db6c3c`

```dockerfile
```

-	Layers:
	-	`sha256:922e6c24fac187deb8a3e592f9efa717103e5c33e6e42abf16e55d4e17e969e6`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 2.4 MB (2433809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4443a0afcd6cbee2d8984ef0d21623a7ecd12248b3b797d52b06c5b0de2c626`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 18.1 KB (18143 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:c3b36251da8d8c83cd217ac18130443a408548b8279d48154b1ee5014dd3a017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194508544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caa96bb80d430d9ed73663a3157346c2bdc86886c0ac16018affb09091a11ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d3f769447612a058b5c1c08f3172f0d9bb6db33422cef0d87b8ccac68c7fe3`  
		Last Modified: Fri, 27 Sep 2024 20:02:37 GMT  
		Size: 6.2 MB (6247915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8186a32770a1bf5e203bfd3ba49128632a5751f3c4f508a6fdf425b068a2787c`  
		Last Modified: Fri, 27 Sep 2024 20:05:11 GMT  
		Size: 155.1 MB (155138095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0166efa8f09f9d34637aa2d0452a81f5e2ef041a151bddefdd9abf4e607ea07`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8b0832ee68678287a64245a7ec53b51f6ba74729b3b5c5c91f4299e6a78dbf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56864e26ded220a222e9cca8194cb8f2d10551c9a8a63782dbcce17bfba0978`

```dockerfile
```

-	Layers:
	-	`sha256:0460486f592911556e960f36da455b683b06d88a1ae8e0da55527dc7a23ea0b7`  
		Last Modified: Fri, 27 Sep 2024 20:05:07 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99edf4d20db000565a77363e73a5b6708ebf73999ebcdc62af58e827f0b797b2`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:5b79789cbd15e34b5e5ba122367e7cc4fea382adfbc18fb02e7f1f348175ee13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a6d8661b0d89d9d228ea5550d4dd90012f8942104089e4d2e4d58a3a7cd0de9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210263386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed168594764546c640d12865de7c635d1cefe2949ee57b70ec586393ec1534fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182085a2bd4238e08dbca7e44c6afd4550c296cf5eb42de3ec5cf6302cafc03a`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 2.4 MB (2426535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d49b6582f95365a58fbcff58a62b9108a9fa6c7b62f0f6a5b06510ee6c61d`  
		Last Modified: Fri, 27 Sep 2024 06:02:25 GMT  
		Size: 176.4 MB (176407883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9056300b29b64f60977708108ea2170e4096f30710a05b7fbfe47def949c785`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f5414d7265071fd556d9ea4040f0a83f1f77d917c40b40a6ca28b5a815305df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000c50b764d4aca5dfda929e9aa18af7007d3500fa8efb7c67d1260ba905f328`

```dockerfile
```

-	Layers:
	-	`sha256:8225e188aa3325ca2d1d55f823b5b7fd73c7e939ac05fb50c9b91a3e6e0df434`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 2.7 MB (2704258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1353d2b7d50082fcfa16a5e0fa98954b4885702ed55486b467d5c75be048766b`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 17.0 KB (17024 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:87002f396c64aae9aa14134ae25f9002df8e98399ffa7541bc007aeab8f876e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209722190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb32505e3367989eba9fc2b68e0b1d90b3a6c9bac86e2232b771ba6e3eba6c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae16479b4a6d419166a62766e11d7cf55f343a8bc7fcd1395faf6d51d353af2c`  
		Last Modified: Fri, 27 Sep 2024 15:13:14 GMT  
		Size: 2.4 MB (2415175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269cfe61ae4b9bc51837c0323a6ecc829a2b38779855cdce6879ae23448b7f2`  
		Last Modified: Fri, 27 Sep 2024 15:15:36 GMT  
		Size: 177.2 MB (177231492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899b24b42e9b99fa3faf2fbaf1759237dbc9771fbc86182942026e406c70c5ef`  
		Last Modified: Fri, 27 Sep 2024 15:15:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b408dc85edca4f1603a0a69a254faba33415bf60bc131e3044bd163ef214c5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10973eb9eecc0a9050743aa1053453d73a4af94d3d05f026568b57c4c6a317ba`

```dockerfile
```

-	Layers:
	-	`sha256:b5aacb49c6de13b43b939cea21523c7b1cfc18865ad7eae8d921c67c0900da7f`  
		Last Modified: Fri, 27 Sep 2024 15:15:31 GMT  
		Size: 2.7 MB (2703404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e38dca020b464a09746058599800a845814701b266197533a8d69a0a0a8341a`  
		Last Modified: Fri, 27 Sep 2024 15:15:31 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4c7edccb102956cc93130349f095acec27597ab54dff0238f21e2ba56ac5b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192749376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baca23c74ea3d21522d749da975c4f5be81acfdd597e5078775244e551c21728`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cc83917d93d2e33fb8b8376cf95f1f52f3157c1a31c724ca2bbc678ba2432`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 2.5 MB (2533048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c23afe0d0e89bec70804015480f93d04b0d9c1e4111a0758f85fa7d941f39`  
		Last Modified: Fri, 27 Sep 2024 09:04:04 GMT  
		Size: 157.8 MB (157802460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc1b280e96af97557a62ff86230f0ab54bd446afb64cbc3fa7033708aa2ee9f`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:676fb71b6790dbc7286756b68b15e7848ecfbaf5302dc5cca6be3193983162fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23d74a66fd9ad651929c82135a3fea0bf14fab9a2fc7478dedf66b44f60a4ff`

```dockerfile
```

-	Layers:
	-	`sha256:5f100f4b5fd6aebaeb2f20577494908d87e6b8736df28a7dc3905eff51c2e364`  
		Last Modified: Fri, 27 Sep 2024 09:04:00 GMT  
		Size: 2.7 MB (2701356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0730af273b4ee412156504af7dd5f1cce5f50a0f0282d017a8fbbd2138d47939`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 17.0 KB (16992 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:c4fc77ea32ad538611320462a177287d2afeaf005cec47bcec0ef8f079ee3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:f5b7a5d89a776a52654df6cdc2f453acb0a23d7d3f255995341b08e613c20fea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650770905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffaed81f3ddd0160dee4292b8760a00b15daa2284e6d7550809db7b474c8ff5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:06 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98c3a27050e21570df353f32e34737975c167124ff93b0aabcbcfebd6da02f`  
		Last Modified: Wed, 11 Sep 2024 00:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779194b4faf7d90e8b8103b561f6ca5fc3682a86eccd8e31a15cce8b5fee36f1`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74dec76cb2ab6e6ac2c4ca4f74778e51672e33cc296fabb2173e734ea3c1b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009491f9c893e7c5a3253f95583d0ecd8184a6454de6070a5a7cc1a89f17693`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcefd18a962d106ad9c0fc49b9dc5212671fb25eed18744837eb00e4fcab7b70`  
		Last Modified: Wed, 11 Sep 2024 00:03:40 GMT  
		Size: 188.6 MB (188572040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aaa1274fe7b347c3a0a7e742d9ae6fd44bd035eb50e3a1fe113217abc7989b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:2cab9a25c9d3bfe25aeaa95a6834b1c3b556983fc27d9c56ea4e75489090a653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908828121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214453b717c0ff79e61203d426a7f28735e6f86956dbcf4d5a519a3091f8ad79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:45 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e87ce4def28983a85a8feae259f722a11d49bc0b84d749b7e34913356dc95`  
		Last Modified: Wed, 11 Sep 2024 00:03:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953baccfb54d37992b9fb3999ffc13b8a8df9ec38a24cb180f50bda01624d623`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02261425b7f2c15a5ebc1110304f56df360da36ddad112dd5d9bcec1c672ec`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b4bdfffdbadfef9b29758beba56c09132c973f2416598b7bfbf95bc8e5f16`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab808b08890c898b38424587225b2749d4ee9161eabd606f013d23fef083d93`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 188.6 MB (188553269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d806365baa294ec32907681acaf995fb87ae4e5e5eca5c0117dd2f6ca50b`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:071f99d2f752a692f95e646dcbac53d9c46147c6c07453b4b8eed3c6dfe949da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:2cab9a25c9d3bfe25aeaa95a6834b1c3b556983fc27d9c56ea4e75489090a653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908828121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214453b717c0ff79e61203d426a7f28735e6f86956dbcf4d5a519a3091f8ad79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:45 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e87ce4def28983a85a8feae259f722a11d49bc0b84d749b7e34913356dc95`  
		Last Modified: Wed, 11 Sep 2024 00:03:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953baccfb54d37992b9fb3999ffc13b8a8df9ec38a24cb180f50bda01624d623`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02261425b7f2c15a5ebc1110304f56df360da36ddad112dd5d9bcec1c672ec`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b4bdfffdbadfef9b29758beba56c09132c973f2416598b7bfbf95bc8e5f16`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab808b08890c898b38424587225b2749d4ee9161eabd606f013d23fef083d93`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 188.6 MB (188553269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d806365baa294ec32907681acaf995fb87ae4e5e5eca5c0117dd2f6ca50b`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:48ce2cee12549cb828316566cbedbd26803ee87933039787514d5a951a7459e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:f5b7a5d89a776a52654df6cdc2f453acb0a23d7d3f255995341b08e613c20fea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650770905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffaed81f3ddd0160dee4292b8760a00b15daa2284e6d7550809db7b474c8ff5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:06 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98c3a27050e21570df353f32e34737975c167124ff93b0aabcbcfebd6da02f`  
		Last Modified: Wed, 11 Sep 2024 00:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779194b4faf7d90e8b8103b561f6ca5fc3682a86eccd8e31a15cce8b5fee36f1`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74dec76cb2ab6e6ac2c4ca4f74778e51672e33cc296fabb2173e734ea3c1b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009491f9c893e7c5a3253f95583d0ecd8184a6454de6070a5a7cc1a89f17693`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcefd18a962d106ad9c0fc49b9dc5212671fb25eed18744837eb00e4fcab7b70`  
		Last Modified: Wed, 11 Sep 2024 00:03:40 GMT  
		Size: 188.6 MB (188572040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aaa1274fe7b347c3a0a7e742d9ae6fd44bd035eb50e3a1fe113217abc7989b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.5`

```console
$ docker pull julia@sha256:b544097f9505726044eeea7d4ea64e886988db30f1ea21cb2522fd5005ae3e12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.10.5` - linux; amd64

```console
$ docker pull julia@sha256:f5b1927364c8bffee5822ba13667ca9e51f9923bd0fe33215d127551c06ca10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211247606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fe4756b7a451031d820120512cd66f08934250e4a9bcd0d9ba6f0e3828a165`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc6f44de6d0b704148b6bdf5cba037de7a43d64f5b5d4da4d8f23c7188990fa`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 5.7 MB (5712600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7134ce0f20e64a1c3bb8470ad7d72d78d14e84453ef931b3fa65b758e22231a0`  
		Last Modified: Fri, 27 Sep 2024 06:02:34 GMT  
		Size: 176.4 MB (176408361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258737ac35d22de0c0259d455441f0470dcb22df8f601561b874e68c02cead8e`  
		Last Modified: Fri, 27 Sep 2024 06:02:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5` - unknown; unknown

```console
$ docker pull julia@sha256:ff64efb663ff246078ce57c834e04c4968af4e63c0bae3314e614365a66e4672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae1a822bf2e640bf56997bf9ef7be7e2fafeeadb60613d1b793aa8b2c4f2053`

```dockerfile
```

-	Layers:
	-	`sha256:3619fc12db3a39c2a6585f87e26f0eaf0f5d7cd02cef0254cb885ec6a44add28`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 2.4 MB (2436737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b717e6747a6123300be6310eab9da09c48bf55afea4ee6a911f5d062acb54d43`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:21af0b797d4a18faef30cf721c98237115a90696640fe096edbfe828e9fec0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211925150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9296e0673b7953e84ab99026dbd77c95a63e7f50448f5b34646faaf4b3c5421`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf2cffac6bd44b0b139097cfe17e7b533b5a86fbffff9abfa0e088d1424142`  
		Last Modified: Fri, 27 Sep 2024 15:11:45 GMT  
		Size: 5.5 MB (5537204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241f999fe6317b6fb7daba481b6a7e7efc2178fc5c001ac3fbb8b259579bbb9`  
		Last Modified: Fri, 27 Sep 2024 15:14:29 GMT  
		Size: 177.2 MB (177231207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01158d4865186a9702739cd5cc69c9135ca0147f74a8178f83a6181ca14c99b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5` - unknown; unknown

```console
$ docker pull julia@sha256:ea16c3897f9dc8694b4a2629303a1bd1e9ff9c97d03da3274700f7b3414fdbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c898ae3a2f7c7c4be36b93d49880ce320cb4e9fd994bb2170d93c4d015e3d770`

```dockerfile
```

-	Layers:
	-	`sha256:9a70940517463f9332eda6f96174abaaa9888881e5802bb2be6ee83f579e032b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de7911dac3f6c11ec918dc086613e4a6d64f4f7194799a21e17071000ea5815`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 18.6 KB (18551 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5` - linux; 386

```console
$ docker pull julia@sha256:7f685fd0579c82e39f8f69bd3f2296d04afad594e2cf55a9701890515083616d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193816907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2155d9e2a0ff50655807a4faf3e4e403a0e90354494d2dbb3418b59a41a24d61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6223d248229dfac9f186a38958d0a6e92ea66920b20244f4f0bea36966a792`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 5.9 MB (5870471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660ffa6dccab120bd3667f6a32b461ae5528e92619c0074aa0e9e1dc137fe7f1`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 157.8 MB (157801853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b6a44c9f899c316b7e95a07ac6bdfb215e1c72550994ddaaa9c2f9e7f40fca`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5` - unknown; unknown

```console
$ docker pull julia@sha256:f6de79dc38320c97ea2c42c3b65953e6a1a30a1941370f65a24198b3536b6f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2451952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571df0fe87f29308420db7c8dac17210f5d98ae220667064c5e5eee9b8db6c3c`

```dockerfile
```

-	Layers:
	-	`sha256:922e6c24fac187deb8a3e592f9efa717103e5c33e6e42abf16e55d4e17e969e6`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 2.4 MB (2433809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4443a0afcd6cbee2d8984ef0d21623a7ecd12248b3b797d52b06c5b0de2c626`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 18.1 KB (18143 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5` - linux; ppc64le

```console
$ docker pull julia@sha256:c3b36251da8d8c83cd217ac18130443a408548b8279d48154b1ee5014dd3a017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194508544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caa96bb80d430d9ed73663a3157346c2bdc86886c0ac16018affb09091a11ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d3f769447612a058b5c1c08f3172f0d9bb6db33422cef0d87b8ccac68c7fe3`  
		Last Modified: Fri, 27 Sep 2024 20:02:37 GMT  
		Size: 6.2 MB (6247915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8186a32770a1bf5e203bfd3ba49128632a5751f3c4f508a6fdf425b068a2787c`  
		Last Modified: Fri, 27 Sep 2024 20:05:11 GMT  
		Size: 155.1 MB (155138095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0166efa8f09f9d34637aa2d0452a81f5e2ef041a151bddefdd9abf4e607ea07`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5` - unknown; unknown

```console
$ docker pull julia@sha256:8b0832ee68678287a64245a7ec53b51f6ba74729b3b5c5c91f4299e6a78dbf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56864e26ded220a222e9cca8194cb8f2d10551c9a8a63782dbcce17bfba0978`

```dockerfile
```

-	Layers:
	-	`sha256:0460486f592911556e960f36da455b683b06d88a1ae8e0da55527dc7a23ea0b7`  
		Last Modified: Fri, 27 Sep 2024 20:05:07 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99edf4d20db000565a77363e73a5b6708ebf73999ebcdc62af58e827f0b797b2`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:f5b7a5d89a776a52654df6cdc2f453acb0a23d7d3f255995341b08e613c20fea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650770905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffaed81f3ddd0160dee4292b8760a00b15daa2284e6d7550809db7b474c8ff5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:06 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98c3a27050e21570df353f32e34737975c167124ff93b0aabcbcfebd6da02f`  
		Last Modified: Wed, 11 Sep 2024 00:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779194b4faf7d90e8b8103b561f6ca5fc3682a86eccd8e31a15cce8b5fee36f1`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74dec76cb2ab6e6ac2c4ca4f74778e51672e33cc296fabb2173e734ea3c1b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009491f9c893e7c5a3253f95583d0ecd8184a6454de6070a5a7cc1a89f17693`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcefd18a962d106ad9c0fc49b9dc5212671fb25eed18744837eb00e4fcab7b70`  
		Last Modified: Wed, 11 Sep 2024 00:03:40 GMT  
		Size: 188.6 MB (188572040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aaa1274fe7b347c3a0a7e742d9ae6fd44bd035eb50e3a1fe113217abc7989b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.5` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:2cab9a25c9d3bfe25aeaa95a6834b1c3b556983fc27d9c56ea4e75489090a653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908828121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214453b717c0ff79e61203d426a7f28735e6f86956dbcf4d5a519a3091f8ad79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:45 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e87ce4def28983a85a8feae259f722a11d49bc0b84d749b7e34913356dc95`  
		Last Modified: Wed, 11 Sep 2024 00:03:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953baccfb54d37992b9fb3999ffc13b8a8df9ec38a24cb180f50bda01624d623`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02261425b7f2c15a5ebc1110304f56df360da36ddad112dd5d9bcec1c672ec`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b4bdfffdbadfef9b29758beba56c09132c973f2416598b7bfbf95bc8e5f16`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab808b08890c898b38424587225b2749d4ee9161eabd606f013d23fef083d93`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 188.6 MB (188553269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d806365baa294ec32907681acaf995fb87ae4e5e5eca5c0117dd2f6ca50b`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.5-bookworm`

```console
$ docker pull julia@sha256:8013e5265728e9b176257bd9db73e52fcbabbfb22db66c384110d7acdf631186
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

### `julia:1.10.5-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:f5b1927364c8bffee5822ba13667ca9e51f9923bd0fe33215d127551c06ca10c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211247606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fe4756b7a451031d820120512cd66f08934250e4a9bcd0d9ba6f0e3828a165`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc6f44de6d0b704148b6bdf5cba037de7a43d64f5b5d4da4d8f23c7188990fa`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 5.7 MB (5712600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7134ce0f20e64a1c3bb8470ad7d72d78d14e84453ef931b3fa65b758e22231a0`  
		Last Modified: Fri, 27 Sep 2024 06:02:34 GMT  
		Size: 176.4 MB (176408361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258737ac35d22de0c0259d455441f0470dcb22df8f601561b874e68c02cead8e`  
		Last Modified: Fri, 27 Sep 2024 06:02:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:ff64efb663ff246078ce57c834e04c4968af4e63c0bae3314e614365a66e4672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae1a822bf2e640bf56997bf9ef7be7e2fafeeadb60613d1b793aa8b2c4f2053`

```dockerfile
```

-	Layers:
	-	`sha256:3619fc12db3a39c2a6585f87e26f0eaf0f5d7cd02cef0254cb885ec6a44add28`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 2.4 MB (2436737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b717e6747a6123300be6310eab9da09c48bf55afea4ee6a911f5d062acb54d43`  
		Last Modified: Fri, 27 Sep 2024 06:02:28 GMT  
		Size: 18.2 KB (18193 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:21af0b797d4a18faef30cf721c98237115a90696640fe096edbfe828e9fec0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211925150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9296e0673b7953e84ab99026dbd77c95a63e7f50448f5b34646faaf4b3c5421`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf2cffac6bd44b0b139097cfe17e7b533b5a86fbffff9abfa0e088d1424142`  
		Last Modified: Fri, 27 Sep 2024 15:11:45 GMT  
		Size: 5.5 MB (5537204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9241f999fe6317b6fb7daba481b6a7e7efc2178fc5c001ac3fbb8b259579bbb9`  
		Last Modified: Fri, 27 Sep 2024 15:14:29 GMT  
		Size: 177.2 MB (177231207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01158d4865186a9702739cd5cc69c9135ca0147f74a8178f83a6181ca14c99b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:ea16c3897f9dc8694b4a2629303a1bd1e9ff9c97d03da3274700f7b3414fdbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c898ae3a2f7c7c4be36b93d49880ce320cb4e9fd994bb2170d93c4d015e3d770`

```dockerfile
```

-	Layers:
	-	`sha256:9a70940517463f9332eda6f96174abaaa9888881e5802bb2be6ee83f579e032b`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de7911dac3f6c11ec918dc086613e4a6d64f4f7194799a21e17071000ea5815`  
		Last Modified: Fri, 27 Sep 2024 15:14:25 GMT  
		Size: 18.6 KB (18551 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5-bookworm` - linux; 386

```console
$ docker pull julia@sha256:7f685fd0579c82e39f8f69bd3f2296d04afad594e2cf55a9701890515083616d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193816907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2155d9e2a0ff50655807a4faf3e4e403a0e90354494d2dbb3418b59a41a24d61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6223d248229dfac9f186a38958d0a6e92ea66920b20244f4f0bea36966a792`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 5.9 MB (5870471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660ffa6dccab120bd3667f6a32b461ae5528e92619c0074aa0e9e1dc137fe7f1`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 157.8 MB (157801853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b6a44c9f899c316b7e95a07ac6bdfb215e1c72550994ddaaa9c2f9e7f40fca`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f6de79dc38320c97ea2c42c3b65953e6a1a30a1941370f65a24198b3536b6f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2451952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571df0fe87f29308420db7c8dac17210f5d98ae220667064c5e5eee9b8db6c3c`

```dockerfile
```

-	Layers:
	-	`sha256:922e6c24fac187deb8a3e592f9efa717103e5c33e6e42abf16e55d4e17e969e6`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 2.4 MB (2433809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4443a0afcd6cbee2d8984ef0d21623a7ecd12248b3b797d52b06c5b0de2c626`  
		Last Modified: Fri, 27 Sep 2024 09:03:53 GMT  
		Size: 18.1 KB (18143 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:c3b36251da8d8c83cd217ac18130443a408548b8279d48154b1ee5014dd3a017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194508544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caa96bb80d430d9ed73663a3157346c2bdc86886c0ac16018affb09091a11ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d3f769447612a058b5c1c08f3172f0d9bb6db33422cef0d87b8ccac68c7fe3`  
		Last Modified: Fri, 27 Sep 2024 20:02:37 GMT  
		Size: 6.2 MB (6247915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8186a32770a1bf5e203bfd3ba49128632a5751f3c4f508a6fdf425b068a2787c`  
		Last Modified: Fri, 27 Sep 2024 20:05:11 GMT  
		Size: 155.1 MB (155138095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0166efa8f09f9d34637aa2d0452a81f5e2ef041a151bddefdd9abf4e607ea07`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8b0832ee68678287a64245a7ec53b51f6ba74729b3b5c5c91f4299e6a78dbf8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56864e26ded220a222e9cca8194cb8f2d10551c9a8a63782dbcce17bfba0978`

```dockerfile
```

-	Layers:
	-	`sha256:0460486f592911556e960f36da455b683b06d88a1ae8e0da55527dc7a23ea0b7`  
		Last Modified: Fri, 27 Sep 2024 20:05:07 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99edf4d20db000565a77363e73a5b6708ebf73999ebcdc62af58e827f0b797b2`  
		Last Modified: Fri, 27 Sep 2024 20:05:06 GMT  
		Size: 18.3 KB (18257 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.5-bullseye`

```console
$ docker pull julia@sha256:5b79789cbd15e34b5e5ba122367e7cc4fea382adfbc18fb02e7f1f348175ee13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.5-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a6d8661b0d89d9d228ea5550d4dd90012f8942104089e4d2e4d58a3a7cd0de9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210263386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed168594764546c640d12865de7c635d1cefe2949ee57b70ec586393ec1534fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182085a2bd4238e08dbca7e44c6afd4550c296cf5eb42de3ec5cf6302cafc03a`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 2.4 MB (2426535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d49b6582f95365a58fbcff58a62b9108a9fa6c7b62f0f6a5b06510ee6c61d`  
		Last Modified: Fri, 27 Sep 2024 06:02:25 GMT  
		Size: 176.4 MB (176407883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9056300b29b64f60977708108ea2170e4096f30710a05b7fbfe47def949c785`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:f5414d7265071fd556d9ea4040f0a83f1f77d917c40b40a6ca28b5a815305df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000c50b764d4aca5dfda929e9aa18af7007d3500fa8efb7c67d1260ba905f328`

```dockerfile
```

-	Layers:
	-	`sha256:8225e188aa3325ca2d1d55f823b5b7fd73c7e939ac05fb50c9b91a3e6e0df434`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 2.7 MB (2704258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1353d2b7d50082fcfa16a5e0fa98954b4885702ed55486b467d5c75be048766b`  
		Last Modified: Fri, 27 Sep 2024 06:02:22 GMT  
		Size: 17.0 KB (17024 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:87002f396c64aae9aa14134ae25f9002df8e98399ffa7541bc007aeab8f876e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209722190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb32505e3367989eba9fc2b68e0b1d90b3a6c9bac86e2232b771ba6e3eba6c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae16479b4a6d419166a62766e11d7cf55f343a8bc7fcd1395faf6d51d353af2c`  
		Last Modified: Fri, 27 Sep 2024 15:13:14 GMT  
		Size: 2.4 MB (2415175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269cfe61ae4b9bc51837c0323a6ecc829a2b38779855cdce6879ae23448b7f2`  
		Last Modified: Fri, 27 Sep 2024 15:15:36 GMT  
		Size: 177.2 MB (177231492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899b24b42e9b99fa3faf2fbaf1759237dbc9771fbc86182942026e406c70c5ef`  
		Last Modified: Fri, 27 Sep 2024 15:15:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:b408dc85edca4f1603a0a69a254faba33415bf60bc131e3044bd163ef214c5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10973eb9eecc0a9050743aa1053453d73a4af94d3d05f026568b57c4c6a317ba`

```dockerfile
```

-	Layers:
	-	`sha256:b5aacb49c6de13b43b939cea21523c7b1cfc18865ad7eae8d921c67c0900da7f`  
		Last Modified: Fri, 27 Sep 2024 15:15:31 GMT  
		Size: 2.7 MB (2703404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e38dca020b464a09746058599800a845814701b266197533a8d69a0a0a8341a`  
		Last Modified: Fri, 27 Sep 2024 15:15:31 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.5-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4c7edccb102956cc93130349f095acec27597ab54dff0238f21e2ba56ac5b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192749376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baca23c74ea3d21522d749da975c4f5be81acfdd597e5078775244e551c21728`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 28 Aug 2024 05:59:11 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 28 Aug 2024 05:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 28 Aug 2024 05:59:11 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 28 Aug 2024 05:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.5-linux-x86_64.tar.gz'; 			sha256='33497b93cf9dd65e8431024fd1db19cbfbe30bd796775a59d53e2df9a8de6dc0'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.5-linux-aarch64.tar.gz'; 			sha256='59620a93cd64542d1f901ef9cfaecd310d0673b2bab2e2345774d456952a7ad0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.5-linux-i686.tar.gz'; 			sha256='508b573b0afc6427ce6b2bdfe471fcf86ff920383193aedb5fd6982bcb5cdb8a'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.5-linux-ppc64le.tar.gz'; 			sha256='80ccbe68d1bc5c1e971d526da463f8ecf62eb6ee81d4fd01345ccbe1e2a8833a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Aug 2024 05:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Aug 2024 05:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215cc83917d93d2e33fb8b8376cf95f1f52f3157c1a31c724ca2bbc678ba2432`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 2.5 MB (2533048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c23afe0d0e89bec70804015480f93d04b0d9c1e4111a0758f85fa7d941f39`  
		Last Modified: Fri, 27 Sep 2024 09:04:04 GMT  
		Size: 157.8 MB (157802460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc1b280e96af97557a62ff86230f0ab54bd446afb64cbc3fa7033708aa2ee9f`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.5-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:676fb71b6790dbc7286756b68b15e7848ecfbaf5302dc5cca6be3193983162fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23d74a66fd9ad651929c82135a3fea0bf14fab9a2fc7478dedf66b44f60a4ff`

```dockerfile
```

-	Layers:
	-	`sha256:5f100f4b5fd6aebaeb2f20577494908d87e6b8736df28a7dc3905eff51c2e364`  
		Last Modified: Fri, 27 Sep 2024 09:04:00 GMT  
		Size: 2.7 MB (2701356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0730af273b4ee412156504af7dd5f1cce5f50a0f0282d017a8fbbd2138d47939`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 17.0 KB (16992 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.5-windowsservercore`

```console
$ docker pull julia@sha256:c4fc77ea32ad538611320462a177287d2afeaf005cec47bcec0ef8f079ee3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.10.5-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:f5b7a5d89a776a52654df6cdc2f453acb0a23d7d3f255995341b08e613c20fea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650770905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffaed81f3ddd0160dee4292b8760a00b15daa2284e6d7550809db7b474c8ff5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:06 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98c3a27050e21570df353f32e34737975c167124ff93b0aabcbcfebd6da02f`  
		Last Modified: Wed, 11 Sep 2024 00:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779194b4faf7d90e8b8103b561f6ca5fc3682a86eccd8e31a15cce8b5fee36f1`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74dec76cb2ab6e6ac2c4ca4f74778e51672e33cc296fabb2173e734ea3c1b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009491f9c893e7c5a3253f95583d0ecd8184a6454de6070a5a7cc1a89f17693`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcefd18a962d106ad9c0fc49b9dc5212671fb25eed18744837eb00e4fcab7b70`  
		Last Modified: Wed, 11 Sep 2024 00:03:40 GMT  
		Size: 188.6 MB (188572040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aaa1274fe7b347c3a0a7e742d9ae6fd44bd035eb50e3a1fe113217abc7989b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.5-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:2cab9a25c9d3bfe25aeaa95a6834b1c3b556983fc27d9c56ea4e75489090a653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908828121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214453b717c0ff79e61203d426a7f28735e6f86956dbcf4d5a519a3091f8ad79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:45 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e87ce4def28983a85a8feae259f722a11d49bc0b84d749b7e34913356dc95`  
		Last Modified: Wed, 11 Sep 2024 00:03:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953baccfb54d37992b9fb3999ffc13b8a8df9ec38a24cb180f50bda01624d623`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02261425b7f2c15a5ebc1110304f56df360da36ddad112dd5d9bcec1c672ec`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b4bdfffdbadfef9b29758beba56c09132c973f2416598b7bfbf95bc8e5f16`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab808b08890c898b38424587225b2749d4ee9161eabd606f013d23fef083d93`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 188.6 MB (188553269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d806365baa294ec32907681acaf995fb87ae4e5e5eca5c0117dd2f6ca50b`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.5-windowsservercore-1809`

```console
$ docker pull julia@sha256:071f99d2f752a692f95e646dcbac53d9c46147c6c07453b4b8eed3c6dfe949da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `julia:1.10.5-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:2cab9a25c9d3bfe25aeaa95a6834b1c3b556983fc27d9c56ea4e75489090a653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908828121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214453b717c0ff79e61203d426a7f28735e6f86956dbcf4d5a519a3091f8ad79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:45 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e87ce4def28983a85a8feae259f722a11d49bc0b84d749b7e34913356dc95`  
		Last Modified: Wed, 11 Sep 2024 00:03:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953baccfb54d37992b9fb3999ffc13b8a8df9ec38a24cb180f50bda01624d623`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02261425b7f2c15a5ebc1110304f56df360da36ddad112dd5d9bcec1c672ec`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b4bdfffdbadfef9b29758beba56c09132c973f2416598b7bfbf95bc8e5f16`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab808b08890c898b38424587225b2749d4ee9161eabd606f013d23fef083d93`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 188.6 MB (188553269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d806365baa294ec32907681acaf995fb87ae4e5e5eca5c0117dd2f6ca50b`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.5-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:48ce2cee12549cb828316566cbedbd26803ee87933039787514d5a951a7459e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:1.10.5-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:f5b7a5d89a776a52654df6cdc2f453acb0a23d7d3f255995341b08e613c20fea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650770905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffaed81f3ddd0160dee4292b8760a00b15daa2284e6d7550809db7b474c8ff5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:06 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98c3a27050e21570df353f32e34737975c167124ff93b0aabcbcfebd6da02f`  
		Last Modified: Wed, 11 Sep 2024 00:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779194b4faf7d90e8b8103b561f6ca5fc3682a86eccd8e31a15cce8b5fee36f1`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74dec76cb2ab6e6ac2c4ca4f74778e51672e33cc296fabb2173e734ea3c1b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009491f9c893e7c5a3253f95583d0ecd8184a6454de6070a5a7cc1a89f17693`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcefd18a962d106ad9c0fc49b9dc5212671fb25eed18744837eb00e4fcab7b70`  
		Last Modified: Wed, 11 Sep 2024 00:03:40 GMT  
		Size: 188.6 MB (188572040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aaa1274fe7b347c3a0a7e742d9ae6fd44bd035eb50e3a1fe113217abc7989b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:953dea6eb7d5f820c621b14f661055d436ece5d21aef78de937fcab7e76196dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:7f1ea30c44d54a9e6c62826464004386a34f5d23c86d8a21804539f695ee7777
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

### `julia:1.11-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:0ead6a1b95a86885b371febe6eaa67bf599880e2b2cd3de34a9505813573af2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:3189c0222570ec54eb4b841eae57a8608fd4f9ec9edd9a14540b9260c3d869fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6adb1c4e29da9b0db77b49b12f3cdb86f4f558956365c7771e2a14b295f6586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc211be43b941cc7bed9c1efe4f919b0601f547a5fbc6f0bbe1b8930e3b3334`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.4 MB (2426612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e659bb993041a09a231b20ad74957f1dde65addfb857777ed82f84c9a1aa99`  
		Last Modified: Wed, 09 Oct 2024 00:03:03 GMT  
		Size: 256.7 MB (256678724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c341be1dadb8314f2ddf31ee83f2f36b8aa832c9c7b2a11fe3b318cc28923`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:407e6865ec77aca6a2bb36eade6869492617a14c97461edbf242afd4194875e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf33dc5e61d7a2e38b5e593bc6c8a4d730fc4afcb3d523fda249792389b253c`

```dockerfile
```

-	Layers:
	-	`sha256:b00a888b1404f60813abf79309d0552a2a223ce66b295536956ef4a21a9c99c3`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.7 MB (2703142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bb48a49b1dce446afd847293b802c912383b7812811d80f1b3e222e4313b7b`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 17.0 KB (17029 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6e86a4843cca3beda39d329bceeca3b5a3f6c09e5a504828c325910aee5405b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285978592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f01c62f4afb077d528b72f5d1d2c0cdce1d15d33801743e7a5e7e62b0365e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a4c652dcb6e4589d9a0cc32c529a61a75e3f76b625e79053438c20d0f5d31`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.4 MB (2415138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edec0316fb8e0d5486508662dc676444bc4c8fdbc3f497dc4808fa9aa532e2e5`  
		Last Modified: Wed, 09 Oct 2024 00:12:36 GMT  
		Size: 253.5 MB (253487922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139c1c9276db7fa9a352b42b7e7a31b711f27329b6345cfd6ad74d105ffa769`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:75e0c340627d366e6e5d1b9007eb26a19d0b4ab609f921e75fd87f5395add5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd034322e6a91416242cbcc74a1c3cd03f9dc8325878df0abcef1846fd37003`

```dockerfile
```

-	Layers:
	-	`sha256:76e7c1b9e2823e50b79fe6130a733e6d9ff612cbd555a988cca8f5ac2d6d8c0c`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.7 MB (2703404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca20bf39129cc8626302ab268628257409909617223ad1a750d02864b0969af7`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 17.1 KB (17141 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:0be92a1464ae33a39b49ad6b69480f175f53ae755cd895b7e22785b18a632a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269413890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd33baadc292686a52f75034d4e79563db36fb012b51c2b454b593e49899689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c033560c807a67a65f22752c592cf61e48562e82d93642b101c86db6d67871`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.5 MB (2533016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a852befa831645253114ea7ea017a3f866d8cdae0f620077cf54c8e3b95819b`  
		Last Modified: Wed, 09 Oct 2024 00:02:57 GMT  
		Size: 234.5 MB (234467000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779f8328d72cd1cef3fe44a19e3033fbd3cc72502986798dabda96cc9a126`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1f754a87e8efc2c9e954363d3bdc622afa0149a1d3c3b5bbfbc297d39334c504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1dc590891a313455cf48d8bcb99d1adae6b3929815eb94acb4f373e3b2210f`

```dockerfile
```

-	Layers:
	-	`sha256:50a9335a97f4f82d99f4890789ee44b8848bfe0f1839001c62935973b7f14532`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.7 MB (2700240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10ac5795d098541e486a8c4c1d254f83cccbbc32b4df6dcbc14b1c599c55446`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:03c2584e54f7aec302ff3cf53455330392404ef88c83cd549449795ac55fea4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:4a1f6ea76a93a9b8956d5547a0869e9dbd4dc51de6d7e31b90906b5be035ec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc91138b8da18073cb65f800c851fd992881d9c0f177b10b20e7a0de12a92032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.0`

```console
$ docker pull julia@sha256:953dea6eb7d5f820c621b14f661055d436ece5d21aef78de937fcab7e76196dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.11.0` - linux; amd64

```console
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.0` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.0-bookworm`

```console
$ docker pull julia@sha256:7f1ea30c44d54a9e6c62826464004386a34f5d23c86d8a21804539f695ee7777
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

### `julia:1.11.0-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0-bookworm` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.0-bullseye`

```console
$ docker pull julia@sha256:0ead6a1b95a86885b371febe6eaa67bf599880e2b2cd3de34a9505813573af2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.0-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:3189c0222570ec54eb4b841eae57a8608fd4f9ec9edd9a14540b9260c3d869fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6adb1c4e29da9b0db77b49b12f3cdb86f4f558956365c7771e2a14b295f6586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc211be43b941cc7bed9c1efe4f919b0601f547a5fbc6f0bbe1b8930e3b3334`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.4 MB (2426612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e659bb993041a09a231b20ad74957f1dde65addfb857777ed82f84c9a1aa99`  
		Last Modified: Wed, 09 Oct 2024 00:03:03 GMT  
		Size: 256.7 MB (256678724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c341be1dadb8314f2ddf31ee83f2f36b8aa832c9c7b2a11fe3b318cc28923`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:407e6865ec77aca6a2bb36eade6869492617a14c97461edbf242afd4194875e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf33dc5e61d7a2e38b5e593bc6c8a4d730fc4afcb3d523fda249792389b253c`

```dockerfile
```

-	Layers:
	-	`sha256:b00a888b1404f60813abf79309d0552a2a223ce66b295536956ef4a21a9c99c3`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.7 MB (2703142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bb48a49b1dce446afd847293b802c912383b7812811d80f1b3e222e4313b7b`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 17.0 KB (17029 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6e86a4843cca3beda39d329bceeca3b5a3f6c09e5a504828c325910aee5405b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285978592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f01c62f4afb077d528b72f5d1d2c0cdce1d15d33801743e7a5e7e62b0365e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a4c652dcb6e4589d9a0cc32c529a61a75e3f76b625e79053438c20d0f5d31`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.4 MB (2415138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edec0316fb8e0d5486508662dc676444bc4c8fdbc3f497dc4808fa9aa532e2e5`  
		Last Modified: Wed, 09 Oct 2024 00:12:36 GMT  
		Size: 253.5 MB (253487922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139c1c9276db7fa9a352b42b7e7a31b711f27329b6345cfd6ad74d105ffa769`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:75e0c340627d366e6e5d1b9007eb26a19d0b4ab609f921e75fd87f5395add5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd034322e6a91416242cbcc74a1c3cd03f9dc8325878df0abcef1846fd37003`

```dockerfile
```

-	Layers:
	-	`sha256:76e7c1b9e2823e50b79fe6130a733e6d9ff612cbd555a988cca8f5ac2d6d8c0c`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.7 MB (2703404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca20bf39129cc8626302ab268628257409909617223ad1a750d02864b0969af7`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 17.1 KB (17141 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.0-bullseye` - linux; 386

```console
$ docker pull julia@sha256:0be92a1464ae33a39b49ad6b69480f175f53ae755cd895b7e22785b18a632a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269413890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd33baadc292686a52f75034d4e79563db36fb012b51c2b454b593e49899689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c033560c807a67a65f22752c592cf61e48562e82d93642b101c86db6d67871`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.5 MB (2533016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a852befa831645253114ea7ea017a3f866d8cdae0f620077cf54c8e3b95819b`  
		Last Modified: Wed, 09 Oct 2024 00:02:57 GMT  
		Size: 234.5 MB (234467000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779f8328d72cd1cef3fe44a19e3033fbd3cc72502986798dabda96cc9a126`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.0-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1f754a87e8efc2c9e954363d3bdc622afa0149a1d3c3b5bbfbc297d39334c504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1dc590891a313455cf48d8bcb99d1adae6b3929815eb94acb4f373e3b2210f`

```dockerfile
```

-	Layers:
	-	`sha256:50a9335a97f4f82d99f4890789ee44b8848bfe0f1839001c62935973b7f14532`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.7 MB (2700240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10ac5795d098541e486a8c4c1d254f83cccbbc32b4df6dcbc14b1c599c55446`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.0-windowsservercore`

```console
$ docker pull julia@sha256:03c2584e54f7aec302ff3cf53455330392404ef88c83cd549449795ac55fea4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:1.11.0-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.0-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.0-windowsservercore-1809`

```console
$ docker pull julia@sha256:4a1f6ea76a93a9b8956d5547a0869e9dbd4dc51de6d7e31b90906b5be035ec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `julia:1.11.0-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.0-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc91138b8da18073cb65f800c851fd992881d9c0f177b10b20e7a0de12a92032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:1.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:7f1ea30c44d54a9e6c62826464004386a34f5d23c86d8a21804539f695ee7777
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
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:0ead6a1b95a86885b371febe6eaa67bf599880e2b2cd3de34a9505813573af2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:3189c0222570ec54eb4b841eae57a8608fd4f9ec9edd9a14540b9260c3d869fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290534309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6adb1c4e29da9b0db77b49b12f3cdb86f4f558956365c7771e2a14b295f6586`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc211be43b941cc7bed9c1efe4f919b0601f547a5fbc6f0bbe1b8930e3b3334`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.4 MB (2426612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e659bb993041a09a231b20ad74957f1dde65addfb857777ed82f84c9a1aa99`  
		Last Modified: Wed, 09 Oct 2024 00:03:03 GMT  
		Size: 256.7 MB (256678724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c341be1dadb8314f2ddf31ee83f2f36b8aa832c9c7b2a11fe3b318cc28923`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:407e6865ec77aca6a2bb36eade6869492617a14c97461edbf242afd4194875e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf33dc5e61d7a2e38b5e593bc6c8a4d730fc4afcb3d523fda249792389b253c`

```dockerfile
```

-	Layers:
	-	`sha256:b00a888b1404f60813abf79309d0552a2a223ce66b295536956ef4a21a9c99c3`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 2.7 MB (2703142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bb48a49b1dce446afd847293b802c912383b7812811d80f1b3e222e4313b7b`  
		Last Modified: Wed, 09 Oct 2024 00:02:55 GMT  
		Size: 17.0 KB (17029 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6e86a4843cca3beda39d329bceeca3b5a3f6c09e5a504828c325910aee5405b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285978592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121f01c62f4afb077d528b72f5d1d2c0cdce1d15d33801743e7a5e7e62b0365e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a4c652dcb6e4589d9a0cc32c529a61a75e3f76b625e79053438c20d0f5d31`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.4 MB (2415138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edec0316fb8e0d5486508662dc676444bc4c8fdbc3f497dc4808fa9aa532e2e5`  
		Last Modified: Wed, 09 Oct 2024 00:12:36 GMT  
		Size: 253.5 MB (253487922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139c1c9276db7fa9a352b42b7e7a31b711f27329b6345cfd6ad74d105ffa769`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:75e0c340627d366e6e5d1b9007eb26a19d0b4ab609f921e75fd87f5395add5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd034322e6a91416242cbcc74a1c3cd03f9dc8325878df0abcef1846fd37003`

```dockerfile
```

-	Layers:
	-	`sha256:76e7c1b9e2823e50b79fe6130a733e6d9ff612cbd555a988cca8f5ac2d6d8c0c`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 2.7 MB (2703404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca20bf39129cc8626302ab268628257409909617223ad1a750d02864b0969af7`  
		Last Modified: Wed, 09 Oct 2024 00:12:27 GMT  
		Size: 17.1 KB (17141 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:0be92a1464ae33a39b49ad6b69480f175f53ae755cd895b7e22785b18a632a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269413890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd33baadc292686a52f75034d4e79563db36fb012b51c2b454b593e49899689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:23 GMT
ADD file:176ca55c782e88e529d56f56999487b261e37eaa9b59fcfdf2b400ed60a31a55 in / 
# Fri, 27 Sep 2024 07:23:24 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5306a3a8e6d3817e237e681e3f75f332f8a6ba35c1f365dcff9af549d9f45234`  
		Last Modified: Fri, 27 Sep 2024 07:27:50 GMT  
		Size: 32.4 MB (32413499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c033560c807a67a65f22752c592cf61e48562e82d93642b101c86db6d67871`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.5 MB (2533016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a852befa831645253114ea7ea017a3f866d8cdae0f620077cf54c8e3b95819b`  
		Last Modified: Wed, 09 Oct 2024 00:02:57 GMT  
		Size: 234.5 MB (234467000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc779f8328d72cd1cef3fe44a19e3033fbd3cc72502986798dabda96cc9a126`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:1f754a87e8efc2c9e954363d3bdc622afa0149a1d3c3b5bbfbc297d39334c504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1dc590891a313455cf48d8bcb99d1adae6b3929815eb94acb4f373e3b2210f`

```dockerfile
```

-	Layers:
	-	`sha256:50a9335a97f4f82d99f4890789ee44b8848bfe0f1839001c62935973b7f14532`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 2.7 MB (2700240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10ac5795d098541e486a8c4c1d254f83cccbbc32b4df6dcbc14b1c599c55446`  
		Last Modified: Wed, 09 Oct 2024 00:02:47 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:953dea6eb7d5f820c621b14f661055d436ece5d21aef78de937fcab7e76196dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:ef1061e4b63208225976c970282780614fdfd024cd6ac43b0d27dc40e7d040db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291517947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a66a0b02f60bd0db2206a80dbf319e903df574d1d1c9a93fb73ae5b9ca10fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7482166de8331086f3ddaeb838040e8ee91451c4b08bbd83c6eca3957448e4b`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 5.7 MB (5712655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8880db6fced3305ee65d0c2c781c7d0c2b6a882373fa08f31ba7ddb8ee41215`  
		Last Modified: Wed, 09 Oct 2024 00:02:58 GMT  
		Size: 256.7 MB (256678643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264c1c93a38ff42a99a29f8bcd7a5f0bb71b23ff16c3b94931a2139f8244764c`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:a74e0d8bb17a6334c719547c2af27d0ac0aaa77bbc1ac23b1b5b8cdec05aa622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3cd19fe51a8bcded7cb46bb15659f763d4bf6f78ba07a925ec60665f695b2a`

```dockerfile
```

-	Layers:
	-	`sha256:91b2fadeb06f9c561c3ffc58da131ec3ebe4fbc010eeb5da903a13c7ac7bc182`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 2.4 MB (2435621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c859cb832efa59109bb4ad4b82a89821dda4dde2dd611d9faf57e34bc67de8`  
		Last Modified: Wed, 09 Oct 2024 00:02:52 GMT  
		Size: 18.2 KB (18174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:154329ae1b7c6a298465a1919338a8b16769cddba796ba670e90395eb93b31de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288181842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c59866d3e8789af6f81e780a705202415ea2f8cd70a8819917fac60d1a6b98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72317c252662678f8f92370f6eda3dff70a8eb6c3e973c3a370b91db599f0a08`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 5.5 MB (5537189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45a167527588a6609faace3996075e7d8a724fe93cd1944f518e5aea5cf4668`  
		Last Modified: Wed, 09 Oct 2024 00:10:59 GMT  
		Size: 253.5 MB (253487910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c80de7b80146917a0a9a1dfe1cbcb2193a93be234e8ee25353af2bad3c888b`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:0367a13841bb6711e3b7ca7a2671cafe5ad6de1a499f1727c2a38385367f6b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2997fe4e20e5241923596a007050921c9359bbbabfff1738351a2cdbca3ca5`

```dockerfile
```

-	Layers:
	-	`sha256:6854dc4d2df31d53f370aee64fa506699aeb929643e5b766cf6c39c2070eeb3d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 2.4 MB (2435943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c23ea572a30521fc47834f0071393529f85733acfba98655f3847357567b63d`  
		Last Modified: Wed, 09 Oct 2024 00:10:53 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:78d9e4a20fbda7d9dc88bb1eb62988ac513519950d47d79e3ac708354d5ecea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1ca41cabad9c1246f4f89ee4a7dd7741e0dccbea708cdab0ee13f62fd2bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deacb2dfd23fd7bc8cc145024202399d74e31928ffd15252bdb54891a58b767`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 5.9 MB (5870465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31deb0e4b398374ba55ae195a2fc235979bc408f1656443ec59f778c19f54918`  
		Last Modified: Wed, 09 Oct 2024 00:02:49 GMT  
		Size: 234.5 MB (234466942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258682ba71d979d6125ed75e39a7633ad857c30ba348d65f16fe06021f9a921f`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:9faa754508a96e17e28c8c46f65d48c3ed16c40490975f7f5414e8d4633ec6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce9094c16318b7b356c7da8527e0181ef1bcbaca13da14ba2a5d3e728935a6a`

```dockerfile
```

-	Layers:
	-	`sha256:80e07a46bf3b6e17d8f11bc36657204bfc4431271090bd6363c18fe146cbe373`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 2.4 MB (2432693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999a47f4d98e025d412ae49c30af611e5e8f6ea03ca1a6d24dd672dff1d3e35b`  
		Last Modified: Wed, 09 Oct 2024 00:02:44 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:fd0dbcbf8f18cf12b9ca6e129ebf0545041f9054154f465b23f374062b5528fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284126925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedda1b2780a46d74f1a4cbcd8eea972ddb31dad889f8da3f625da7f207cba20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 07 Oct 2024 23:59:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 07 Oct 2024 23:59:18 GMT
ENV JULIA_VERSION=1.11.0
# Mon, 07 Oct 2024 23:59:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-linux-x86_64.tar.gz'; 			sha256='bcf815553fda2ed7910524c8caa189c8e8191a40a799dd8b5fbed0d9dd6b882c'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-linux-aarch64.tar.gz'; 			sha256='66b9195b4c6b85403834dca9ef4fcae75f15be906bb3bb2c48eccb780ab810a1'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-linux-i686.tar.gz'; 			sha256='b4088274ca31ed3c58fa6f4d0f3887b0610ea38e1aa87000993cb24900c773aa'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-linux-ppc64le.tar.gz'; 			sha256='6fc3981aded87517b9b6515e0ce9d56d2889c0ffef1e1646bb44808e57cb3276'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Oct 2024 23:59:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Oct 2024 23:59:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad53db1f464e67ec1c1268a52973618375eac7b8a9164cbf6157e2936154ad`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 6.2 MB (6247852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8792363c65b33c5655a083d753e2498e02f53cac94ff58064d7926e7ab65d1b4`  
		Last Modified: Wed, 09 Oct 2024 00:12:39 GMT  
		Size: 244.8 MB (244756538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6d60f82df055f88245b349e1893e4dea871299b659c84a29d73ad7f62929b`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:3d66025a232ef5fa50ac87819e6f1c3a4904c863b32864c492c105f62e50191b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13515c31a3183ea9be2914d469eee55fd8add79c935a453f6ca9e01f0f4a3a`

```dockerfile
```

-	Layers:
	-	`sha256:277955b4720c3b446f5c93c96981768e2279efe2ad94b99015667501213ecbc2`  
		Last Modified: Wed, 09 Oct 2024 00:12:33 GMT  
		Size: 2.4 MB (2440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bbb1c273c897e6a1fe7cadbbb5fb1426775295fe30dd67179aadd117c44adf1`  
		Last Modified: Wed, 09 Oct 2024 00:12:32 GMT  
		Size: 18.3 KB (18263 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:03c2584e54f7aec302ff3cf53455330392404ef88c83cd549449795ac55fea4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:4a1f6ea76a93a9b8956d5547a0869e9dbd4dc51de6d7e31b90906b5be035ec55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:1db3b6bcf914c231e87055b43f570951f9bd5cf6287105a5cd3c80a9ec1d5d08
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972980770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e7a90fdae55aaac2e4f191bc17f0bf8d403824783f1529d4daeb6a58c0f11`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 09 Oct 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:58 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:02:00 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cce082b59faf3eb447c7759e475e5e4c4654a0a058234a4af0532dd6987618`  
		Last Modified: Wed, 09 Oct 2024 00:04:23 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fb80305cdcb8f0150233eac7ee4f6a6b351ced44c9b6bbc7d856f901dddfef`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09550b288e5c98b3ea16120a0d3d528d33395ece218b44f90f0d2fda2d862d7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64632b10d230c316ca4d10ecda13e563b055ab53887d8a74f8b9fd93c167f5a8`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab4c72716ac34984beb07744944388a11efa2f4fe5faf2dd324361e8dbf2a0`  
		Last Modified: Wed, 09 Oct 2024 00:04:52 GMT  
		Size: 252.7 MB (252705900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:859323bd9bed80752e644ae240948117b50a8e4e4511836e6b7884059845ecc7`  
		Last Modified: Wed, 09 Oct 2024 00:04:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc91138b8da18073cb65f800c851fd992881d9c0f177b10b20e7a0de12a92032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
