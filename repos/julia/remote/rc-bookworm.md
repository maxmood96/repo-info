## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:e21fb3aadcd338b9fe9bfd4d0f65e15e5fca31d5e8cc4fa01b01abdc8d4e61d5
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
$ docker pull julia@sha256:57dc51ff330a3729ed55fc5b76d6f8656d0d15dd134b1ad49625c374b02a0e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319597570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1ee63776f85c91a389761dbed681493426f384fcdeb50f9ae5223e71eb913f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 28 Sep 2025 11:59:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Fri, 28 Nov 2025 23:55:38 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9786dac152393dc2f83ae9af2611f299dec3f6bb1e9a03a6320f62b1face72e2`  
		Last Modified: Mon, 29 Sep 2025 23:55:04 GMT  
		Size: 5.7 MB (5716166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0607df4accadab64cd77f38ec0995d4bf2e5acf1da627ddb7e2e1812105c3e`  
		Last Modified: Mon, 29 Sep 2025 23:55:11 GMT  
		Size: 285.7 MB (285652697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6a7c5ebd73464deb4167d3635ca7e9f34f0673803f1d5856c081df1826ef4b`  
		Last Modified: Mon, 29 Sep 2025 23:55:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:785104cad43da4f80db1f92a6d5e2632bbef41fbd9ff34c36b82f88597e309e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5702051671c5e9e847eb7afc44ecbb8094953e673ed1b82740ac250139699341`

```dockerfile
```

-	Layers:
	-	`sha256:f472150a65524da27208fa402e9558105cb45ab032758a8adba9dae2e5059000`  
		Last Modified: Mon, 29 Sep 2025 23:55:04 GMT  
		Size: 2.6 MB (2567402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771e3eb2eb7bd7e2790f13e46cf7a02515bccdc9e1954296aaeed23c08a9b14b`  
		Last Modified: Mon, 29 Sep 2025 23:55:04 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a802f91d92457c59054704a8b333d2dfeafb46e7d9d7bece6fb1afcd7d1fafd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339214194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1d2be331ba057d8f60eeab73c71a8876b5e19730712717749c4131fadfb2fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 28 Sep 2025 11:59:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Fri, 28 Nov 2025 23:57:51 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d41ea68355683aecdc550a342269ce801e411063e1270506a9bdd59a297950`  
		Last Modified: Mon, 29 Sep 2025 23:55:29 GMT  
		Size: 5.6 MB (5567129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3e336974beb9bcf02f5fea000e20556db3bad70df173a7867e91197ce32d9`  
		Last Modified: Mon, 29 Sep 2025 23:55:35 GMT  
		Size: 305.5 MB (305544548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e0538872bcf564465f9e739438e201266a122479fddffd104cc2d671469626`  
		Last Modified: Mon, 29 Sep 2025 23:55:29 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7f368373a405ed5d76448adfb784e965cfd8fa2aed56158d0d2440029599ece3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27500e10aa72afcf7dbe6a6ed0e9a9bdc709176df761ceb40b7b3579d3129e6e`

```dockerfile
```

-	Layers:
	-	`sha256:6f1f97ffe0c93d130ffd6c64119dfdd13ff05b79514362055b1d2e7f41e41ace`  
		Last Modified: Mon, 29 Sep 2025 23:55:29 GMT  
		Size: 2.6 MB (2567665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da82c899a5e7a100774e3fc38f53342aa269669611acbdc106d13abd328803fd`  
		Last Modified: Mon, 29 Sep 2025 23:55:29 GMT  
		Size: 16.5 KB (16459 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:bc30d013694b7b834dab814434a7fff2beb9052eb787e91d9ca7d0ca6520342e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264821982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557aa8c557fc902794f898cb14904f4e8d51cc8be506883c25d31524dc8b3e42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sun, 28 Sep 2025 11:59:29 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Sun, 28 Sep 2025 11:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sun, 28 Sep 2025 11:59:29 GMT
ENV JULIA_VERSION=1.12.0-rc3
# Sun, 28 Sep 2025 11:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc3-linux-x86_64.tar.gz'; 			sha256='d89d6483c141160d893d71bd1ab87f6d56bc8d5762c35093c7644c3cbc1a9d1d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc3-linux-aarch64.tar.gz'; 			sha256='1dfb20c6beaa1c4dbfbf6e8168b74e213023367990e35003d6b35d83579f0b11'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc3-linux-i686.tar.gz'; 			sha256='372fcd8135e0836394d8e0c5ab7ef4f768b91f3613c4f807a7bf71470893b7ac'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 28 Sep 2025 11:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 28 Sep 2025 11:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Sat, 29 Nov 2025 15:11:04 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e15757babd691f1d0d9dd8d6604144b3699f6c2824b82c09789133435218914`  
		Last Modified: Mon, 29 Sep 2025 23:55:18 GMT  
		Size: 5.9 MB (5878012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83111c9ccdb2287ef3272f554bbe8682b27516878b08647ba8d6cf20e29ab16b`  
		Last Modified: Mon, 29 Sep 2025 23:55:26 GMT  
		Size: 229.7 MB (229733968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea264aba2c72ba170589822c1b07318e46f63dfaad5c176ae2b37d928686597`  
		Last Modified: Mon, 29 Sep 2025 23:55:18 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f7014d6c88cf4ee72269444961b74ef51eb34976d68c8734c175d8087d018191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3010eedf5dc119cd30c9054d108f9986bc630e134f7dc0b34a0f6cc16413c7fe`

```dockerfile
```

-	Layers:
	-	`sha256:d463d67fc34530a8e4da67d7d8f2eaf3900764e1af64cbd2ecfa941c0b6fbe8b`  
		Last Modified: Mon, 29 Sep 2025 23:55:18 GMT  
		Size: 2.6 MB (2564554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:622adc31b8e71be9e7c4c1a1e49cc31bdca86dca74f4486e53c91aeb1b6e05bc`  
		Last Modified: Mon, 29 Sep 2025 23:55:18 GMT  
		Size: 16.3 KB (16324 bytes)  
		MIME: application/vnd.in-toto+json
