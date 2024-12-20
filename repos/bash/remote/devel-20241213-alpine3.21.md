## `bash:devel-20241213-alpine3.21`

```console
$ docker pull bash@sha256:f1d2a7135b5f6723d2169c5d3e133b47e0c498bd75bfebae6603bad39220fb27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20241213-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:47c2b709a9a3aaf705412e5ad310db36ea0691671beccecbbcfcdfb83df52d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea52dd78c27939db7049be5dc66bf49ca916bbba7c50f7f820021f902146469d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05daa63f28e9cecd02b9e545a71003d2e6d107b8e4f68f35b2c503094207bb4f`  
		Last Modified: Thu, 19 Dec 2024 21:31:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b42153aa367b3ee8c07ae9050907d963662bd736fce9cffcaa1b4ea2aeccde`  
		Last Modified: Thu, 19 Dec 2024 21:31:26 GMT  
		Size: 2.9 MB (2948199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215c39251bb0640d58f412c21702d21112f22b4cba3fa0367c7ddb4db1611662`  
		Last Modified: Thu, 19 Dec 2024 21:31:26 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:bc4cec4d2a68afa357fce44f88fc434804e8c9b3bc710b2712d97618a3dff1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430e96f2e2820ebadaf65f40a7411514d464f20ce1a5350798c2202c543725e9`

```dockerfile
```

-	Layers:
	-	`sha256:8c2c84361bda8aadeeb8dcbea59a4a7c783e7c6d09b54a221ce412b3fa789519`  
		Last Modified: Thu, 19 Dec 2024 21:31:26 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dbfad5c510c548b30bbf0fccf1fdf41dcd67290c1ed34826c0867f32857aba`  
		Last Modified: Thu, 19 Dec 2024 21:31:26 GMT  
		Size: 17.7 KB (17676 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241213-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:2a0f9f6c70cf1969e0fcb5badde581c4242cc013c36051406544f8e3f2826b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6253761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216d3521b9972d141c2333eed299e650edfcb35eedb5f9bb09a12cc135d0615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dad000104d8d6e4aac117d865936836caa8bf357d618a8bb7acf231795da1a2`  
		Last Modified: Fri, 13 Dec 2024 01:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8e04bd18e4561718401f51630b042900999abd901aabf0c7710d1e0f56a093`  
		Last Modified: Thu, 19 Dec 2024 21:32:47 GMT  
		Size: 2.9 MB (2885788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45961a2d025a3f26ec1aa5a62dfae11678ac9abf25ce9369301d3b967790db15`  
		Last Modified: Thu, 19 Dec 2024 21:32:46 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:7f84ac0caaefd17882d4c80fd85b28d30ca0c4e8d15ba876d733b3265344944d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d4dde839c375881b0bb89bfec3a6c9b930e8dde110adc4c9e505cc2603f995`

```dockerfile
```

-	Layers:
	-	`sha256:e101b2ec834deaa51b3bb8efe54ebd3856ef3a38f83f1d4df4526979dcf48124`  
		Last Modified: Thu, 19 Dec 2024 21:32:46 GMT  
		Size: 17.5 KB (17537 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241213-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:0348b4319bbaac3a1b3c63ab487be4fe08706efdc5d0530a6387a7fea09ada26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b31d6e484ee194f16a6dfba7a0acc73a343bc148fa0c571e5546e411e3c26a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092b47e0e9bd9310a551d1dc6827d9f6b0069c38ba1559b7a818161c42820f4a`  
		Last Modified: Fri, 13 Dec 2024 01:32:24 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8642f519f82ba5a453bd526a77c12f6e15c4ee8103c605bc78147dfd360205`  
		Last Modified: Thu, 19 Dec 2024 21:32:04 GMT  
		Size: 2.8 MB (2836941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fee443df55778dec54957321b7326f19928f8de680422d23874e6bf7f732fae`  
		Last Modified: Thu, 19 Dec 2024 21:32:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:bb91f1d83427e8b24a783a748db006c699f632e67e515a51c88bad990b90132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e5e1674b76e4b684c76df6556aa406f269070a9361877b31b5a0ed33538d1b`

```dockerfile
```

-	Layers:
	-	`sha256:6480316bf8dc15d1d752c4c55dee33bb463f223e4fe94db819b9feeeb34da13b`  
		Last Modified: Thu, 19 Dec 2024 21:32:03 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:512999dad133ececd7e341e91e7b29c0b55a91ffdd5546c95b6aeae1d29dd3d9`  
		Last Modified: Thu, 19 Dec 2024 21:32:03 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241213-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:4ed69b962a8e7e207bb55aeaa496bb37f94bfd83917130b109bfd40d15748969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b15c10623dbfcb21233f199b7bc263755a77f40078e354206635f6b92e70db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf7a7d9a0c61bb76ce352187a74e22a43dc03fc95614ed659a63b2a9f0b716`  
		Last Modified: Fri, 13 Dec 2024 01:32:25 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9969fe7a21cb101966cab3e24911e8bf1b896385eeffb0ccbbc89ddc7643a54`  
		Last Modified: Thu, 19 Dec 2024 21:31:30 GMT  
		Size: 3.0 MB (3032968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eebf2087baed513ceed1cb592c69b77a5888455fd2f14347539aab3fe7ea3fa`  
		Last Modified: Thu, 19 Dec 2024 21:31:30 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:b32422f3c7838f35b09dafea17a593b78af858fbb0dd12827611e884f16991be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc343add0afde393af0755c80d52ffcce14402fe8714b619b5f469f8cba426c`

```dockerfile
```

-	Layers:
	-	`sha256:d76af116bb5c38e19989e0dbcc2a5b882eef9497ed245012fb40767269a5fb10`  
		Last Modified: Thu, 19 Dec 2024 21:31:30 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56ac89e570cfa80a538885be2a1fbd3ef92113b0f79ed3121e0091662630d41`  
		Last Modified: Thu, 19 Dec 2024 21:31:30 GMT  
		Size: 17.8 KB (17781 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241213-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:5fd45f5a304a9786984cc23c128ebaef96f7c9f157286096c0888e383d2eb014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6341542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfc8dadf97453a13f3f57ef4d33c5e60747e1c17e8e3ffba2273461aa165373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d35c5eb8050b2a709e6b03398066667fab5a275a6deb4d7a2d76dfdd94a87c`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0873a85ab82ae2bc90d0c6d787d2300f5869b114662caa36d8a484220f472568`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 2.9 MB (2874667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a6c646dd76418adfcabea579761a30bd532acdc1b853f97c9fbaf05727a71f`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:9d06d9282db6eced4301cadad3bf2d0f11a57c33b455e5a7cac66a56af83b911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfca944482563463451f8cb597f6e0f2bfb8d911e85f0e8e76768780829327a6`

```dockerfile
```

-	Layers:
	-	`sha256:48afe77430f5daf163b9e8def135413ac666ffc495bd1f806d47fafa4ca925f4`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8950aa2a41404c0527716be42afd5f8d2de2f2a3be207ba425edfd7d49254f`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 17.6 KB (17645 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241213-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:a5d9afdbc3352a6d718bf954376fe646aad4bfce77efe6f332353a85463a3a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6794881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78e384c044cc17233a72356f75faaa76039f7330670d64d313bf2862060a52e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b87b85a573e0641b22c0c1975b4daedc795bfc844d58d95354403cfa86fb1d5`  
		Last Modified: Fri, 13 Dec 2024 01:32:04 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0a83fbad8efc684c5f29f452ce702e654aa03029dde604d9b6450148afbcac`  
		Last Modified: Thu, 19 Dec 2024 21:32:25 GMT  
		Size: 3.2 MB (3216980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8b0db630cc111bab6651f58137c1586ab365e2030d0628a6430ac1dc553cb0`  
		Last Modified: Thu, 19 Dec 2024 21:32:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:f3d1bba7e5345d33c5face72bed3441b3eef47284950bf0321ca64361fc740da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181ff81d699a49686009407a9be4fa59cf31f20dc998c3b6b80768e722e0e31`

```dockerfile
```

-	Layers:
	-	`sha256:a086a2194fe087ce635c8bad18013ed555b0d50fc85e92ee2bd74ba18d1bfc08`  
		Last Modified: Thu, 19 Dec 2024 21:32:24 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca32897255c7a0ee228e74257b2cfa76d5e0eeaa68db618d7f3af47d412a26e4`  
		Last Modified: Thu, 19 Dec 2024 21:32:24 GMT  
		Size: 17.7 KB (17721 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241213-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:1d14af0e63610c9ead95b9b0d613355e54c01770d8c2210fe52eb0aa72a4ad96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6628c12ae62be8715ecce334ca33b2cf0693eddcdd3639e54df9189ed19c33e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e78ecf1799363eb590970338b7d1c596a4b70bbabc18d7b41caa66e767f889`  
		Last Modified: Fri, 13 Dec 2024 17:51:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aabc6f7e1648de1474a439f6e10533db7f4568be10a9a1e0052ef395a14b1b`  
		Last Modified: Thu, 19 Dec 2024 21:40:41 GMT  
		Size: 2.9 MB (2899490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b219acfecae1b46fb6f5209e74a0fd7c81d0e540fab41a8c01857a673a954840`  
		Last Modified: Thu, 19 Dec 2024 21:40:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:81f8fadeccede43fb3c78a39a26f58e7bcce8986da75cc219ee87aa0a7df3c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8022ee81c637d6bce867bfe078ba2470eff0f2209e9ca9561fac2f34cd46e0`

```dockerfile
```

-	Layers:
	-	`sha256:b0614c627d38aaaabf31e8a46bcc8b8567e7810757d3ee267e22123451d812f9`  
		Last Modified: Thu, 19 Dec 2024 21:40:40 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:764a856f282e70ba93bdbf13920ab0c2b573c30472f82384094aae394e674ec1`  
		Last Modified: Thu, 19 Dec 2024 21:40:40 GMT  
		Size: 17.7 KB (17721 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241213-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:350088700427a0ac50aba2493853d03fb2b2a4d8dd04db140e7f95902daef947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759b8d0d48b20c78c7cc22a96f3acbbc01c01f575b0e643ec01e6e48cc747beb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_COMMIT=bb56d620e075e3c96ae84b52de6b74683d9ab320
# Tue, 17 Dec 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20241213
# Tue, 17 Dec 2024 05:18:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Dec 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7913dad0640ae3de60db04eecf7fac8f80f68bc8b846efa764ba07e8ce672eb9`  
		Last Modified: Fri, 13 Dec 2024 01:31:15 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec27ba436c275619ce1517fc110ce673b9334908ebe664d9651ce99430cce96`  
		Last Modified: Thu, 19 Dec 2024 21:32:11 GMT  
		Size: 3.0 MB (3043501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b744f007f3acf2c745da43d8dd6ac5c26974d449ae9f3e92f003c5b3904eb9`  
		Last Modified: Thu, 19 Dec 2024 21:32:11 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241213-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:4ff0c518800e95dcf7e3b6d91c1e3bfd11ae8c735802548944dabe19f8c0124e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 KB (130648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f95a3d4945dd6e2c52a6624ba9689c472ffd0b20b8d95b7bd5008795c6cdcdd`

```dockerfile
```

-	Layers:
	-	`sha256:cb911d5a5ab05a38c481efc50a3f1b8a8ae02bae523219cada673824119842ae`  
		Last Modified: Thu, 19 Dec 2024 21:32:11 GMT  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d7ebf2248f33baf92de50e777aa25c2cef3c6303d29025915006779af07f257`  
		Last Modified: Thu, 19 Dec 2024 21:32:11 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json
