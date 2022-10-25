## `julia:buster`

```console
$ docker pull julia@sha256:89ce35e7e08b8132e6473ed76d21afa20025e89ee2acb0a8a1aa0ca1f8c392e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:fd095d1e93bebb2414c4ccaba895cbf68c9848c40ed65b90a6e1efe10a9c0b3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177437938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1c5f02099e85ab98d644c94796f3a7b38330da4716b128dbaa2551083c2ee6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:03:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:03:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 25 Oct 2022 04:03:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 04:03:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 25 Oct 2022 04:03:35 GMT
ENV JULIA_VERSION=1.8.2
# Tue, 25 Oct 2022 04:03:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 25 Oct 2022 04:03:53 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:03:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:03:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5802bde2e4692cd833ce202a6807b40af7441e290c91f1f6fd3af07d0d1de5f2`  
		Last Modified: Tue, 25 Oct 2022 04:05:55 GMT  
		Size: 4.5 MB (4469818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72161d5c513984a1b7d054760945f13091985502450dde21e47bc02e8536605`  
		Last Modified: Tue, 25 Oct 2022 04:06:17 GMT  
		Size: 145.8 MB (145826916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590d7096527945a5605b0c17bcb687da4cde3e2b35792f5519f2db3f6d055fcf`  
		Last Modified: Tue, 25 Oct 2022 04:05:55 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6f6958f79cbcf1b7c44ac0f07247c10d705f5a8400980d1989e379faa56f372c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169894450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607eff22a32556833d2752be6c62ccdd2e92dce2a623a7eb4629c9617eb9b16e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:01:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:01:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:01:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 20 Oct 2022 20:40:09 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 20 Oct 2022 20:40:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Oct 2022 20:40:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e410967f644c335c9ba4865ddc128a10c8a2ddaa2f87531730e0dc3cfd45e10`  
		Last Modified: Wed, 05 Oct 2022 03:04:03 GMT  
		Size: 4.3 MB (4346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8297636379925d4f7ea1fdac2965d49b5cac0c8b948da968e5bea62d5b0757`  
		Last Modified: Wed, 05 Oct 2022 03:04:23 GMT  
		Size: 139.6 MB (139635231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c83fb6c88ca729e484684e9d07cc7a39c4015e5169ab8a6645e265793260add`  
		Last Modified: Thu, 20 Oct 2022 20:41:20 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:35ee4ea9dc562a62b691fedc6ac614bc2fae788f4115285932c6ca5023dc857c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175135316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb59478e9d68ae42f3d5a7628a2b579eb0d09434e17da94ced457865588f55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:10:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:10:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:18 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 20 Oct 2022 20:38:45 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Thu, 20 Oct 2022 20:38:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Oct 2022 20:38:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796da4c51cacb791da540589b88d5bf127f182fb0d4eb46530ca9ff61ea44fbc`  
		Last Modified: Wed, 05 Oct 2022 02:12:49 GMT  
		Size: 4.6 MB (4616877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb28420c7c0fd820677e95822c0e1e9da492a9d8a6950338327051151adb5d`  
		Last Modified: Wed, 05 Oct 2022 02:13:06 GMT  
		Size: 142.7 MB (142720561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5227673c3e993de22ccce069344eba014e175d8cf665a3d27b977c56eed4d6a0`  
		Last Modified: Thu, 20 Oct 2022 20:39:59 GMT  
		Size: 377.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
