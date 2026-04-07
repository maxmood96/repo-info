## `julia:trixie`

```console
$ docker pull julia@sha256:57fd313df1d00f62bd21ceb4a1d530d0a53a53d04a84f14e1cb1bf5be79ee034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:trixie` - linux; amd64

```console
$ docker pull julia@sha256:8877544d9f298e969cf9938ecadba3f1f7486c426d24a45efa2c8ddc7b93809d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327476259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe1a7aa2ed7d9228586fa4471ba6e45308a20c02498ab72718005b7b3859ad8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:22:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 07 Apr 2026 01:22:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 07 Apr 2026 01:22:19 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 07 Apr 2026 01:22:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 07 Apr 2026 01:22:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:22:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:22:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b0bc01db768269d1282f831f035a818c63f284e15d137a1dacd9ccd50d851e`  
		Last Modified: Tue, 07 Apr 2026 01:22:59 GMT  
		Size: 6.2 MB (6247060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eaea49b72f684931f679a2ace26873eb1789d2dba3352e3cf0439d52678620`  
		Last Modified: Tue, 07 Apr 2026 01:23:10 GMT  
		Size: 291.5 MB (291453187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5601b82c88fa0d400e1487eb1e2f86ce8be24b8d46a4c0b8d3892626027574`  
		Last Modified: Tue, 07 Apr 2026 01:22:59 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:4f410bac0704a557e6ffd99797f10e4d7e20afddd476f29b50460bb039122ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35622fc86431b4128c5a95fda96e9e63fa8501d4a18fab1502680a34d4f2685`

```dockerfile
```

-	Layers:
	-	`sha256:4eafadd267d97909694bd0389d0ed8c2e58832eed2be0cb654b28c09d7326bea`  
		Last Modified: Tue, 07 Apr 2026 01:22:59 GMT  
		Size: 2.2 MB (2240259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bd729e3116e296ca9822ce85450584a7b0858e8f5ca76a949283d5a6a336178`  
		Last Modified: Tue, 07 Apr 2026 01:22:59 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:afc8ee820c4f2a724e5cc27134a9297312d1896d68559d87789b774534e7aa5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347546976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d34d854c8cdecfeb8a65fdbd4e4f08a7a231a82237eda5e4e56666da2473b21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 07 Apr 2026 01:21:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:21:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 07 Apr 2026 01:21:37 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 07 Apr 2026 01:21:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 07 Apr 2026 01:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1942f1b89988dad64aafe3423da5e52c0a6ad524ed7dad152a0c88682915d33`  
		Last Modified: Tue, 07 Apr 2026 01:22:23 GMT  
		Size: 6.2 MB (6154476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40afb279b80db4c7cfb6500eb16921b6237e2e5cfb40d244e62a1635d211e5ed`  
		Last Modified: Tue, 07 Apr 2026 01:22:31 GMT  
		Size: 311.3 MB (311253578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a456992e1bfdfb9f68ae75732853f6af852be8f2483a7c3339afc0b55c7b3a35`  
		Last Modified: Tue, 07 Apr 2026 01:22:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:fdba562d9493fef3f3b30ae1958958d13d6f9b774ca8524e2b6797a1e407cfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c5b8b19581f726b6f29978148987feb86ec0fd14a7a91a202cb858cc097ee2`

```dockerfile
```

-	Layers:
	-	`sha256:b477bbceda37192dce11a924db2c8cd9cca8e456484d9698bea5ded6fde4d710`  
		Last Modified: Tue, 07 Apr 2026 01:22:23 GMT  
		Size: 2.2 MB (2240591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab644e58ae9f156909c1cc43470ef1770a6b83b503f1f3358c6fb11aaf4c471`  
		Last Modified: Tue, 07 Apr 2026 01:22:22 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:962d78e99d3f95c5bec23fd1eaaf47c1a66a13430a918fa25954570444f2e95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268933573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a38ba8adbfc93a4001df60bbbb732c9e73221617944253ae2a8680ad591fc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 07 Apr 2026 01:18:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:18:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 07 Apr 2026 01:18:10 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 07 Apr 2026 01:18:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 07 Apr 2026 01:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:18:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce1f27a2975669231338ea7392707bfad311e6772e7ad198939bbe2209bcfd3`  
		Last Modified: Tue, 07 Apr 2026 01:18:42 GMT  
		Size: 6.4 MB (6433792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930647bddca64703e8099033e4b8596b34026c88a1e30f2ce9ad55c71e2bdc5c`  
		Last Modified: Tue, 07 Apr 2026 01:18:47 GMT  
		Size: 231.2 MB (231208156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77406c32aff326cf2b9c636836f7bb60428b64439cac662c1e3ef85822b849a`  
		Last Modified: Tue, 07 Apr 2026 01:18:42 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7169607a9dea42dd9180321a155ae6825e6b997d2076f96034ddb63cb0f0ac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c8f29309a5dda48399db9de7e0ab82f6edbece89dd705094990d9bbc3ae893`

```dockerfile
```

-	Layers:
	-	`sha256:774664774162f05eaabd521bed39118d42011b19be66c7a37a5fcb89076d04e0`  
		Last Modified: Tue, 07 Apr 2026 01:18:42 GMT  
		Size: 2.2 MB (2237384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c570542af8244f348e2fd23bd7e944e84b002975e61dd3f24996a92f1518dc6`  
		Last Modified: Tue, 07 Apr 2026 01:18:42 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json
