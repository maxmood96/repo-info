## `bash:devel`

```console
$ docker pull bash@sha256:448dbcbef493f9858f5abca0a107c046e0fa8d6eefa43dae371dc41e095ea942
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
$ docker pull bash@sha256:773e87602753482837fc0ff29a249239a90c1cbffe3880cfdce467b94b8bb7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6531526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd39b66f5004015d5b8071f91588eca01311f5d765cd3c4e9c31ab0af1a349a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124ee53ecfac9b1b71fa553c95f391976db458c03b9f65743981e65cf638947d`  
		Last Modified: Tue, 22 Oct 2024 18:56:35 GMT  
		Size: 2.9 MB (2907382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1975ec31bb125ace5d82854cac75d66b0a112b1ff571aa4cd3f4d87aaa45e2db`  
		Last Modified: Tue, 22 Oct 2024 18:56:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ce81132566d232a5d587a793aa8b79e345ab3090a98d504ec860b60182fe35b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe140ea3a9405c8867fa8b7b65cf8d0f93cd84be159733e9813964036c18af15`

```dockerfile
```

-	Layers:
	-	`sha256:87aa31f8377e20cdd3bb39a821863f803bf96b17c9d582ce7324bf3f4dbe367c`  
		Last Modified: Tue, 22 Oct 2024 18:56:35 GMT  
		Size: 110.1 KB (110095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b49d1da0f0920800c9d51ec9bdb6f336df36ab6f7875df1121911ed88c2549e8`  
		Last Modified: Tue, 22 Oct 2024 18:56:35 GMT  
		Size: 16.2 KB (16169 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:704734073808717cd6fd74af443be6f93039a1ea86155c79e878a64f939b7f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6206a267d7db4b40b618789bd1f73d98596b73715c29ab1b7e4cfbc390511cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92f077a45faedc5efd8e85a03deaa2ceae7e498e148fd0ba0a9ab1c731fffd1`  
		Last Modified: Tue, 22 Oct 2024 18:57:07 GMT  
		Size: 2.9 MB (2857156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddc4655fa0abd25d263643e6485915ad93b02a8b5c69717d10586a9ae9ea342`  
		Last Modified: Tue, 22 Oct 2024 18:57:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:43d2224be8b402c912f2ae25b5dcc8e0b3c9c006fe299ed1a258e1fe70150292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (16024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c6b4103f607c56a5e4d7f58852625d6486f6e2bb6b8c568aed26b66bb2fae0`

```dockerfile
```

-	Layers:
	-	`sha256:71c48e38af5c72b610ffc1a98277ac8b6abbbab174532c16413d4a57284001f1`  
		Last Modified: Tue, 22 Oct 2024 18:57:07 GMT  
		Size: 16.0 KB (16024 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:b30d7edfe8ebe8c23a25a35ca98355a06b9c766a3a1a77739ab22c4d7c2d950e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329a4623691304433f2985811e6d06d41fea419ccc28dee4afe5041680ece55b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b16c694c346a63f2f99f8103a9eb3dc26a4f2f844766c8525826dbde6d59d4`  
		Last Modified: Tue, 22 Oct 2024 18:56:17 GMT  
		Size: 2.8 MB (2800311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3b4698cbbb780b004d698397a5a2c75f95a811b98154cb6d94a5a7042a845c`  
		Last Modified: Tue, 22 Oct 2024 18:56:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:69f1d930b14db5f91f10fd6ea0a9203cf0f271a8db2858c1a16b4fe01d5d4e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba0df8680beb15b8a5836764f2b950b006a46a214f6319ab7870c39219b6765`

```dockerfile
```

-	Layers:
	-	`sha256:d48b1e41d994e1917cafce7370b7139dd774343436f3e1d92069f4bfbc4b6687`  
		Last Modified: Tue, 22 Oct 2024 18:56:17 GMT  
		Size: 110.1 KB (110131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e851002a6841e79a4f1e0d296a624a386c8bb86e8cc231bad6788883b191379e`  
		Last Modified: Tue, 22 Oct 2024 18:56:17 GMT  
		Size: 16.2 KB (16239 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:1b4f97d146d6a08846519b0509e145686f719da6a3e639e05e34de91170e26ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7d4a22ee52dbcf94562efd4c4b485bf1d9a4d9ff01e6c79866ca350857cc97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3b29f4a53513015855c59160129814fbabe1c0d9313c409a31f07c434b6d12`  
		Last Modified: Tue, 22 Oct 2024 18:56:03 GMT  
		Size: 3.0 MB (3006811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf75ec970d339d6a78427ebd0734b195a524b0d9176e5e255ef6c5e2333a449b`  
		Last Modified: Tue, 22 Oct 2024 18:56:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8120367f6ce16efcc91163f01327491036a37d6325262adb2e45d3bb3edb4788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9672f309accf4c60b9122cbd60d6f2a9f449a9794ab7c87e2165f29a9d22e20a`

```dockerfile
```

-	Layers:
	-	`sha256:8168d112501533beebea12dc9f29f0244a1b8e59d886ab902048ec20ae2350ce`  
		Last Modified: Tue, 22 Oct 2024 18:56:03 GMT  
		Size: 110.2 KB (110151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed67a91f6dc80e1c83533eb2408a60db73a0ea4c9996b4447037082ae4c200f8`  
		Last Modified: Tue, 22 Oct 2024 18:56:03 GMT  
		Size: 16.3 KB (16267 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:19ce9e2200cecb9c77881f6b99c645da594368b97f1266e5961f3b2823667882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95eb1ae57b5917e57d6bfc3ad3709d8f33814cf605055d0baa960a8d066d721d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198b30afbf296b292bcf58689704865b47a9c11207f72d2152a71fef796470cf`  
		Last Modified: Tue, 22 Oct 2024 18:56:36 GMT  
		Size: 2.8 MB (2849029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670dcd4b38226351299fd39cf177bc8739a87a77a90700907d9a3906c833ba25`  
		Last Modified: Tue, 22 Oct 2024 18:56:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e87e1981a8ea1686f9641f2c8f2ad470d83fb59c935cc54929bda8ca3de80aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2090b7bed19fd6398ce6ef072c51637c278cb52c391e39abcef72ceea0ff7ed`

```dockerfile
```

-	Layers:
	-	`sha256:a26bba75bc6e3ba3af35fef350030a3fa7df05c4168f8fdc0f7f1ef0ed9b0df1`  
		Last Modified: Tue, 22 Oct 2024 18:56:36 GMT  
		Size: 110.1 KB (110070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a05d5decdd62db8fbc5fbeb7476e3bf8b057b897915389e4c8b6f97126cd3d6`  
		Last Modified: Tue, 22 Oct 2024 18:56:36 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:17586ce02b66ecb5797919127fb1f722b11074c4b83019e86f160516b8f6f99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6753158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3c64b6e79b6e459fec8606e5856c225292079be6590f851fc1da450641982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fa277b9cf5b72e6cdc031d9713ee1f8399a59e7d083eea6515e1f84f965e4b`  
		Last Modified: Tue, 22 Oct 2024 18:56:11 GMT  
		Size: 3.2 MB (3180404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082b08338dd3b686568bde533f77cf1c932ee6352088abbfcf680e72e33a1817`  
		Last Modified: Tue, 22 Oct 2024 18:56:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:50835eee208dad960eef075312fda2186049a90ddcbc842d27f0ca1c92e3c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 KB (124382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7070c1a5d08240983ba515ed1a3079ffc74beb5bbeb6445cb68f14fd2094ca0d`

```dockerfile
```

-	Layers:
	-	`sha256:e0744ff30f5dffd20feace5c3205a2447cab5dfb08cc8713f744cf26d0909d71`  
		Last Modified: Tue, 22 Oct 2024 18:56:10 GMT  
		Size: 108.2 KB (108175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d25098ecfc8e593bb1e53e8ca2b66e182c06a7ceed7fc38ea6a46f6ff73b591b`  
		Last Modified: Tue, 22 Oct 2024 18:56:10 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:9148413a603cbf68764c0ef7c35f0ae10121e12b1c2be969d28ad9b322805825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56180a5f5fc5b6952c7378eff21df54ca5ae9175b8e1323d13d4d3bad755cf4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5328eb4d0dd0cf373348f04ff553b2a12d01854fca01c604f14c66fca8134d`  
		Last Modified: Tue, 22 Oct 2024 19:02:41 GMT  
		Size: 2.9 MB (2857388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eabe017f282cdda5534a3fc1a4baafb69b7781adb289630d8d248c78561f4b4`  
		Last Modified: Tue, 22 Oct 2024 19:02:40 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:868a293c0f47eb6675413637df63a7af3db2e2f3eda083f34e66e5d661d0d7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 KB (124378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d09364dd771ce175c489a016ffee2a2179aea9b082ab90e4d6c3d0a8be95f7`

```dockerfile
```

-	Layers:
	-	`sha256:d9acebcb0c775b3815ed687af6ce7b0be7dfef2ff3e292800afb0c0415ca27c9`  
		Last Modified: Tue, 22 Oct 2024 19:02:40 GMT  
		Size: 108.2 KB (108171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5605d4a169fe8e967155adee80c806c9e8010ca4b5fed5435028657ee7a19047`  
		Last Modified: Tue, 22 Oct 2024 19:02:40 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:a04ccf6c644713db361b8b7a655dbaa6ea16ef557301c322eb18508f763b97c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6468836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54287095e64aacb2fcc02819947593472e25df896476e547d9f436d5bc12ca7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_COMMIT=261c6e8cc6c59b63be3a1597aadec72e9cf5ae72
# Tue, 22 Oct 2024 04:18:10 GMT
ENV _BASH_VERSION=devel-20241018
# Tue, 22 Oct 2024 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Oct 2024 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Oct 2024 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98552333b006e495fe01f2fd76fa2c64c0b025cc691311e0d4b63383ad653e08`  
		Last Modified: Tue, 22 Oct 2024 18:57:17 GMT  
		Size: 3.0 MB (3006901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcba5106d203d37287a622c7a4b347b4d79ec8cf14a6c88ccd89692b53f08c7f`  
		Last Modified: Tue, 22 Oct 2024 18:57:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1c7640deb5ac4dfc0ccf862d147b565bc485f6a8edcfa8f53950922852588b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 KB (124310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bebcb6918302145870bc0480b3a5b145b5e417736f82ea2b979575e9e571691`

```dockerfile
```

-	Layers:
	-	`sha256:598e7412d97c14805c0f0be4c60105138b976c3d0d9cccc0cb381952d01fc8c3`  
		Last Modified: Tue, 22 Oct 2024 18:57:17 GMT  
		Size: 108.1 KB (108141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51fddaf3e854e35de8bb266cb41b2fab3581fabda645bca454ef5778faad45a7`  
		Last Modified: Tue, 22 Oct 2024 18:57:17 GMT  
		Size: 16.2 KB (16169 bytes)  
		MIME: application/vnd.in-toto+json
