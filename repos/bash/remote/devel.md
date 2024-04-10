## `bash:devel`

```console
$ docker pull bash@sha256:3b7927fc14275245855d8b2d5af61c9ba1dfcd13c21f4340a32dd6891a5021dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:598ee2e2170bcc19ea800334db3183bd7aacb3db4473624deec112b98044b188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6295974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae95d78766fc5e81a0ab539193c159cfe6da28d4a0fc886f28624fd1db86d8bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_COMMIT=e6795c05dd877334832568a7145f0587ad3901e0
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240406
# Tue, 09 Apr 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d804bb60415da4d8702c43f858ffce9e74e8473ae7b7de7c9956e7dbad29bc80`  
		Last Modified: Tue, 09 Apr 2024 23:50:23 GMT  
		Size: 2.9 MB (2886910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698ea4f15a5146df5236c3016a52e52692426c0a5d1a7a6ca53e7e2108098f85`  
		Last Modified: Tue, 09 Apr 2024 23:50:23 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:06646a5aceb8ec95b0997aeba905e3c215c6fc43599b2d4a239c2ddb08529a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b1c48090561b48556ea827e35745b532f023bae144ba08c93cc9b6da0a797a`

```dockerfile
```

-	Layers:
	-	`sha256:97913414bd968db4616b86c4f227ccf2b7462c8ce7bd40c79b4592658e41984e`  
		Last Modified: Tue, 09 Apr 2024 23:50:23 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3b66e182f3dc231751afb1ce763feea4baf61d40689af884a34a19f230fe97`  
		Last Modified: Tue, 09 Apr 2024 23:50:23 GMT  
		Size: 16.3 KB (16299 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:4e29a04e64ff6aa37d0be059d4d14bb58e72949c837ff4c165b10f2a0a63359c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34d4f5a29582da47727846fa7c48df934479308f83ecf1bd63ea61dd8201ff7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_COMMIT=e6795c05dd877334832568a7145f0587ad3901e0
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240406
# Tue, 09 Apr 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb6b78f088e83c08eae22fa5b47de6724875e77634b7a20b4de03cdb4d5c6a8`  
		Last Modified: Wed, 10 Apr 2024 00:04:19 GMT  
		Size: 2.8 MB (2839261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e6e0cffcd34f6a053196b3bc428a5444673a53d189e0f08728e194aa233df3`  
		Last Modified: Wed, 10 Apr 2024 00:04:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a6c90da40e9ce0c2fbb42102598ff2caf9ce7c856906e78171e99b5ee81ea8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (15989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e7170b9879ec0a0859baac7ab401c80fbf101aca879a7585174fc336fe1034`

```dockerfile
```

-	Layers:
	-	`sha256:43c6fe102d776652f585e124d2dd16d14dc5714d548bb244de4a82288956ad8c`  
		Last Modified: Wed, 10 Apr 2024 00:04:18 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:af9d9a13759158143ca46fe223ab4f402e742cee74f0b81f89934bce5f9a9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94fe5bf3a4e208237ccf8ffd4b6eee3d93a90b28576f48a8cbf8c09df3468f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_COMMIT=e6795c05dd877334832568a7145f0587ad3901e0
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240406
# Tue, 09 Apr 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9312e5bf2ad21202d21a010b0e9e9f9acc0c8ccd9ed1fc0b2caeb4133096b668`  
		Last Modified: Tue, 09 Apr 2024 23:53:24 GMT  
		Size: 2.8 MB (2783962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe56fb3974aaf1c1333a39f7450bbbe45e9291d007574f8eff054bc926a94b`  
		Last Modified: Tue, 09 Apr 2024 23:53:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:cce742f35b249edc2d4f1a82a434b1ea9e6f5d24e5a3199a18f9f7505f1e371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6caffa9a1d13b5d64fd00bdf8ba3707cab0ebfb9c7ec07b2fb770e18108928a`

```dockerfile
```

-	Layers:
	-	`sha256:7f4b2c247ba2e814f28d50b3621b600bd62519a967703d0db77b8cc26833827f`  
		Last Modified: Tue, 09 Apr 2024 23:53:24 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172d5ff05e50f44bffda26664e3546062a072f20f088c7c268e05a425e818d36`  
		Last Modified: Tue, 09 Apr 2024 23:53:24 GMT  
		Size: 16.2 KB (16204 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:2561ef5a8aeceb2b6ee794743594ecc1641c42dedc44f4fc2b06a868b255509d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00f4eccce9d525bc958b446be925f415f1cbe1a56b87e29666161f564bfa4c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_COMMIT=e6795c05dd877334832568a7145f0587ad3901e0
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240406
# Tue, 09 Apr 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e48b6a2919e800645ac5b0a82ade5e676fa83b9d425703b50b921228bab9b0`  
		Last Modified: Tue, 09 Apr 2024 23:52:16 GMT  
		Size: 3.0 MB (2989680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2750884de74087590d02a407f7cd628e64e5bef68b67cb1d78ef368d2bcb20a2`  
		Last Modified: Tue, 09 Apr 2024 23:52:15 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f53120ef561c290ebf117bbe7a59d56e762a035dbd6277eefe9dd6a2cfb90e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d476bcc6ba2591dee363d8736817fe282e43cb70a22271ca12e97567867967`

```dockerfile
```

-	Layers:
	-	`sha256:3feebf574f67cfcbb4652ebede3c9f2a9161ae8eadda82384bd0baac3e70d44f`  
		Last Modified: Tue, 09 Apr 2024 23:52:15 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30ea19dbaebb6257d39b6937b00be5536648db29f3c536fc08ec937a30ec61c`  
		Last Modified: Tue, 09 Apr 2024 23:52:15 GMT  
		Size: 16.1 KB (16144 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:b3b24fb98397354ac6f16b29485da7098690238a4c0327b19b1ff97aa12dc55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053cb62bc1de8a68be2f99f35d2e339fbd9ff305834c0596aba8855ce02f169d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_COMMIT=2532a2ccefc50e26a32ddd430286af6f5c43d881
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_VERSION=devel-20240401
# Tue, 02 Apr 2024 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66733db5286fbe8531dbae7f0c745f3640b8d5c0248dcb8098e06ecf82ec1023`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 2.8 MB (2815763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e52512be8797e030ff71721f7954015926afa9de168619d6c9cab14c64321`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3a75988c7ef5b5c5d182e34aedb0a6b54117a4ccf1e1b02795629eafe95c4dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335174ea1f2b4a11b4ddbad36711ed3ea5df9f13eac22a353f74a20648286b8`

```dockerfile
```

-	Layers:
	-	`sha256:75745f73b9bdf3f8fd79e045ac3ef8a0577402104b296c8d0ebff0062f5a384a`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f7cc8550dd446f71a8326bf3fe2dd381e0c920f4bb61201d1a02c42dd3e939`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 16.2 KB (16187 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:4b58a07995c155c8903487c64929267e2fb9aa23ff24a1f08c121a2c7c4c2245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6517228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ced51a934ed3220bccefe0463a885c92ce93b699d84fe42903b04ba646f2092`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_COMMIT=e6795c05dd877334832568a7145f0587ad3901e0
# Tue, 09 Apr 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240406
# Tue, 09 Apr 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Apr 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6673fea94b1e2c7ef2cc7d2ffcc32d2cd072e5f570d1ca49460e97cf09f00c2`  
		Last Modified: Tue, 09 Apr 2024 23:50:33 GMT  
		Size: 3.2 MB (3158538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9d3a8ca4b8ff3c5aa6d8ac83b14bd85b42469b83a4ae769bcf1cde551658be`  
		Last Modified: Tue, 09 Apr 2024 23:50:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2b0735403fe14958910f6ce58cd1016ffceef871796ef4db79cb9d572d659758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37c0aeae2ddce6b6a7622c9dc8ed1189e430d332e088fad00de62b4e0342e62`

```dockerfile
```

-	Layers:
	-	`sha256:d71737dcb1ba3023c38186d70e42dfa7cab6e065fa0e9a267dcbf720213eee43`  
		Last Modified: Tue, 09 Apr 2024 23:50:32 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87b0f86712f8fbe8bdce255bb79c58101732728b3ad44673e2480dc1194f2354`  
		Last Modified: Tue, 09 Apr 2024 23:50:32 GMT  
		Size: 16.2 KB (16172 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:77df0d772d52ee217bc3c818bfbe42c3a209dffccc5bf8af1322422563d5d497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6220991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c36d6217f744cc61784d7abd7aae0c29b3dd755177d25318e33ad02bbf5c0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_COMMIT=2532a2ccefc50e26a32ddd430286af6f5c43d881
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_VERSION=devel-20240401
# Tue, 02 Apr 2024 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2543bff7d2f54b2086b0286cb1c37a1ca700d15fa11cc1b2d88ce07eb4e87`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 3.0 MB (2978024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e10c1c0ac8c03737e6941ac492a7b0d9c24dabdca1ed809a0606af4141285af`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:16b2ba959f7f4763ef0e3222282145d29bff3685db6fb7e5d030198b8c7bb97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33805e19c2671bea8c2f56d836215f25a865a87ad78f5c0f602f037af0e38f2c`

```dockerfile
```

-	Layers:
	-	`sha256:6c45da99e0b55bb563c72199fc28815f17ba021cf165e22ef1813fd370dda148`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0563043058dfd078cacaab69588340462b94651a004addfb3ecf1339832997c`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
