## `bash:devel`

```console
$ docker pull bash@sha256:82663b61039a37d9ff9579a849fb4d991e5249d94ebc24f7426f3f2c23a60941
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
$ docker pull bash@sha256:83b45005e0051c0d0dfb3cc96a095bf8b71bec4af2e9f3546af93ae17041461e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6268139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d9b9fa54ead01b73892b9b612642a78f97ec80aec3173f3050aef82f9eb4ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_COMMIT=138f3cc3591163d18ee4b6390ecd6894d5d16977
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_VERSION=devel-20240127
# Tue, 30 Jan 2024 11:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b9504f6d97b8015c3f246294ba9ab0e408fc6bf9dc491703804d86d4dc5620`  
		Last Modified: Tue, 30 Jan 2024 22:51:54 GMT  
		Size: 2.9 MB (2859073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e636233588d479b9365c9683457a0c40a6948ffc760c76b0b5c20cbec1f49c3`  
		Last Modified: Tue, 30 Jan 2024 22:51:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3ca425bb6aaf92c9699cdfe3d0ea514b93ddb424034f120b39b91267aa304a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c1bfedbbc82a762a22bb54094d6d6f2919e1953d988133c476fe798cc6f8e7`

```dockerfile
```

-	Layers:
	-	`sha256:bdaf33a73ceaf0a057bf42fb9de71e7c38bce8ffb17c1696b4c4e3e2cb4cae2f`  
		Last Modified: Tue, 30 Jan 2024 22:51:54 GMT  
		Size: 97.7 KB (97738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c56fd2697580810fc2bc2d4141de202cd3cdbb7cafa74a0436ea8496da7c5c2`  
		Last Modified: Tue, 30 Jan 2024 22:51:54 GMT  
		Size: 16.3 KB (16256 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:f9b2fbfe3a04c0b4216f2ab3e908a95b3fb40b1f45439652717ae5fc7d02f0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5972889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a39877a214f4c7a2d77176f502ce80e278e67668e952481107e482d70fd9f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_COMMIT=138f3cc3591163d18ee4b6390ecd6894d5d16977
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_VERSION=devel-20240127
# Tue, 30 Jan 2024 11:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d092566b558a919d6f0332040cc82f681685ad051f81c9a49eb3f8936af5b29d`  
		Last Modified: Tue, 30 Jan 2024 23:12:22 GMT  
		Size: 2.8 MB (2807161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa1f0405bb1b5d006caabd8590e1c2f97762f4084400ba63429b4c8f0516af2`  
		Last Modified: Tue, 30 Jan 2024 23:12:22 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ed01a72433260e126b8a181a0166202c2c4dc3817e93490d0ecae7621e0b341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce690abe0eeab73b7540428fece40dac3d47a32f69041f93ee8b06959d1464e0`

```dockerfile
```

-	Layers:
	-	`sha256:f360e3361dd70f2fb595adc39f40ceee2529a240fd0bb6411b2f07d2a217daca`  
		Last Modified: Tue, 30 Jan 2024 23:12:22 GMT  
		Size: 15.9 KB (15944 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:1662c5a52a4b6a409e1056fdafee924e56505f02deec6115e25dc6bc78c40ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5681997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5071499aff3b8db2fadfa4448879477dbb918e8edae2b125dc2db9e0e094bbd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39332213a9c9ff5e55f3b1dd79e467b712301f8aad7b6a5381ff3bd18958f0`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 2.8 MB (2762761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958384b65facfc72616cfd2de95db2b8f39f479a72cc6e30e92f3f963cd05a02`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0d8eb4faacf8c4cbac9ec506d9f37249d68508376e5a961c8ca29b8b87554dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (114014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7323eee9659c83f03fa786e31a25b1b81b518a9d760b243e880b99689a72af3`

```dockerfile
```

-	Layers:
	-	`sha256:0528a1914ce2c7c06ae34b3da240edb72b889cd04c331d27e3796f855d71cd63`  
		Last Modified: Tue, 06 Feb 2024 21:15:43 GMT  
		Size: 97.8 KB (97774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901aa743294bd7e455314a2a4bc43416a2c74193e91b09c4697547db27e4a1a8`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 16.2 KB (16240 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:70aafbc29fc59844eaa442104f5bea546657b815833f2c23c3a6196ca26ccdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6311139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1c896fbee07b7278b9dae50320a730d86f8c3b628eb1c9bdf5278d9f7ea5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_COMMIT=138f3cc3591163d18ee4b6390ecd6894d5d16977
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_VERSION=devel-20240127
# Tue, 30 Jan 2024 11:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a7c04385e3bb8401342f998615f9ff00bf11d1d3117c133cf2f7bd94faba5c`  
		Last Modified: Wed, 31 Jan 2024 00:03:53 GMT  
		Size: 3.0 MB (2963086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d33fda0db53a396512c37e21ce19e0622e5badeabb73a64857a5df455507d73`  
		Last Modified: Wed, 31 Jan 2024 00:03:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2f21116305e871b0554a02d76e0cb4a772cf3c700db9aa10ac4eb59c76baac1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 KB (113849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1bb635d1f711ef6a4b0ebb9cbf3b6d593fe7b71c4fc893148b6b52744a3376`

```dockerfile
```

-	Layers:
	-	`sha256:d8d9607dc1571200ec7e6d4d2f144a5fb1c109781901e2d0662c7cefcc1374a9`  
		Last Modified: Wed, 31 Jan 2024 00:03:52 GMT  
		Size: 97.7 KB (97749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9757937ebb315b45548e3d3d14d315a216f83a5798d10309bad050b5570b9a`  
		Last Modified: Wed, 31 Jan 2024 00:03:52 GMT  
		Size: 16.1 KB (16100 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:106d44f20fab5a6a137287e024a3634c676d95f7e775d51f83d17a387c97b683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deaea5065d9c35199ed5582ba3a56010e961bdf0390b9f4ac5538f0769ad9f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c74c168fe970d864f136115d0d7444a15005286b2f4e0abbe62a5f51f30bb2`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 2.8 MB (2807640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e87e1da61672f1558758ad618347805f4d429fc9b4ffecef717997b13e8b156`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:717f864553b7edbb153ae1895a2ce7dc63bf9a9faa68790cb7fb0b91b984a066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (114020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f89ed899a03284c65a418d691a18f3865c8af756d5382a50845c2f377601d25`

```dockerfile
```

-	Layers:
	-	`sha256:f9497b998df074fe61b87d932f996661e5858af78923361fffa0a61822a31278`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 97.7 KB (97713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e18368389c39de100deb12f90b6fcd2530de8423fb2bb541649ea1c31bbc79`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 16.3 KB (16307 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:5bbde3d14aebe57e0dfe2b0b4999948028799b0da82261c9d01a978fc2f24ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f974873a521c98b11efb6c6c8d77d54c9a6f38f7dafb1054673dc66b2b6cf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dac185e9baa17ae736bedc73bd1e314be8991800eb2489a37c7a07468e1daf`  
		Last Modified: Tue, 06 Feb 2024 21:14:08 GMT  
		Size: 3.1 MB (3135082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228b0860bdec7a5182a635f7663fb05b4e3bfa6880d6d292c285f78fc149efb`  
		Last Modified: Tue, 06 Feb 2024 21:14:07 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0d150750716c8c1f3134922c14cd58faa7dffd65a71cb276b59d06c1e543c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a04f8396478b2428d9ada38a1dd27a042c5557b7bf71daac5de84a08fae4ec`

```dockerfile
```

-	Layers:
	-	`sha256:6016a0fe176f6b8ed4f6102dc8447b8f5e04aefefb8ee42cb9767e5a981dbde1`  
		Last Modified: Tue, 06 Feb 2024 21:14:07 GMT  
		Size: 96.1 KB (96136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df60a4324a9ac4b639424c7c404f508b93d4b525b52d580b741646ad620cf57`  
		Last Modified: Tue, 06 Feb 2024 21:14:07 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:5386cff39a30c93d41177943a515fbf81faafaa73ae9d395f121377002e7ed45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6203127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5b46b8c092cf3ffa2d02e80f0d103d49f08b0ee778b2623d9314b1c7ce5700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_COMMIT=138f3cc3591163d18ee4b6390ecd6894d5d16977
# Tue, 30 Jan 2024 11:18:07 GMT
ENV _BASH_VERSION=devel-20240127
# Tue, 30 Jan 2024 11:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jan 2024 11:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Jan 2024 11:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27da5c42998f0d93e98e982d13139a632a4c07f40cd5eef8f3a9bf66cdf110b`  
		Last Modified: Wed, 31 Jan 2024 01:17:55 GMT  
		Size: 3.0 MB (2960155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db88fe4c89bf615761494a63ef774be866478eab35e380eb65f386d8fefd495`  
		Last Modified: Wed, 31 Jan 2024 01:17:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c9a74dae216464df89ca530e79a8316fdd6c738d977ab884f8c631d84ed6ad51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7917126ba6d73a8e212de8e4286fcdfed51437cc98d3fdef3ac96108fd211202`

```dockerfile
```

-	Layers:
	-	`sha256:c4258795a3874e097d760691dbccf4af640ea02e6100f74e86ea23a77b7e48ff`  
		Last Modified: Wed, 31 Jan 2024 01:17:55 GMT  
		Size: 96.1 KB (96102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccc870a2b488524b752edb39bc86fe58b1220b59e3fb88fa9b3ebd35c53208c3`  
		Last Modified: Wed, 31 Jan 2024 01:17:55 GMT  
		Size: 16.1 KB (16090 bytes)  
		MIME: application/vnd.in-toto+json
