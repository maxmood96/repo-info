## `bash:devel`

```console
$ docker pull bash@sha256:1fed98e6b456cbd8b32da40444d03f3a6ddd9259040e2905ad7e70a93f154f02
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

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:b47c23aa81e94cca4c8082b796977de5f5681602e7848c8c7fad1ec7db8aa18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6531543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97546bc70ceebce65f81ab013993b55682b3df8980cde9990996fea884efddd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2a2831c60d84b8e016a252217cb80d523362dbdcccbc2b5beb53e129068689`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 2.9 MB (2907398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec69aaf8ed0380481ddda3ebd9cda123aeb5039bac62439d8564ae547c8632d`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1f8f427ae4970ceab77efcd9d7377fed81d05b84e9cc56689ac2b86150d3ed6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a1b7c14889d1154b9fe6053b48ec4d4cae34ef56b02ec523a3fc22eb9ea45b`

```dockerfile
```

-	Layers:
	-	`sha256:42a247538cedee4f4357e238113f22fdc056e94c56b9fa80a0718ac86465254d`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 109.9 KB (109896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c001ab3d687fff09076448c3226d7c2c568978e319ce748657e347af357cf5ca`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 16.3 KB (16291 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:00834dde45788b066bc218fbd4f92e79d0fe21fdd8cd169f6a9d9ba419971580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a241e35fd34bed072a6abcfb0256fcbe55d656aab056b4c702c675c511bfc0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c341ed1bb38c0a708372d696bd5972ca4a105551371f68673ab6136058ae78a`  
		Last Modified: Tue, 01 Oct 2024 22:18:41 GMT  
		Size: 2.9 MB (2857297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a8de2f49a814fedc714f71609b89100a933a1d3c3e8fd30e0b7f105be4e26d`  
		Last Modified: Tue, 01 Oct 2024 22:18:40 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:db53916263f1abe505d7e6bf1d0dc9fe4bebd7e8458a12b528cc1159929f7891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6d30ac979d2cd0372f208bcf60eecb96dc4d53123374769180c3fe113af9d`

```dockerfile
```

-	Layers:
	-	`sha256:b9964a4e70a2526493af85bed4e118cbd9cfe319f5fe55e7e7574df719db80b6`  
		Last Modified: Tue, 01 Oct 2024 22:18:40 GMT  
		Size: 16.1 KB (16143 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:3444c0f230d58870499d8b945dccde63a1a6c80a0f15a0cc39d56c83f434e46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4e4ac3482dd524ca9f9dd9ecea4f9e9d27694444ce411616d5b197cab09b38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4468cd8bc2999f4ca63de0823d6b138b17fff2c15bfce74aefe8f88db6705b`  
		Last Modified: Tue, 01 Oct 2024 22:18:08 GMT  
		Size: 2.8 MB (2800373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71bf33a881af90132705239de30151623f1b004ecac84842b68ba92d8032cf3`  
		Last Modified: Tue, 01 Oct 2024 22:18:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c63ea1d9dbb7fa7262d1c252412f2417c9460e0d2efe14ddc2a1a248283b5bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf43ca7d4f85ef97d15bc74e8b403b99add180c8d809c3af5f32dfad9b935fc`

```dockerfile
```

-	Layers:
	-	`sha256:c9587956091ef80f92b57d026006d97348f73dba2bde3968ec5ec60972ff54ce`  
		Last Modified: Tue, 01 Oct 2024 22:18:08 GMT  
		Size: 109.9 KB (109932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a424429ac8266d730d4739abecd2f0221ed4b8115d2808161d7d5fb1190361`  
		Last Modified: Tue, 01 Oct 2024 22:18:07 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:e1db70c0657366711f0185e0cb12e590a2d330172c4494a549ec396b9a2e8121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718378c106b6b0367b80d533c134c4d882de23f6e7aa7463e1a4556b5e1de428`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f8a6c4c5777f1d7325800915433424b6f77939679bd9226c95c9ac1f84ee06`  
		Last Modified: Tue, 01 Oct 2024 22:18:32 GMT  
		Size: 3.0 MB (3006781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666eca56e523f6db94dd002b73924c69f015b4a62482a6682123f50e7dc3901c`  
		Last Modified: Tue, 01 Oct 2024 22:18:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:87f258d6a48ad5154140de7840a4628f4595a2e1186ba89f85fa14b7cd7e7cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2bf3a8adad8b896547ffb4fb359cd453eae3d955dddcb9cf3c10acc609302d`

```dockerfile
```

-	Layers:
	-	`sha256:5a1d5d72d0a51f8bdc92b118a89d4cd5fb6730e33d1e95ec06e66083c09d79ca`  
		Last Modified: Tue, 01 Oct 2024 22:18:31 GMT  
		Size: 110.0 KB (109952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f41b4cdd0111bf460b0ff21bfeb3c44182510c8792bd2649d7ce65b00801cf0`  
		Last Modified: Tue, 01 Oct 2024 22:18:31 GMT  
		Size: 16.4 KB (16389 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:edc19c5e22db576d6d2165625771acb72ea7d9607b4cad6125dbb17f8675aefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e186b914c588fd4bc23655f5554e1ea8143490d4fe25897d654791a68c93f9d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da69b259ad33078e78251f1aa92d613a943877af9d05b80a363e249d28ffb771`  
		Last Modified: Tue, 01 Oct 2024 22:19:22 GMT  
		Size: 2.8 MB (2848997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301c87eee57fa04e3388297ed1861ed796d0bad007b294660b3e45a6ccd8a210`  
		Last Modified: Tue, 01 Oct 2024 22:19:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:20c1aea92d1bc72fbcea1bd04f470c0340845bdfd1d7fc0acce264b13d987002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a780a92374fc43358b326de740bfbcfd9aa7d659ef2102b213f858410bb2a356`

```dockerfile
```

-	Layers:
	-	`sha256:4b6e3122492dc41208fdb8375cdf8a0a6213c1ffa99a9cdeb2107d9e724b17de`  
		Last Modified: Tue, 01 Oct 2024 22:19:21 GMT  
		Size: 109.9 KB (109871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb86734f65fd5533728477d81d74430c96dfaca5f2f788caa11f0fb71c27a03e`  
		Last Modified: Tue, 01 Oct 2024 22:19:21 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:0320780bf9d3dc368c0194257b391c9fe18e2463339f13c514dce1b241347078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6752848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a2adf9eb6d2afffd5fb6d7f91fabeef9b8d6ec57bdb8c77a453d9e4e2d7619`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0443383fe2c781d2f86d49ba11d4739a53fa448b995aab14017e546706361aed`  
		Last Modified: Tue, 01 Oct 2024 22:20:26 GMT  
		Size: 3.2 MB (3180093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0adfa4d9eb6203fe34191842660b83b667f85eafbc4682f5ace89b0c76482947`  
		Last Modified: Tue, 01 Oct 2024 22:20:26 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:da45eee5aaa4a69ed53e3be6f21dd546267f460549d531d1e6ebbe3d737848be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba6c341a26d6dc02f5f68e4a835e71a8a748b93518f5348753c84746982b9f2`

```dockerfile
```

-	Layers:
	-	`sha256:319f879af6f6c79e95b026df4b0a96c7c7b9dc8149135941cddeea933c228f78`  
		Last Modified: Tue, 01 Oct 2024 22:20:26 GMT  
		Size: 108.0 KB (107976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1c5555b656e4fd20fe7b9cc2307a134b69ea5aec94d37fe9d5b9914aca1b41`  
		Last Modified: Tue, 01 Oct 2024 22:20:26 GMT  
		Size: 16.3 KB (16330 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:01464b68366b5d0ddc3616368ce8d00b6d38414f6c126fb83e0b9ff4d08e309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090e869817ec916fb5668b081b3e176d48c7880261c1d5b4dd1ca115af5e2f32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c508be4da2376373740580437605be7935dcbce8dfe7839a5b52915591923cf6`  
		Last Modified: Tue, 01 Oct 2024 22:27:34 GMT  
		Size: 2.9 MB (2857299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49af1ddd9ba56e26364dc3241116f97df2e01ed410ddf03e04772284ce2bb77d`  
		Last Modified: Tue, 01 Oct 2024 22:27:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c7cd6c738a3ab263552e1bcf3d26a9bafbdf3295909749d19830340a955e8ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d525a383b8dc56e63c5ea290c28c16eac76f62d2b835d44615cacfa84aff4599`

```dockerfile
```

-	Layers:
	-	`sha256:c279b895e93a093d8c2d8ea40a6bfd180ec95fce07a18b28c526a565f096282a`  
		Last Modified: Tue, 01 Oct 2024 22:27:34 GMT  
		Size: 108.0 KB (107972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbcfc96ce2a878e6e12cf19506c713f025e04d249c147933d6d13973ac3e8c02`  
		Last Modified: Tue, 01 Oct 2024 22:27:33 GMT  
		Size: 16.3 KB (16330 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:35429f6f5e6e27865ceb66390542c4ced215b20e92da3c56858bfe2dfa185f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6468213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81f190b4b3f5669d4b4c8d186e8bff9cd01ac2bc76e9470508ec4a4a530c2cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f06dff9b4e827b724859232603047eb8f174ba53d47507a068e30bb1faf7ad2`  
		Last Modified: Tue, 01 Oct 2024 22:18:01 GMT  
		Size: 3.0 MB (3006281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b79c8e80730fe38674163c1ecb066f43bc26fc731757556c8b3d46e97f08b8`  
		Last Modified: Tue, 01 Oct 2024 22:18:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8110c5608769ca74fe8293292d1c4924524ba0b676b29ee1922a7ad8534ae42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e580382a2c598328f027315284203d40003bdacba7bd24f49dd40daa0c826a`

```dockerfile
```

-	Layers:
	-	`sha256:e97165ed3a56328082e7dd8adfd51aeb3afb250ff86ae5c0464dc67684fcee46`  
		Last Modified: Tue, 01 Oct 2024 22:18:01 GMT  
		Size: 107.9 KB (107942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:006b31c11dd598a4b39d59f9373fe2f7e5b0b0bc33d4c90a81e952a292fcf88b`  
		Last Modified: Tue, 01 Oct 2024 22:18:01 GMT  
		Size: 16.3 KB (16291 bytes)  
		MIME: application/vnd.in-toto+json
