## `bash:devel-20250616-alpine3.22`

```console
$ docker pull bash@sha256:18317ef73278bc3ddb5b5f9f7a2b147e5526048935d6c18f805f5d337b9dde2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `bash:devel-20250616-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:da2fb174a9617248a3c7bec16555ed2431f940b3046676c43be56b3edb278eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900001b515523b91bf382e546f7c56ce9daeb79084a321c81d3255ea081a85d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e64cfb027ca45085bc44363aeca8e86d42050dc2ee28dc1bb054a6a1b00d059`  
		Last Modified: Tue, 17 Jun 2025 17:14:20 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6728372b7976c16505e4108bc16ee1568398e795d13cc9c2178f8cf048a9fce`  
		Last Modified: Tue, 17 Jun 2025 17:14:23 GMT  
		Size: 3.0 MB (2998203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543d8d9b19c4072d2abf5b6d98440f6ce9b74d3b6a5de04e557b10260d9870ff`  
		Last Modified: Tue, 17 Jun 2025 17:14:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250616-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:1e1594d62d101bb27668d5fb1704dc9dba3abd6974d792cac3e19fd9b26d8895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7febfa5c3d5bd1de689f0e6f768029947480c6bb8816a04ba09183f277e41d`

```dockerfile
```

-	Layers:
	-	`sha256:ba9b59780d4cc64427d0ddf66ba14e83eadb1d6d2ef833680ac9c8bd8f6c91fb`  
		Last Modified: Tue, 17 Jun 2025 18:02:42 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92d8576d68043c54e3fa859fdf91ccf1dde56233320d3aa9ed5bc9ee3ef977e`  
		Last Modified: Tue, 17 Jun 2025 18:02:43 GMT  
		Size: 17.7 KB (17708 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250616-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:e24d4afed57694317879ab91a6d5fe1ebb180c75b2e9b65560dfff8f1c3a03de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cb90f09f8757b21e1e9fc7cfd3afd01ffab348f0d04eb4acb08ac735d07890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa72c6a9e21dc757e636874754288c8a9e0c46684f2567c68530f8619b60f607`  
		Last Modified: Tue, 03 Jun 2025 22:50:33 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ee8c3f762b1058320a4d913f2f919b00c37090e69cd88964dffbe906233ad9`  
		Last Modified: Tue, 17 Jun 2025 17:14:18 GMT  
		Size: 2.9 MB (2934278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ee08308e529bc8050b57ca5a479d9e75d5f4a83c54a76b495b8e7743c8a8b`  
		Last Modified: Tue, 17 Jun 2025 17:14:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250616-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:0f17246ac8422baa0d9dfab753de3880a623a9917b38b36d7df3501d9f539ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff69bcfa762cacdbb010bd04f47dad4e1a9f761db8d90e808be0193116bd5f8`

```dockerfile
```

-	Layers:
	-	`sha256:9bbd0d8451401d3b5540686aff32eed3d14f1507b3e87d1ea04ae5b5f8aeef29`  
		Last Modified: Tue, 17 Jun 2025 18:02:47 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250616-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:9cb899a79a8b402830f473fc2db99c9f265b0bdf915d8f091fad36022901fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638b32e9df403bf88f189e6b567576726430431b5a776dbd04462ec034643422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c819c0679f438ddba9b06be4a6e783b330b7f5c4f96ad0ea2f2d1f74876f460`  
		Last Modified: Tue, 17 Jun 2025 17:14:30 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d71ef348f8cf4abff6b3b2756527deb56d55ff08eca16ab303bc2f70f2c15af`  
		Last Modified: Tue, 17 Jun 2025 17:14:34 GMT  
		Size: 2.9 MB (2925080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61058e1e2366608261402911edc2d64ddfaa0a9ee667efcfe655ef2240481948`  
		Last Modified: Tue, 17 Jun 2025 17:14:32 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250616-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:b114cf47afd08a602d5a57fefffb6f984657abc8da3c0684e0e3943f63f8217e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a6dc08f0cf70035f201df7dca2b400d0a890614efa3aa9ad1cabfffe5c1f31`

```dockerfile
```

-	Layers:
	-	`sha256:0f1135182a3e655d078fe1ddc6e87857d7a543ee8e8bcd01fcc38805666374f7`  
		Last Modified: Tue, 17 Jun 2025 18:02:51 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e886fc6f4a0fc04d581361aaa59bba714cb4d6322d6859a5f721ec57d072996`  
		Last Modified: Tue, 17 Jun 2025 18:02:52 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json
