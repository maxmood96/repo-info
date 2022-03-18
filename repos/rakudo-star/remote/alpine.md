## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:b126520ca0e44cf1871baff7d4e673d252c07db826347f0314dee12f45d0e254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:1350f863a3c144c321f0348f82c249f5b494459fd983a024e5648f5107605f59
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44260395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba07483ee7ca8cd662dfde4702de6b51a61f458acaaca78e5a60933296fbe9b`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:36 GMT
ADD file:51c08645923aa2d3513f66571f0c598a727dd5805e4f2bb87fb660b2f789348d in / 
# Thu, 17 Mar 2022 15:19:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 05:33:32 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Fri, 18 Mar 2022 05:33:32 GMT
ARG rakudo_version=2021.04
# Fri, 18 Mar 2022 05:33:32 GMT
ENV rakudo_version=2021.04
# Fri, 18 Mar 2022 05:49:33 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Fri, 18 Mar 2022 05:49:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 18 Mar 2022 05:49:34 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:e1096b72685a2366348e697f5b57e3b8feb41660e3dbe68447e168381515111a`  
		Last Modified: Thu, 17 Mar 2022 15:20:24 GMT  
		Size: 2.8 MB (2817181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9e14dcc503ba76fdbab99ab35ef1af5d285e6d42274808b96da1c6c32b6df0`  
		Last Modified: Fri, 18 Mar 2022 05:49:51 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1debf69148874429e49b0ef1c69b5e9360d74787241432e5ac02f70af4e4611d`  
		Last Modified: Fri, 18 Mar 2022 05:50:01 GMT  
		Size: 41.4 MB (41441958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:384d9268a75f3a3735d84dd873d5207ae189c135e1a89196c4474a6aee19e4d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43721128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff87c318d4dffb3eb9b251ba368417e93cb9e238679b1f87fd5e7a83222a35cf`
-	Default Command: `["raku"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:19 GMT
ADD file:0bbbf3ca52651bbef2547689474beafcef779899da63743efd8166a01d9f3f7a in / 
# Thu, 17 Mar 2022 18:43:20 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 19:45:29 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Thu, 17 Mar 2022 19:45:30 GMT
ARG rakudo_version=2021.04
# Thu, 17 Mar 2022 19:45:31 GMT
ENV rakudo_version=2021.04
# Thu, 17 Mar 2022 19:57:07 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Thu, 17 Mar 2022 19:57:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Thu, 17 Mar 2022 19:57:08 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:6b5c040bf1f18956758f68628afdc8e179044ac75bcd411134da39a661a772e0`  
		Last Modified: Thu, 17 Mar 2022 18:44:11 GMT  
		Size: 2.7 MB (2719134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea717d276872b676e23307cf0536de1b7879964e211c5f4ba27add5a6c97684e`  
		Last Modified: Thu, 17 Mar 2022 19:57:28 GMT  
		Size: 1.2 KB (1227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3788eb8eaf75ef7d435862230a6d9cff30dfaa85278390213a51ba8136049be3`  
		Last Modified: Thu, 17 Mar 2022 19:57:36 GMT  
		Size: 41.0 MB (41000767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
