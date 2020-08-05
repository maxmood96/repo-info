## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:e76e256d9edc931ce9c21c4d14a81a3e0101faa9b7a68ce7a32f8eb41a863302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rakudo-star:latest` - linux; amd64

```console
$ docker pull rakudo-star@sha256:a49292de4a41ca67f3e12110409bb361081a766525e05d5b40f294a8044950a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150001948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed7a15124ea9ddf9257fe57a3d3481bf8647a857843bf6e9192f2834d5e5e6d`
-	Default Command: `["raku"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:00:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 23:14:27 GMT
MAINTAINER Rob Hoelz
# Wed, 22 Jul 2020 23:14:28 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Wed, 22 Jul 2020 23:14:28 GMT
ARG rakudo_version=2020.01
# Wed, 22 Jul 2020 23:14:29 GMT
ENV rakudo_version=2020.01
# Wed, 22 Jul 2020 23:29:05 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 22 Jul 2020 23:29:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 22 Jul 2020 23:29:06 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed641c4ae9821ca3c399071ea82ae667237acbcaad1e367c3e1e87fc967834c`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 7.8 MB (7811702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd57146431eae70720cf24877e818256ae1a30b9c1c9e7d0ad093c945ca0af2`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 10.0 MB (9996319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac34a4d7c330794ec24a76e7e58b50d4c8f6a2fc77ca958d83092c8962e7d6d7`  
		Last Modified: Wed, 22 Jul 2020 03:16:44 GMT  
		Size: 51.8 MB (51829832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de580b425d6edb19f5ea8f38c97e1929509eda5e92b1e628b4940ddcbc6d6a0`  
		Last Modified: Wed, 22 Jul 2020 23:29:18 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da746470630ade3f48c20198edcde8e44fbda2b2976cd7c755e3dce685b013b`  
		Last Modified: Wed, 22 Jul 2020 23:29:26 GMT  
		Size: 30.0 MB (29972013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rakudo-star:latest` - linux; arm64 variant v8

```console
$ docker pull rakudo-star@sha256:8afa08ffd328d49c49f9653acaed3170443207a931bd1db526a5f9475cc1a523
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148507889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3c93e57a13b958a6634ad929c6886249f5799bbb9af884f18bf61a68e35ee3`
-	Default Command: `["raku"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:06 GMT
ADD file:ce999027b153d392f8a0f85e2e7a17b9279f3cf7ad0e45192378d527275f99c6 in / 
# Tue, 04 Aug 2020 06:57:08 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:10:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:10:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 11:10:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 07:45:44 GMT
MAINTAINER Rob Hoelz
# Wed, 05 Aug 2020 07:45:47 GMT
RUN groupadd -r raku && useradd -r -g raku raku
# Wed, 05 Aug 2020 07:45:48 GMT
ARG rakudo_version=2020.01
# Wed, 05 Aug 2020 07:45:49 GMT
ENV rakudo_version=2020.01
# Wed, 05 Aug 2020 08:08:31 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '         url="https://rakudo.org/dl/star/rakudo-star-${rakudo_version}.tar.gz"     keyserver='ha.pool.sks-keyservers.net'     keyfp='ECF8B611205B447E091246AF959E3D6197190DD5 7A6C9EB8809CFEAF0ED4E09F18C438E6FF24326D B6F697742EFCAF5F23CE51D5031D65902E840821'     tmpdir="$(mktemp -d)"     && set -x     && export GNUPGHOME="$tmpdir"     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir ${tmpdir}/rakudo         && curl -fsSL ${url}.asc -o ${tmpdir}/rakudo.tar.gz.asc     && curl -fsSL $url -o ${tmpdir}/rakudo.tar.gz     && gpg --batch --keyserver $keyserver --recv-keys $keyfp     && gpg --batch --verify ${tmpdir}/rakudo.tar.gz.asc ${tmpdir}/rakudo.tar.gz         && tar xzf ${tmpdir}/rakudo.tar.gz --strip-components=1 -C ${tmpdir}/rakudo     && (         cd ${tmpdir}/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf $tmpdir     && apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Aug 2020 08:08:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Wed, 05 Aug 2020 08:08:34 GMT
CMD ["raku"]
```

-	Layers:
	-	`sha256:d5517ee72007172d5b814636405254dea459120ce08f85777bb287d106a6a240`  
		Last Modified: Tue, 04 Aug 2020 07:03:41 GMT  
		Size: 49.2 MB (49175491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283897ad4463628bd259e1cbb5eb788e7df554b42ae17fc6f5d02c4a56035c2`  
		Last Modified: Tue, 04 Aug 2020 11:23:01 GMT  
		Size: 7.7 MB (7681458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb40d9f5fecfa098b8f7ece6c287c6fd61b114043c8b4647359120a7d943a3`  
		Last Modified: Tue, 04 Aug 2020 11:23:02 GMT  
		Size: 10.0 MB (9983917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b5fabb62f79acd92186da3c02d23bd8c15d79603a700959b582bd9e62854c`  
		Last Modified: Tue, 04 Aug 2020 11:23:28 GMT  
		Size: 52.2 MB (52163657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64adca0fec41bee3e39cfcb8bef6c779faad7240da23781100b13c74aa6fadce`  
		Last Modified: Wed, 05 Aug 2020 08:08:53 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74c0966995b42738b8eb02bc06deea980e6b81126b313f561f962bd6b0d29e7`  
		Last Modified: Wed, 05 Aug 2020 08:09:07 GMT  
		Size: 29.5 MB (29501599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
