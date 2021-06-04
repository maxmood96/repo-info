## `rakudo-star:alpine`

```console
$ docker pull rakudo-star@sha256:e8406e8e7c862be2977444ecf58772f2363a585538fe6e8a5330768b4b6f71e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:alpine` - linux; amd64

```console
$ docker pull rakudo-star@sha256:fabd7fd108880a3d146e814acd6c58b8cc0eabe1bbaf02d0fbfe1dacda6938c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44253017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191025b6c889caa8d972f7f2088b56e9fadf2e6dd325216cb2ba2134acf02feb`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Fri, 04 Jun 2021 00:00:03 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Fri, 04 Jun 2021 00:00:04 GMT
ARG rakudo_version=2021.04
# Fri, 04 Jun 2021 00:00:04 GMT
ENV rakudo_version=2021.04
# Fri, 04 Jun 2021 00:11:37 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Fri, 04 Jun 2021 00:11:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 04 Jun 2021 00:11:37 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f926f78c0f543da1d8221712988a02754c1ba359c7212f1ec6f97441aebdab97`  
		Last Modified: Fri, 04 Jun 2021 00:12:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca73a9af61ab7bf85d8556808fa8b75e6561dcaec4764f2c01723d52ba13261`  
		Last Modified: Fri, 04 Jun 2021 00:12:25 GMT  
		Size: 41.4 MB (41439790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:alpine` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:eb12738c4df5818a02f5482c8c3864e672a79a9eb630318afd1077e286aa6995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42208945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887224c9ae6f1de04ffba95bad2e6ace1c5c427f4652a7be2f54492ab48cc033`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Fri, 28 May 2021 11:13:45 GMT
RUN addgroup -S raku && adduser -S raku -G raku
# Fri, 28 May 2021 11:13:45 GMT
ARG rakudo_version=2020.10
# Fri, 28 May 2021 11:13:45 GMT
ENV rakudo_version=2020.10
# Fri, 28 May 2021 11:25:10 GMT
RUN buildDeps='         bash         gcc         gnupg         libc-dev         make         perl     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -eux     && export GNUPGHOME="$tmpdir"     && apk add --no-cache --virtual .build-deps $buildDeps     && mkdir ${tmpdir}/rakudo         && wget ${url}.asc -O ${tmpdir}/rakudo.tar.gz.asc     && wget $url -O ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && bash bin/rstar install -p /usr     )     && rm -rf $tmpdir     && apk del --no-network .build-deps
# Fri, 28 May 2021 11:25:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/core/bin:/usr/share/perl6/site/bin:/usr/share/perl6/vendor/bin
# Fri, 28 May 2021 11:25:11 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a1a3ef8ed22f59e56f4c136a3f0aa9f167b7e5f00a9c13dde85fe0d080cf9f`  
		Last Modified: Fri, 28 May 2021 11:25:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988bc508a443f626658cdd2678d201d6a294d26f3daf5fdc159566e8bede12c5`  
		Last Modified: Fri, 28 May 2021 11:25:59 GMT  
		Size: 39.5 MB (39496992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
