## `bash:devel-20240119-alpine3.19`

```console
$ docker pull bash@sha256:f97e8281b51b17199a74b67eb396041850ed3ce4dc8b45aa2456a35051b456a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `bash:devel-20240119-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:994a55c0d52deb0950212e1fc9a78b584f9dcc0b11f0a154992e8d04813666ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5971329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb94a1870bb8d0fb943efc5b0c4b0768e23d0b925a045e510baeb3ee4c716b91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0422bcfc00f13984c86ab0641a8ad2f9eca707a1fb62dca019e9388546cde479`  
		Last Modified: Wed, 24 Jan 2024 20:56:48 GMT  
		Size: 2.8 MB (2805849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc819627c2d5a54128d2101447b7dbfcdb39bf855db8659edc0f2e80476bab9`  
		Last Modified: Wed, 24 Jan 2024 20:56:48 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240119-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6b515a86de745db8e841490a61238fe25ff7509f4ec34c984f37a2f8e3dd125c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6600266ef7c277e9d91d6f815bd69c87c71942fb7c99b089d79ff3115c83000`

```dockerfile
```

-	Layers:
	-	`sha256:30cda76b483b980c19e911b6012721b5bcf9c72820819a9f259cc107cf60a34f`  
		Last Modified: Wed, 24 Jan 2024 20:56:48 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240119-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:6b9b1befeb60d6ea7f1987577ae396793ca1b3da98521e29278c4f9aac48f121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa81cc7c125a67bb7311b02d90f0590991a36e6cf746f18dc3c59ab0e0df5d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_COMMIT=a4f44b7a11af874556529209fae7e8d261d51293
# Tue, 23 Jan 2024 05:18:01 GMT
ENV _BASH_VERSION=devel-20240119
# Tue, 23 Jan 2024 05:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jan 2024 05:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jan 2024 05:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b7fb6dbc104c0af2dabb1d9635843612091d701ea05c0a045f2d978310078`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 2.8 MB (2804622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a3368bf1e2c72bb5c2e339e229a816ec20a58e97c33405e3fea5a9420f69ef`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240119-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:5cc3905316c044dc288ff55ab11e9e8f200bbb24598485ada9273dac21697f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eae7c79aed8519ca9e6200f0c691a0bf737b5f33a996aee7497141ed7b541b`

```dockerfile
```

-	Layers:
	-	`sha256:a2b473636420e7e59a37c64eced4a28feba5205302aba8bd46e8e4ab23d46f02`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 97.7 KB (97707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e5976dbdc763694b995b861961a14f863fe53d50d84d6ee34186b91ac83eb8`  
		Last Modified: Wed, 24 Jan 2024 20:50:22 GMT  
		Size: 16.2 KB (16187 bytes)  
		MIME: application/vnd.in-toto+json
