## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:5ceb00fd65b4e0757e3b9d409c2ddee75a6461ee749b4323a57f17f23dd41d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:afa1287ffd0dd7a4f7e9eda4413a6db44fea0349267867eb4d045c53aa62d870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44253891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6b2308c66d4f98d46093f619d6c6ecef75713487ae0d609bb75c6af15589c`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 05:31:21 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Wed, 01 Sep 2021 05:31:22 GMT
ARG rakudo_version=2021.04
# Wed, 01 Sep 2021 05:31:22 GMT
ENV rakudo_version=2021.04
# Wed, 01 Sep 2021 05:42:29 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Wed, 01 Sep 2021 05:42:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Wed, 01 Sep 2021 05:42:30 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808c2518553c6a54b0365432153e8136c91eefdaea94c98566615a36b2b2df89`  
		Last Modified: Wed, 01 Sep 2021 05:42:44 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2096ab665aeaeab23021868ff13652759683bde4c547dbc030f93790238987d3`  
		Last Modified: Wed, 01 Sep 2021 05:42:52 GMT  
		Size: 41.4 MB (41438556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:de53babbc71e5a59c7b324aa203149831a915c0b6079c16a99896b8a86fc32e8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43492610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ba751091064204722ff8f9d54781cc837c0d367fa157ecbe90ce4a83efc0ed`
-	Default Command: `["raku"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:04:17 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Fri, 12 Nov 2021 19:04:18 GMT
ARG rakudo_version=2021.04
# Fri, 12 Nov 2021 19:04:19 GMT
ENV rakudo_version=2021.04
# Fri, 12 Nov 2021 19:20:48 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Fri, 12 Nov 2021 19:20:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 12 Nov 2021 19:20:49 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36b9beb576248b5b9cc394bfbf7a671e2c7f854a20f20fd07276c9f037376f2`  
		Last Modified: Fri, 12 Nov 2021 19:21:12 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7287b91118e11495947fa8f79b5ec45889ec80768e34807d2637258c3d9defc1`  
		Last Modified: Fri, 12 Nov 2021 19:21:20 GMT  
		Size: 40.8 MB (40771741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
