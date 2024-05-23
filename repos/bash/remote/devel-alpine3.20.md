## `bash:devel-alpine3.20`

```console
$ docker pull bash@sha256:837fdcf662bde6728d7b5dbfc3addf6017642633c76d01e728c04ccb1aa22ac9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-alpine3.20` - linux; amd64

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

### `bash:devel-alpine3.20` - unknown; unknown

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

### `bash:devel-alpine3.20` - linux; arm64 variant v8

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

### `bash:devel-alpine3.20` - unknown; unknown

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

### `bash:devel-alpine3.20` - linux; 386

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

### `bash:devel-alpine3.20` - unknown; unknown

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

### `bash:devel-alpine3.20` - linux; s390x

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

### `bash:devel-alpine3.20` - unknown; unknown

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
