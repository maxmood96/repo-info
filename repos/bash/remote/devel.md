## `bash:devel`

```console
$ docker pull bash@sha256:0c5752a0ab8f525cbbe9d0159a3bcc823b1e4e5bb4cd3f39dc9f9dbac05eed89
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
$ docker pull bash@sha256:c9f0f219d891981cdaf98259e42c47e9b3faaf99dc29cf1869c75a11601f8fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6278244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f71bf42089c5554f9a0049a292cefde984b54580c429aae6daf73434a8e213`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_COMMIT=43ecbeb31e5bbbc1a7557243af82b9f3e6390ced
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20240221
# Tue, 27 Feb 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d39df161924bd9dd0cf456f6aad44ba83ed55fbb0061e2d0d35d24b8b5b96d6`  
		Last Modified: Tue, 27 Feb 2024 20:51:49 GMT  
		Size: 2.9 MB (2869178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ae458ae26f5f14c9775df137724144e0720a27be5b90821e2160e6bc775ca8`  
		Last Modified: Tue, 27 Feb 2024 20:51:49 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f8bc157dde8c6c6387d75d6223f6ca9d52e88d8a0985159f29e82c693d2acd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84eaf387391f293d38a694e1bd3ed49d70fd1fd6adf41edebc59d4dd806b2bd8`

```dockerfile
```

-	Layers:
	-	`sha256:0eceeafd51e8b1ac83b7821795490b899a9cdcb09726e8dae8043fc2b988a212`  
		Last Modified: Tue, 27 Feb 2024 20:51:49 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d6a9f8821dcb3eb2a8faaef83f4c3524c23fe6439bbe1fa456307d5fb9ecf1`  
		Last Modified: Tue, 27 Feb 2024 20:51:50 GMT  
		Size: 16.3 KB (16251 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:9796083a69f354e4fcccb2956f3a796d748fe12cbfdfe657641e6811060c7e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5986986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c765df82088fb7f82dbec0bce043ddb508d7c768bb71dffcb0c21da84f36ffc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_COMMIT=43ecbeb31e5bbbc1a7557243af82b9f3e6390ced
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20240221
# Tue, 27 Feb 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f3685a6576d338d511026467c82b4a4bbe60facfdf27cfd61864172064a656`  
		Last Modified: Tue, 27 Feb 2024 20:51:29 GMT  
		Size: 2.8 MB (2821252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdf018eb3ddca0a690ac1228e43ace5262a59873d328406886f1cff2c3055c7`  
		Last Modified: Tue, 27 Feb 2024 20:51:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:eff6a8c0c8f83b66eede2d5801c9f854aa7b35fc7e5a28594446909d6db1bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932ed3675bd26e9de7e349b80aea2b8070b13d87b2c7e276e758b48b73a038e7`

```dockerfile
```

-	Layers:
	-	`sha256:99efa0712aecd10afd55eaf27cf299aa6ffb6d9c6ce205877ac8d21d4faf9bca`  
		Last Modified: Tue, 27 Feb 2024 20:51:29 GMT  
		Size: 15.9 KB (15941 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:4c9cb9c7d2bd0310c228c791218b9715c01e26db9af72bcf1241a7df83fced10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5687271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b13ad40b0f9280e56d1e16f3217b67f74a70a1aa76da2dae504cf7689fc2a47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_COMMIT=43ecbeb31e5bbbc1a7557243af82b9f3e6390ced
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20240221
# Tue, 27 Feb 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060917418c12362665493f30d0617dbbaf29b69f1c4c4c0190219b2cb9dd2492`  
		Last Modified: Tue, 27 Feb 2024 20:51:44 GMT  
		Size: 2.8 MB (2768039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d5375be49f6b7cd4fbd54b80e835d8fef304ecc031b2811b029de7d1380e8b`  
		Last Modified: Tue, 27 Feb 2024 20:51:43 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a0107126d018fc24804731fbc045e581f9a38a2bb571f6a33d92e3cda22d4b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c025e261e7fb55d46986da702512f8fd64fc091884c389ad914b9a0d0ea14f`

```dockerfile
```

-	Layers:
	-	`sha256:ffd96dfdcddb07e9547cba66604e006e73d718eb16c9cda7558c45c4f37db779`  
		Last Modified: Tue, 27 Feb 2024 20:51:43 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd3745f60fabd76979eee9362a81dd56770c8be53bbb4f5f68a3ddc08c1f1d2`  
		Last Modified: Tue, 27 Feb 2024 20:51:43 GMT  
		Size: 16.2 KB (16155 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:92a83252002fb60fba6299609e14ead78431421c81b1eb2fd480af8f3f0231e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89f65cc939a11d4030de8d691012a736ba6224fe960147675c6984b9be3bc8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_COMMIT=43ecbeb31e5bbbc1a7557243af82b9f3e6390ced
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20240221
# Tue, 27 Feb 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134367f8e35f0dc4f0d825373996f67dc0421d6869274907a33aea1779c3a53c`  
		Last Modified: Tue, 27 Feb 2024 20:52:48 GMT  
		Size: 3.0 MB (2972379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa4e4e53d92e481f27ad900f89a796d598458ce38b3351a2f21b77227daed8d`  
		Last Modified: Tue, 27 Feb 2024 20:52:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ee475f1b305bb097d32813ad11c63bfcc7cc5d399e10842e7cbb04ef3e6f69d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0a362cc5b1f3c195f08d5ca53a4fe8cf0beac0102db641719db5a2be9f05c`

```dockerfile
```

-	Layers:
	-	`sha256:336a93349af449b2fe00b32773be4ef3dc0fd90619d698c246a9ce41d7dec027`  
		Last Modified: Tue, 27 Feb 2024 20:52:48 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022ae0f854852de721bce2609b93de28bb2246df88a4a041773e8442dc0b529b`  
		Last Modified: Tue, 27 Feb 2024 20:52:47 GMT  
		Size: 16.1 KB (16096 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:1d3017bba385ba5301d9b8938a1afdc85d64db1d9dcd5a47f3127cc65c4cb6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6057757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527cc0a3afb1c3a37d7879f98dea55ffc9b3dcc080c0feefa5294c86d11ce21e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_COMMIT=54f3ed2278025081f897b9bd958fcf099fd5be18
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240304
# Tue, 05 Mar 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af798975e7b55e62f30bf7f40df6f9726c5a8a86a658492cde7240e30819628c`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 2.8 MB (2813334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a9c6784cee5e82e1503f386263304fe6ca8faf59743a037cf2d57ac7c9fdb6`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:750a505b5e6d718923ce4d9621118317148e0f108a4201fdffb8748eb66667e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4c68819f189e0482858ba23a29b1345450afdfc56ce10e64f4b35c6152381d`

```dockerfile
```

-	Layers:
	-	`sha256:a6e7719f0b943058b3ca2fb8660b6afab5f2a28262cc147a4b5312595a15deb6`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa50ac30e8179acdef3a8837a56737c3b01adffcc8ea168947f54215f68ae68a`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 16.2 KB (16195 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:9be587026993a40550d302be35ba241fba6bb3398e9e2cace469d2ab6905829c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6502955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138a21e605f88903aab696f244245bf9d83a55826b023263d43e145921ccf2d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_COMMIT=54f3ed2278025081f897b9bd958fcf099fd5be18
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240304
# Tue, 05 Mar 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526a0dd8a562e178a521176ca8de66e135ea756a83b1a03686f67e055cb093af`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 3.1 MB (3144266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f0b58760696b833488e3aa49c09a9c4a7a25d0daa8d41be78f2f7157da66e`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7d77e0801647afe4cab566336af0a2f1791f31170b5ffc1f0e9e43156d5b6bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c46c51ef93ebf1fe3f5194cf41cf7d4539858042e662e12e1a981e921e02111`

```dockerfile
```

-	Layers:
	-	`sha256:a590d19a451ad9e1c2bc8878816500d9b0af26ab6636eccac3457494cab2ae80`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46af97544ce61f7505f6a8bdc1fd9681440ac0f6a1cc29eb0051bdf423582d3`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 16.1 KB (16096 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:71b24b6b94c39795ff1e0c814ba50f75217f86c496744cf5aa11a23dc9d32f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a717b176e12b35d33ce41062f06a94cfd200909d9c315cf2992a23180844754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_COMMIT=54f3ed2278025081f897b9bd958fcf099fd5be18
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240304
# Tue, 05 Mar 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c4427d40245c21ae93d97c5edc31a68c299265c802414845b4b9474212024`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 3.0 MB (2970968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af49d10815172af409e369295c3632feea3c10de39faee583588ed6741df965`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3280529b64231fcb69142f7088377a56f75e7d711a3539c3a6607f931fd624ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2589ccf6c7efe82b3c6e353faf622db5bda50cfc2ccdff6d9618d32d8ff7140`

```dockerfile
```

-	Layers:
	-	`sha256:69fe56bfa426a4c974e95cfa067d3de4d4292c8e10b8a6f8476c2270463c5107`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94e9d360667c194a71174dadc15ffb15cdaea42cb331dafc46f534b66622d0a8`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 16.1 KB (16058 bytes)  
		MIME: application/vnd.in-toto+json
