## `julia:bullseye`

```console
$ docker pull julia@sha256:8a5776a35daa3f5821996974b6bfccbca0acb93c57adb7be66f808fd48601b35
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
$ docker pull julia@sha256:72c9ae493b9eca82f0c07a276f2f0b4f7863d119474f66f8586eefa0a8053ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c67a903937f5891a72c30c6adc5ed4626c951909fa33c301f1aa5aa4c45948`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7165c83944224063d633634d136cf1bf62f390d866ccb2ae699c012548aac6`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.2 MB (2222654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725e528a3666541c2953691421b6a228673594440c7d539fb35f71fc2a46be48`  
		Last Modified: Tue, 11 Mar 2025 17:58:00 GMT  
		Size: 268.5 MB (268484444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d38f27ed12d5f890c2121a4a56d39f8767d3f6cbb1c14d39ddfbb22f45e415`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8a02228943143116153ce0d2488cd203e6ce948bb248949bcb0429c8686408b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91301a3221f1b9ae49dc24f7c05ad6161194f3e57f108ca52589d84115267526`

```dockerfile
```

-	Layers:
	-	`sha256:fc3a810a8f575b0ac14f3c720fac7a97fde163cba0299bdb59633c6e09cd7717`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7391d4ac599c40348906465dcc052d096f6db456615fe307bd2b39cb79da36c5`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dc6141754eb15dc1abb94a4e67d1c698f01f879691520bdc23842d794c80adda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314957093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f10b2054506b5f7fbdf5f4b4cc409f99caaf7ba0559d1ce43fcad496c62ed92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5dc01c337dce742e7c6026ccf096f7b1c09278ca05a29613e61d8fe553208`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.2 MB (2210309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47705c544b0c43fa505ea4141d20e1bd7047b8da8398c7a5e3d1214f40573e1`  
		Last Modified: Tue, 11 Mar 2025 17:59:35 GMT  
		Size: 284.0 MB (284000422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e906007b13ae7c53726d61e1006d643af01db9a126dcf54f834921cca9a146a`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:063ec1c56311e72dc3969d58c12069c7431f9663a075fb5fbca0ecea6b4fadb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8736a85ebdb295f549dc129bf2389633fae54193cc5512562d7d6452465fdb`

```dockerfile
```

-	Layers:
	-	`sha256:f153b82ac16be75d5ce35c461d4642790760c612f40500aba30fd809ff482f9d`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3990310fdd52100587e443fc54cd91ffdd102077037c0b0003599851c0c10ca7`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:415eda97c01612223e23e19484ef8c99744317636dc5c495c6a3ce456ce2c57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a238940033d7286786b0a0ebdb5f1de9242b3576a705221eccc3e647c6a3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768dc8869224f294d9e2ae8231a8c8a74f708a8e5495e183d94dfbedf98d3816`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.3 MB (2328071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4bd659adb5b6bdf7cd848dd04bdd531234e9725242266aa53357febdcb23a`  
		Last Modified: Tue, 11 Mar 2025 17:57:47 GMT  
		Size: 217.8 MB (217845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706ff1c0df0fa586527b601c6e9c2b526f2521b19a51b12649fedbc429419671`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:257c12809f8a9b581f7dde263775c80db30df53d4fcf13cd4fd1820599b3ce66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0464719ad93ca07e66b0669a89f783025f238fad94ecff01f027d6f292c6ea`

```dockerfile
```

-	Layers:
	-	`sha256:e12e0dd0133063f2b20338f66514bc5628916b5506a86b7491ad172daa119aab`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13c04845b43675f6fc2c6eb60313e14e089c471deb5b03bff80a58579050c65`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 17.2 KB (17195 bytes)  
		MIME: application/vnd.in-toto+json
