## `bash:devel`

```console
$ docker pull bash@sha256:7e52abbbb8d3c930348a1d85c7681d66d37268eeab3653de608608e7c5317752
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
$ docker pull bash@sha256:70ce5d5f3d6a7a0e9865df67ba5652e45c66618a653134ae5ca6d79cf32daf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6296713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e2a0fa27cdd1ebed8b1a3d2a75fdf14ff0e326fc264f48c4700d08d9c7576e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_COMMIT=8c8daff1e3661cfe427f194c38c6a1b452cd1456
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240422
# Tue, 23 Apr 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd79b6312d1d50c58dc333171cbe9d2843f90ea93de7d11c51c3c1189e175d`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 2.9 MB (2887647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e57a7ac2b3af0e108d22a338831cb6106bd7e38c549efc306317ceb384ae71a`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7e1a30af97bdc1da3aac8f48ad33fc9266f38c2244c95da9a70ec369cc587325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cc8b39af48c5f614745d59105a95347788a9d5c53cce289ef1df6d3328a881`

```dockerfile
```

-	Layers:
	-	`sha256:ff6b5684380982d6da2ca18c9f4ed4d68a943af7a0229629c0fabde106c354ea`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f94482e63bdc254f129deb9a78cf974559f83060fe8d71f9022a3c167f6e18`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:3754ada82359b56d094e2d269a4080c69a46ae7598e0f9d510a93003b4ace61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6005208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b55716e166d88b57998f616764f838894f6a2ad32ade840c36aa40c83df2a41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_COMMIT=8c8daff1e3661cfe427f194c38c6a1b452cd1456
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240422
# Tue, 23 Apr 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898848d503c15fe9882ae96a17e998fa5e338c8bb8a841638539180619250756`  
		Last Modified: Tue, 23 Apr 2024 23:57:26 GMT  
		Size: 2.8 MB (2839475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e345ccf8a7dfb23702d8ea97c8a256c3476fcba4709c1fc7b2f7c8caca9c96e4`  
		Last Modified: Tue, 23 Apr 2024 23:57:25 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d0dc2a205c3eaab0e4ad6d1bd4473093693b9edd2335a4392d5e7577fe971895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 KB (15809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5bd9dfbb7dd1ad722a473d0bf8bf3cb2987ecb99f9993bb8a72565f7242dbd`

```dockerfile
```

-	Layers:
	-	`sha256:192a87a9b4c1e54f477ef58338bac8cfa6be303264047b84f8650fd8a7d41d7d`  
		Last Modified: Tue, 23 Apr 2024 23:57:25 GMT  
		Size: 15.8 KB (15809 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:c8540d27ec21ba6f6e0389cf588c43fa8ec76bd92aee33aa0e50cb20709881af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b552563c3bf8de049f4df54713b5ebe5b7d989f08b17fbd19636c49ca924142a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_COMMIT=8c8daff1e3661cfe427f194c38c6a1b452cd1456
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240422
# Tue, 23 Apr 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbf487c5d053f626780bb99cb2c3ddec640a5708e36bf25ad52b884a53fbb3d`  
		Last Modified: Wed, 24 Apr 2024 00:04:23 GMT  
		Size: 2.8 MB (2784064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa6ff59e1d8b06d5f30c69a4079649f5abb99c691f98667818b7615a34c2f6a`  
		Last Modified: Wed, 24 Apr 2024 00:04:22 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:9d577d9b9dd39425278e1b93ad57f710375da50f3695764768fe45779429fb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59dfbe26abe6cf889094149c484f5c9bc71226ef6d313b532ae44362e85dcb3`

```dockerfile
```

-	Layers:
	-	`sha256:199faf6d4d680383e86374c1b1bdf38879e480f5ceffdd6599a3871c2e67640d`  
		Last Modified: Wed, 24 Apr 2024 00:04:22 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58515bd45832d88752c5642e1047532b6ea74c94a134c5bd194a1d04a3f0bbbf`  
		Last Modified: Wed, 24 Apr 2024 00:04:22 GMT  
		Size: 16.0 KB (16028 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:4de725a4550c6056b46f3559b142ffeb3e20bd282d6595175f38ec791e3ec7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6338077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb97c79a5574a822531f7c295fec61c8c9b2727b3073441a3bffb43c01336c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_COMMIT=8c8daff1e3661cfe427f194c38c6a1b452cd1456
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240422
# Tue, 23 Apr 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd993daab4f1f74828213894189ff4226df5ec549988c4905e8d6efc62500198`  
		Last Modified: Wed, 24 Apr 2024 02:28:12 GMT  
		Size: 3.0 MB (2990024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d19c7ca0c0eba5712cec39e74115af646eeae4303e03015b7ae259de53205e`  
		Last Modified: Wed, 24 Apr 2024 02:28:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:88b577ca487db41d928d81301003bf61a7a9fcdc2f03a08e6a3e59651ed59dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916de5acfadf690a2b02da0ef11abb1bc874b6874ed813552377c7760a8bfd53`

```dockerfile
```

-	Layers:
	-	`sha256:1a85ff1cae4eed1d99755c6f71f010817115ffae125ef8a178b57ccb817c5a91`  
		Last Modified: Wed, 24 Apr 2024 02:28:12 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6138e84a74bbad412fad50e0b8690d96a7978db6d3f20ef786f9eb33559753b0`  
		Last Modified: Wed, 24 Apr 2024 02:28:12 GMT  
		Size: 16.0 KB (15968 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:9c7a8c3942a78eeb93c1e5539bf4dd26d0352a97e48f03addbaf74d8ab9051df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6071727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec17a5ee790f3a054991555710ecf21ef5fee77899de7611ce571d1136758e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_COMMIT=8c8daff1e3661cfe427f194c38c6a1b452cd1456
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240422
# Tue, 23 Apr 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80e4b077b885775a538b8529c5b9010db31cba9bfeb64f93c5aa9ca18f3cf78`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 2.8 MB (2827300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230c49d8abcdf94d7382e77ace5b4c200ab1175b5cdd18ac6e3fe5ab9cee9ec`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5d64f2885ef2e48391752cda4d03159d0bb01b220727a32a27d52fcf2be61840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6b06c677e6a99a5c3ee9bced59414367f696856268db81135addeba28b87c`

```dockerfile
```

-	Layers:
	-	`sha256:382bf1e7849eeea9b3642b87f19c9d4a527e90b19e6928477a4b3f55fc0f9a65`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e3da7d213ea8eec7400896d31cf0ab54c608339eb7cdbf53e438e18eb1f317`  
		Last Modified: Tue, 23 Apr 2024 23:51:19 GMT  
		Size: 16.1 KB (16094 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:e9041ee21dec1cab4c3220e7da6b7eebe577ee3e874ffcec4c0a3a743806d09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6518461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c493f9b472f331bc5d84ac49c435e0251fc6865b5cb3d3cb9a78015ac62db5e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_COMMIT=8c8daff1e3661cfe427f194c38c6a1b452cd1456
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240422
# Tue, 23 Apr 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d2b44264d76455593fd4edaec9b25d39a9a87a5c0159c52799e81b596bb478`  
		Last Modified: Wed, 24 Apr 2024 00:13:56 GMT  
		Size: 3.2 MB (3159772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c4bccfc0b4c9583c17f5c01cb491e333b8e95401ebf260bea19d6c41b5ec95`  
		Last Modified: Wed, 24 Apr 2024 00:13:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d6a1d6382ba4d81c508d8916ca4f7b35f96479abd7620a78e736364102e7a733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a366fdf15f4062aba2816a1ae5ef9c42de9efa76bf58d88317d983e2cf0269c3`

```dockerfile
```

-	Layers:
	-	`sha256:0da0e9101062918a2ddcd60175d95ea33f0ef06abadd149245bad01075c45a64`  
		Last Modified: Wed, 24 Apr 2024 00:13:56 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cffbc3613e9c06ce6680f50afff1e253f620c2d3342c7c244906366f57ae907`  
		Last Modified: Wed, 24 Apr 2024 00:13:55 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:6bd5dd57c4c1730f582dbbfe26627ef214a41442d2f1e2a761f805faf012db43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6232269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd42fb2f6e0d042c8e0c19b9d260743cc54384e8c6c526a33f8b0e8e2358242c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_COMMIT=8c8daff1e3661cfe427f194c38c6a1b452cd1456
# Tue, 23 Apr 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240422
# Tue, 23 Apr 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Apr 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Apr 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee051a14e4c40963b7ed9177abfa2582181966fcae69027bb05765a2b6df362`  
		Last Modified: Wed, 24 Apr 2024 01:31:18 GMT  
		Size: 3.0 MB (2989296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6354adcd328fb796ec0f2fc63bd4efb1900732ba2696680ec2eb7d409a6a788a`  
		Last Modified: Wed, 24 Apr 2024 01:31:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:019966f5940dd96fd1f970717fe0c30ff925ebf2d54d53e0ecf57b52a7eccff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ade79396fb0ff6ef5ec003cba25c2ddf6b170c48ff02cebb6c1a93d5faddeff`

```dockerfile
```

-	Layers:
	-	`sha256:e037fb6c967a041391bd2a442e59e6df64e0f4c818219b9d253535becbf8bab0`  
		Last Modified: Wed, 24 Apr 2024 01:31:17 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6881292e3e1dce6a75d4e3fb1b3e770f87d25777d5429784bd2ec9835c7049`  
		Last Modified: Wed, 24 Apr 2024 01:31:17 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json
