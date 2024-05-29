## `bash:devel`

```console
$ docker pull bash@sha256:5514fa4e320fa67e4898900cdf5e8e967205a8463d4c382ecf4a2c36e6b80e2a
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
$ docker pull bash@sha256:2cef3199126b3adfc79822127630b6203ed37c5df843fec9410783f5010a195d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59987fcc0bf660a8e8a03c4588738b32545bbab238730fac45fd4f2ac2301178`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_COMMIT=dbd27e54cc741b116d5ce0e731b778c4f014a74e
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_VERSION=devel-20240520
# Wed, 22 May 2024 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:33:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:33:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01fcb5759a3eb06bcdfa37bcd5c3fe4999acbce4e9a08c9ed207aa50151841d`  
		Last Modified: Wed, 22 May 2024 22:55:12 GMT  
		Size: 2.9 MB (2891428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ebbf418eb1bb78f452b8b545a226102220c1f2d63ce93e13c1c62fad5bfb83`  
		Last Modified: Wed, 22 May 2024 22:55:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ccbda17bf3625439fdeea8b96796ddd0c8b3b64d85e3892474646295697cfac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 KB (122852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32512b67cc13d4545d54eceaaade6bcecc3f4ff5cb827e3d8fd8bf675e5d0a66`

```dockerfile
```

-	Layers:
	-	`sha256:2ffa214794e6f23e513b8648838fe06c2410db402ca0244965142e8fd87ec993`  
		Last Modified: Wed, 22 May 2024 22:55:12 GMT  
		Size: 106.5 KB (106509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6918732451c7fe9599184ae8712da606d11cb3310e3077f9e92499e25c9553ac`  
		Last Modified: Wed, 22 May 2024 22:55:12 GMT  
		Size: 16.3 KB (16343 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:217ccbabfcd3240f0ca72b8d8a5e435c6bb7a28d193837e730b34b6761b32774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8d50b66590dc63e965b010e7aae502ea0b7f024f9e3a5472e0be1f03b3049b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 04:18:12 GMT
ENV _BASH_COMMIT=dbd27e54cc741b116d5ce0e731b778c4f014a74e
# Tue, 21 May 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240520
# Tue, 21 May 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 May 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 May 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e1beec0079f3860a9c89c069a4dbb376fc87fc54e47a4dcdf913ede2695107`  
		Last Modified: Tue, 21 May 2024 20:05:29 GMT  
		Size: 2.8 MB (2843301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911efe5393089ae50fd66d5bcb318032aeee23778772b1e02f9cdafb407b158`  
		Last Modified: Tue, 21 May 2024 20:05:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a9a0d92df5f8adb38f04eff7480d495db728f172239dda10260b515b7dd4dce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ef6668fd73ce310452e2ec33a4e3620b8b358fcc16a15c1a6cfcbde5fd7391`

```dockerfile
```

-	Layers:
	-	`sha256:f7a62888545f37b25ae054734371aefe8ac242fcaadef4c85fb16854be35c25d`  
		Last Modified: Tue, 21 May 2024 20:05:29 GMT  
		Size: 16.2 KB (16194 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:99b5dd1086148cbc7d45eb75fc732020a6df8e27ed057cd3671b069f5f446177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5707063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d73ce19d6b3d764e456a7d5e3276e02b00de743b0d5427bf3746715bb049b24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 21 May 2024 04:18:12 GMT
ENV _BASH_COMMIT=dbd27e54cc741b116d5ce0e731b778c4f014a74e
# Tue, 21 May 2024 04:18:12 GMT
ENV _BASH_VERSION=devel-20240520
# Tue, 21 May 2024 04:18:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 May 2024 04:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 May 2024 04:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 May 2024 04:18:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079699a186def8f1d087443ddf1d2b31f2693eb9247c995de112d67bc0da9de3`  
		Last Modified: Tue, 21 May 2024 21:18:47 GMT  
		Size: 2.8 MB (2787826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddd5db666143201fd6c5a2035e909e8cbb7615d3b2dc90f5d8c6f24f3b69d56`  
		Last Modified: Tue, 21 May 2024 21:18:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6de77b29ffe6f7d7163650882568ce2f7fcf21934569ee84848e16330e96afe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab61796a7321a94b87719a3e102df9982db76b263ecdfe42baddb1c930f467a`

```dockerfile
```

-	Layers:
	-	`sha256:045ea497a1959cacff6e3753a8af1121f49917f6a3a7c42a1ebccce361b489de`  
		Last Modified: Tue, 21 May 2024 21:18:47 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bdab5bc339455962c650390a5581b2691a173449a660cd879d7a1f765d2990`  
		Last Modified: Tue, 21 May 2024 21:18:47 GMT  
		Size: 16.2 KB (16248 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:e9952bec379024a12416fba1b4cb2ff6a9098448345abcc3f91d77f7d4c54d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7078833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180404a2e21248268977ad6d88a2eb42c157f155a06ff44cd81fa2fff899b604`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_COMMIT=dbd27e54cc741b116d5ce0e731b778c4f014a74e
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_VERSION=devel-20240520
# Wed, 22 May 2024 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:33:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:33:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5a6ff1a2c1a61bc892a35cdbf91679cdcd7ae04320df5985623e457a0def54`  
		Last Modified: Wed, 22 May 2024 23:18:34 GMT  
		Size: 3.0 MB (2991721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070ad4ca8aaa10a7870f6a48e89aebf92843e1bbaa8b618f8ff84b9be2054f40`  
		Last Modified: Wed, 22 May 2024 23:18:33 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:36e028af0825b43f672b293fc7918c62a4f2ddb5fb61be8f81e0e87dbb6256bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 KB (122873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0099387474bb0c5d7ba7d0f4919ef2c01b8cbf08ada87dddb4773f6d5f383ca9`

```dockerfile
```

-	Layers:
	-	`sha256:13320ed95dd40220ee5274f9d0f655a795d1023e686141fd3c29ad76e8841917`  
		Last Modified: Wed, 22 May 2024 23:18:33 GMT  
		Size: 106.5 KB (106520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5508b1a652fad62bfaad1e4c108fb4e1f9dad6a613039adacde3a2cb2192f8ad`  
		Last Modified: Wed, 22 May 2024 23:18:34 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:79d8ad730af5683cc59f9f1a02ba32ea82ad21d404f75e6cea6aee40ecd22c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6300578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267636ece7b55e5b7302cb8dd45766f776d15e09fb52eecc67a92e3cf59fc309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_COMMIT=dbd27e54cc741b116d5ce0e731b778c4f014a74e
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_VERSION=devel-20240520
# Wed, 22 May 2024 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:33:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:33:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda896fab0e8494c077956bfee0410a5de0370456159d5a324f4ca935c12b8a4`  
		Last Modified: Wed, 22 May 2024 22:55:14 GMT  
		Size: 2.8 MB (2833058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da15d50c29c29867252339be6a61e639eb04951813b6053ecd10d974d4002cb1`  
		Last Modified: Wed, 22 May 2024 22:55:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:09c30b71dc3ca85ff854376cf06e437c99cf4a2b11fbb62302f76a45457ee381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 KB (122798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12e6f578fe2291fc3ec6a5846c0b9bd642ec3cdb3f88ff1d9c3dd96e5641600`

```dockerfile
```

-	Layers:
	-	`sha256:bb18562bf3cdaa4d22b2f2a428ec2f73b1ef23d12a637d1a26e62cf703431ca5`  
		Last Modified: Wed, 22 May 2024 22:55:14 GMT  
		Size: 106.5 KB (106484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c579758c6c4dadb09c455607f646dc11c1409f3d4cb4df8fecba2fe9e7857db`  
		Last Modified: Wed, 22 May 2024 22:55:14 GMT  
		Size: 16.3 KB (16314 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:d58bcc12ce84157d8c62f541578ca8a7d27c76a25dfa85b3f4ff0297be06f115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8e36d496714ebba9a914f1776c74da3bbcd3e7ad1081b376a599d6af90925b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_COMMIT=dbd27e54cc741b116d5ce0e731b778c4f014a74e
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_VERSION=devel-20240520
# Wed, 22 May 2024 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:33:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:33:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c8979e2cfe6050f0b0ce1d1844168f564bed21e71820ac3e79f177fa6d4fe4`  
		Last Modified: Tue, 28 May 2024 23:16:55 GMT  
		Size: 3.2 MB (3163204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d36bfd6c08108c80b9d9f9953278f7299d7314a3c47405eaa08c6b71ffeb23`  
		Last Modified: Tue, 28 May 2024 23:16:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f338e52a5173a5edc64e4a8e244b9cb30ff3443f3dbe026a27a62097dfbdd604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 KB (120804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aabdedd2e7c8b20c2731e493bb1a586b0fd1576cf6fc5572286a963fa775d3`

```dockerfile
```

-	Layers:
	-	`sha256:828be32502e16187317a41042d7c81157677f7e3dcc2505ef20ff0a3255a9f23`  
		Last Modified: Tue, 28 May 2024 23:16:54 GMT  
		Size: 104.6 KB (104589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a36f838b23a423414aeb9e5dcf7a8ba2f209434b29530167baecd57a34be79a`  
		Last Modified: Tue, 28 May 2024 23:16:54 GMT  
		Size: 16.2 KB (16215 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:1743e9310bcf45c617369474986aeb2a16b97a8273ffd444b24cbd29cbf8a856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04566d3948d981dd5d0dda9a2d1f52470fb6776753c0f0c5ffca083df0964f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_COMMIT=dbd27e54cc741b116d5ce0e731b778c4f014a74e
# Wed, 22 May 2024 19:33:03 GMT
ENV _BASH_VERSION=devel-20240520
# Wed, 22 May 2024 19:33:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:33:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:33:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:33:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bddd6fa49f2cc1ab8fb2f467a13e76f50009f65660431e20b0a9e84b0a3442`  
		Last Modified: Thu, 23 May 2024 01:07:09 GMT  
		Size: 3.0 MB (2992237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12efb5dee3480a04a11ccff697b377dff7df060fb58d45d439302b52aeff7b3`  
		Last Modified: Thu, 23 May 2024 01:07:09 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:55587f0e2908a33c4a226a1bbacbaead81eb48993b701d8e9937353bc2f8c16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 KB (120899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0744b40b7a6de17913b22bc7c8fce8ec2e2c46ed77fe69ace6d6bc8f0054d925`

```dockerfile
```

-	Layers:
	-	`sha256:cff747e0e06c073b88371c005a249c0dc135a9d4cc0842e4c6a013e09ce7ca43`  
		Last Modified: Thu, 23 May 2024 01:07:09 GMT  
		Size: 104.6 KB (104555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3514bdb14747150d878fae0dc1f0b2afb509a11c599d06e61fbf92fdc889881f`  
		Last Modified: Thu, 23 May 2024 01:07:09 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
