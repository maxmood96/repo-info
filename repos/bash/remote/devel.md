## `bash:devel`

```console
$ docker pull bash@sha256:20d8b89967b47246bc068d40e01a768e25c46519297d6974cccbade8bafbe2dc
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
$ docker pull bash@sha256:aa21fec3a43083821a7c78298b61dc37f1653ecf202e7d390a5b8fc3ed59170c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6273928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2184fb39054248878564bd25cbd4c4d3b94352568734a5c02951c6f01dfebf17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_COMMIT=e1dd98a1dba28310c78157070c5566a43ed86ca6
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240216
# Tue, 20 Feb 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24130ec4b6e1362b7a5bb3ac4a89ab83a3356baca8ae4321fa5514a33cb3b3e`  
		Last Modified: Wed, 21 Feb 2024 00:51:05 GMT  
		Size: 2.9 MB (2864860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6206aed5b71c2fa9c6a64e4e0bed13dc6c6823664551b1cfcd55cd1a5c364329`  
		Last Modified: Wed, 21 Feb 2024 00:51:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7692040419aa9cddca8c2292dbbf7de6f04cbcdd8c7984378325fccb9d57c2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9690fbd98729879119e414c26aa16f39c45b83ab43ce23ac557d723116ba48bb`

```dockerfile
```

-	Layers:
	-	`sha256:129fb9e5f379895845e0a50610629cdd1e7f1689e0909125cf57580387f7948d`  
		Last Modified: Wed, 21 Feb 2024 00:51:04 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d0d61187bd944ae3fde39253f94b1750b1d5cb9c5b27008dba713be3cc28a3`  
		Last Modified: Wed, 21 Feb 2024 00:51:04 GMT  
		Size: 16.2 KB (16242 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:b4b37e93f3b035c485c8557ef340b491aa710314da1a1c0f6ea2214d03ed2c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3104f9607a40400f700e292753df73e624963aca93cd6e8a9ae83c73dd5b2e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_COMMIT=fbc7d97de6c6f3dedb34f49f89a628a99ef6ddf5
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_VERSION=devel-20240209
# Tue, 13 Feb 2024 05:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64483d37ffb20be6571922ac89697486e8f0592f6bb33c46c91d76bcc80aadf9`  
		Last Modified: Thu, 15 Feb 2024 00:54:17 GMT  
		Size: 2.8 MB (2815371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9b17ffca7a5aedcb97c0f7b4bc6feca6ce21063d7f1ab7d5f6b386f198205a`  
		Last Modified: Thu, 15 Feb 2024 00:54:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:536e14a037cc34616c32d51875a23e723bd7387b2adff543124a1e1ca55c37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185b905c7d8b66bf56fccf67aa8b275cccaf30c5cb10da1d69a20faa527c3817`

```dockerfile
```

-	Layers:
	-	`sha256:b87b907624920d4ad247a5c56b69b40095048137bd62b5318f9291c0dc604622`  
		Last Modified: Thu, 15 Feb 2024 00:54:17 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:9928425da84dc53d541044be5f50b45cdcc9c09bd8f9dd0fb527e6b733eed743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5684418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8829f35b096d6d56d44ec181cd4de14451e852f60a227da9ce3f6905446c6ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_COMMIT=e1dd98a1dba28310c78157070c5566a43ed86ca6
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240216
# Tue, 20 Feb 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac42e8242ae2651b3deb6352a397b1627a966c499513e38810057f03f979dfa`  
		Last Modified: Wed, 21 Feb 2024 00:52:06 GMT  
		Size: 2.8 MB (2765181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b58d0a546a56f8fef702baf5997588969905f5f362bf1cdf3f1328154886386`  
		Last Modified: Wed, 21 Feb 2024 00:52:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:cbd0a952a26b49056f15bba8399e7a77c317f5752a99a4fc84f96a3adc3ac48b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b785a08087dbf1d883a407fb67d1fa997edd505a08c6c5f7147c2e408677be`

```dockerfile
```

-	Layers:
	-	`sha256:c0b1d07d946095ff843c08e3e75ae6df6e32bab957d07a9e72357112401be7fe`  
		Last Modified: Wed, 21 Feb 2024 00:52:05 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e38ffef66ff48db1654d05992359892bd08490a7995e11b6b28254ca3b7577`  
		Last Modified: Wed, 21 Feb 2024 00:52:05 GMT  
		Size: 16.1 KB (16148 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:6eb341f44ae53913f9b5f9c2ccee462964300d5321c28397ae20c6a2eb915850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6315421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad67daef876d4219ab6c7f79a63a1ee1c6f716a6d36f22cf10600ae0e9648ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_COMMIT=e1dd98a1dba28310c78157070c5566a43ed86ca6
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240216
# Tue, 20 Feb 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6303e1853eb1e8022f8eaf3ac8c6e2c1ce3b45e1e16e394fc23d0253ae1b32a`  
		Last Modified: Wed, 21 Feb 2024 00:53:24 GMT  
		Size: 3.0 MB (2967373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7b6d30bd2c6bb023388352ca97d15af510553a19e7359841664aee93eff033`  
		Last Modified: Wed, 21 Feb 2024 00:53:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c50f8f33fb8ff2c231973f18e4a085145afc3ac36f7c266ce1139637876b7073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58df395d2f3ced518f9ef50fec341ffb6effd7c0186b9c53ff26d503c0954a7c`

```dockerfile
```

-	Layers:
	-	`sha256:cbb5c7421644083bc798b7cccf9f852731a6f1904a16a9e57e32f1b7051ef5bf`  
		Last Modified: Wed, 21 Feb 2024 00:53:23 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6df4ba051e54d6561a87b4a39e94cac74c7867e32ba3684d86696388b7d2c2d`  
		Last Modified: Wed, 21 Feb 2024 00:53:23 GMT  
		Size: 16.1 KB (16088 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:ddd561db4c242fbc9e9865a66e4ecaf2ac426658fe227b0b3818728ac8d655bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43862f91600a3c0b1ec0462aa3dcbbb250a46fcdd3137bfc4a63cb18c75dfb9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_COMMIT=e1dd98a1dba28310c78157070c5566a43ed86ca6
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240216
# Tue, 20 Feb 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eee70b84a4ba3ca5f8b45566381964a0c920c42c220d2fcac4a0229e21067c`  
		Last Modified: Wed, 21 Feb 2024 00:51:02 GMT  
		Size: 2.8 MB (2810663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a01d682dac99ebdf143e6b8ed69692784f417b75f12d5325846f91436503a8`  
		Last Modified: Wed, 21 Feb 2024 00:51:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f52cbcc3eb8bdb34d01aaafe18314511713399de221f2a96bbfe464b269da774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5498c12af84060fd69a340697f578bf3019466b5af3760aeec7036f5a75cdbb2`

```dockerfile
```

-	Layers:
	-	`sha256:069f93b1ab3fa345ccab77b0bf4b74690c5e4f5dd8dbca8b874ad5489a665d7f`  
		Last Modified: Wed, 21 Feb 2024 00:51:02 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cedbcf76844c29312968a648cd566340efc6a4235cced93939e663a2a1a7b5`  
		Last Modified: Wed, 21 Feb 2024 00:51:02 GMT  
		Size: 16.2 KB (16215 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:f0adaf2b18352b2ef0bee78074b27675fc71a437c56588cd1fc27de43d9b9e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6498092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7915b6befbbcf6527207da8e953686a5dea48a3cdcef823d3fa57c50b380a5f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_COMMIT=e1dd98a1dba28310c78157070c5566a43ed86ca6
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240216
# Tue, 20 Feb 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b86a6de3ad629dee275996fcc6886f0e2d867debecf2be5d596605b138da87f`  
		Last Modified: Wed, 21 Feb 2024 00:51:07 GMT  
		Size: 3.1 MB (3139401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f83d4394bf9428633b68bb28d4e6eb1974703aea37e9fb93c6a15065ffe9d`  
		Last Modified: Wed, 21 Feb 2024 00:51:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5d4eb22cd22202e00ddaa61924883eba3fe810659ec156e347efaeabbb4dd0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6c793fc7240f0b2b02c21d54887395277b2bfd1cdacb3d0cf8b6200ebd4e75`

```dockerfile
```

-	Layers:
	-	`sha256:417e5e103bbfb5e453cb01da4937630dfcbcc0c81359ca6fd92c81107c6cb3d6`  
		Last Modified: Wed, 21 Feb 2024 00:51:07 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b2da1890de80d616f6fe6aa1e7248cb6b43538913512584b1f92f3ba5f4d67`  
		Last Modified: Wed, 21 Feb 2024 00:51:07 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:905125e9975ab4c69544de4205975fb1837ed739b1ee29157c355701610146ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178901321bd7270b2a342ce41a2527e7c941d7d9aa27f80bead346732ab059b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_COMMIT=e1dd98a1dba28310c78157070c5566a43ed86ca6
# Tue, 20 Feb 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240216
# Tue, 20 Feb 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ef41e6c5691d7f7c0f4a74226c44c57c3495cfd37ba1dd7c6b200b3183987e`  
		Last Modified: Wed, 21 Feb 2024 00:55:13 GMT  
		Size: 3.0 MB (2965779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1958a8d4ebc044a01b50f3979bccaecdf427eb063fde7ebdcd87fe89e2676bfe`  
		Last Modified: Wed, 21 Feb 2024 00:55:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5f365b03b84d06cbbcd979dc24b16a00016e76ed9561d4e8bf8fe31c6cb7bdc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caf98bb89addc6b187a693757f2fa4d5cc203d30034c2dc1445f9faaf1cfa19`

```dockerfile
```

-	Layers:
	-	`sha256:582bbd59d22737f7f3f4bb5f502f709071ceacc551069b0cf2c7c33701a08b3f`  
		Last Modified: Wed, 21 Feb 2024 00:55:12 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f3db32e8d341f4d46dd6320dee17a9b56848d2d4e6a27de5f12f35828822bd`  
		Last Modified: Wed, 21 Feb 2024 00:55:12 GMT  
		Size: 16.1 KB (16078 bytes)  
		MIME: application/vnd.in-toto+json
