## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:7d1769dcc2efd86eaff6383894714a32f799f0360b51a776821ab0a4f43e3cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:185e129596490f9648ecd17c147069cb0fb6ac5c88ebd9700e3f9c29459e3047
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42505492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71c4c9d6dd159035d0def22729e461050195e4b9acc7c64f618f1592f0b485`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Nov 2020 22:32:49 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Fri, 06 Nov 2020 22:32:49 GMT
ARG rakudo_version=2020.10
# Fri, 06 Nov 2020 22:32:49 GMT
ENV rakudo_version=2020.10
# Fri, 06 Nov 2020 22:43:53 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl         perl-encode     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del .build-deps
# Fri, 06 Nov 2020 22:43:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Fri, 06 Nov 2020 22:43:54 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406cfbc4ad756e663752335e88cabb755c8d030849d683c60669928705b16abe`  
		Last Modified: Fri, 06 Nov 2020 22:44:16 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98383171d5c236fb0d35f7b1f683d7dc1ce0aa2ecdb285b11d327d00dde4fad5`  
		Last Modified: Fri, 06 Nov 2020 22:44:25 GMT  
		Size: 39.7 MB (39707402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:221ea7fd1fb65e9517d5e51d6831ab9a509b7ec45d855f87f6b9067fb83748ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.9 MB (31939635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cc87342dbf7e66e1a629ba23269b90e12680d99df3f7d5275abd36923d7d95`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2020 04:02:56 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 29 Apr 2020 04:02:57 GMT
ARG rakudo_version=2020.01
# Wed, 29 Apr 2020 04:02:58 GMT
ENV rakudo_version=2020.01
# Wed, 29 Apr 2020 06:03:13 GMT
RUN buildDeps='         gnupg         perl         perl-encode         gcc         libc-dev         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apk del .build-deps
# Wed, 29 Apr 2020 06:03:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 29 Apr 2020 06:03:16 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a84906ed6937a6e0af1caf5edb5e8c4970a4717f4e68c82a4fb947abd8ad150`  
		Last Modified: Wed, 29 Apr 2020 06:03:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e4fdfa66c93b748ea85652aa2a5178dd5766f9ccc347b84f1930c3f66f8ee5`  
		Last Modified: Wed, 29 Apr 2020 06:03:52 GMT  
		Size: 29.2 MB (29219615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
