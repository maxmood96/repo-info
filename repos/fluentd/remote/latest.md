## `fluentd:latest`

```console
$ docker pull fluentd@sha256:022c4a066b2c1b5e7ff514920be483197d0f768862084daec4bf495ca0b8e706
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:d8750e23171914f5ab2ac4b065203378526d5514090b0df915e272f50db4964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13499259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d87a44d66174de902e064074a16ce13ebb2161ee79c98f493773be1bc1b968`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=
# Mon, 02 Dec 2024 04:34:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 02 Dec 2024 04:34:11 GMT
USER fluent
# Mon, 02 Dec 2024 04:34:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3d54f468907e82dab41fb62a511d1b32b8eef1be2cf4efc6d770728bd823f`  
		Last Modified: Tue, 03 Dec 2024 19:30:15 GMT  
		Size: 10.1 MB (10077361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958a857b518a5be5f36d36eaa1c73629868cf6aeaa32bf6d5f1fdd4a66a3a8f`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680417f5b9239d1e01ac56589e90d318cae2e2cc30b507169c53633db4f3c2dc`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebaee7b849635e6db3690ce13b5c688b4c859037efdcbeb4aa51afd41fe7fe1`  
		Last Modified: Tue, 03 Dec 2024 19:30:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:6f5e38ade8c8a8a57ff5d44a3a4021e24bf37abb94715cd859dd73335f2c9a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.5 KB (986531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b677fa1fda7a9ac0af25861b5b172b398e4c51c6ecdfb024150d2bc0f71ed5`

```dockerfile
```

-	Layers:
	-	`sha256:425b764cb7fe8fece92e7cb4381be08f5486502968b1a0329d545384bfb0b8d3`  
		Last Modified: Tue, 03 Dec 2024 19:30:14 GMT  
		Size: 971.7 KB (971674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1c660c347773a8f26cb45c8624288e5a6f738c0174427c2ee7d18e0bfd25758`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 14.9 KB (14857 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:5a782499ac1c52c4a93ec62c3536cc9aca41d3950ce84f7b8f1e456083c6ae2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12292332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdbe5254e01052564dea6d6fcc28b92c9629eca270edd19f985a4efac60c96f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=
# Mon, 02 Dec 2024 04:34:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 02 Dec 2024 04:34:11 GMT
USER fluent
# Mon, 02 Dec 2024 04:34:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f4cd1a385a777e8683b453a3a08433a07b34d58d27b4e122de41c4fe87e388`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 9.1 MB (9113732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d834a133f3b386e3ac9945ac2639af01b46ab85f5e1cd9a389988b168f6d7c1e`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7dddb7710ff8b62565cad3ab92d3c8c800014ce45f5f055df7138b4398a767`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc74b4c376e61be229f785d839eeb9baed816d712d3afad7a025e72e4122f54`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b91e915190814e127ca583dd9b16a9bd7f47122f92d4b449ff840a0777f03da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9a7ffe9c04b98274b9ddcafa5b6909bd072f92ca1e50f0f7638d3939691420`

```dockerfile
```

-	Layers:
	-	`sha256:af7946b6ba8f43866c1d7f3c2c0b89225722ea3a9b4e3ee86c440d52f1cf2105`  
		Last Modified: Tue, 03 Dec 2024 19:30:13 GMT  
		Size: 14.7 KB (14719 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:54e6dc832bab3fb4aea21713ec108116ac810b091731f399a10566093b02029f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17528351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80714cfb4bd9d5433bfedb0c7629229d9d79fabe08b55e7a40cf48e30b1e0c3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=
# Tue, 20 Aug 2024 02:01:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 20 Aug 2024 02:01:21 GMT
USER fluent
# Tue, 20 Aug 2024 02:01:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25692b121d4e504dd7cf76643d29ac69195c8a810ebfc13c3cac7ea6fbeaa59d`  
		Last Modified: Wed, 13 Nov 2024 01:43:20 GMT  
		Size: 14.2 MB (14166938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df696d4566a3c23ba05022314a55e7d5b92fb8563c3cbdb2a693596b3725ec8`  
		Last Modified: Wed, 13 Nov 2024 01:43:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc0733e2c8e04601cbaf7d3a87537709ba5a3647e29fbecdef9110aabca82f9`  
		Last Modified: Wed, 13 Nov 2024 01:43:19 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d66296d408054f195ce34d6c0fa0c9639a5a7ad876a13a24a6c3be242fcf3e`  
		Last Modified: Wed, 13 Nov 2024 01:43:19 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:9ed50ac2e1a3e0486830d71984287009b9554a0bf073f6f89d9041496c26f09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.2 KB (987214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5d585b2db9c3999b3a2a728e90fd20245c08ffafde5adae765df90819a1716`

```dockerfile
```

-	Layers:
	-	`sha256:54ca07680e68095425c21c06fda9a8ef2e30afc56188f7d35cd7063869d836ac`  
		Last Modified: Wed, 13 Nov 2024 01:43:20 GMT  
		Size: 973.1 KB (973130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e354d8fbd68249f023113ce7d73b72b5a9899223b6194b7d1984d9997af633a`  
		Last Modified: Wed, 13 Nov 2024 01:43:19 GMT  
		Size: 14.1 KB (14084 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:7b41115202b023c51b3e213c683a943866fe04e0a2d2d3b3031cb8b03fbccfc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12600022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a46fc6e0f6c5e413029b06fe8eb1d2ccf05bb20ff27092add92706a4b3eae2e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Mon, 02 Dec 2024 04:34:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.18.0
# Mon, 02 Dec 2024 04:34:11 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.4  && gem install rexml -v 3.3.9  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.18.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Mon, 02 Dec 2024 04:34:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Mon, 02 Dec 2024 04:34:11 GMT
ENV LD_PRELOAD=
# Mon, 02 Dec 2024 04:34:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Mon, 02 Dec 2024 04:34:11 GMT
USER fluent
# Mon, 02 Dec 2024 04:34:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Mon, 02 Dec 2024 04:34:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ab80d4d2b0222e03eca115215a16260e1a5f86f8b55e9b677e9d5c30b909a6af`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.3 MB (3253666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9087a139040da60c7dc1a640d09172bdd9cd977b7e3189f7f056f516203ebe74`  
		Last Modified: Tue, 03 Dec 2024 19:30:22 GMT  
		Size: 9.3 MB (9344193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9f87bc28b79eb4f8804d5c882853ddfb87ccaead1e77266a8669ea09e8fee2`  
		Last Modified: Tue, 03 Dec 2024 19:30:22 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2c0d6d1cc18848329fc98860e275e1b404256b49697e7352aaf601ca37f4aa`  
		Last Modified: Tue, 03 Dec 2024 19:30:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e594dbecaa3cb803d9acfa0c095d8ddd03862c677c32fff71d12c2916e643a`  
		Last Modified: Tue, 03 Dec 2024 19:30:22 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:107f76118084ca58145b8d1a5056a586492eda694b0c390e8adb807000c31a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 KB (983418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894648cc72e622871c705d7f5c2d1b591070ea95023e20da9675708000688abb`

```dockerfile
```

-	Layers:
	-	`sha256:917bea3a10208ec9ee409175daa8a4463a3176076b7999d3c10239a8da1c9527`  
		Last Modified: Tue, 03 Dec 2024 19:30:22 GMT  
		Size: 968.6 KB (968594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19be7cf7a0fe2c9492788a51969bb65d41b3ea0d59b930a1027167c4e4b1a66c`  
		Last Modified: Tue, 03 Dec 2024 19:30:22 GMT  
		Size: 14.8 KB (14824 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8d0b87f79f4fb0e7510ccb2e596233e2a14469ee6e849a54722153096ed13609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17096414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670d22d6a96527663e84ee091f5127297e23b252e920e94f17ec1331bdc268b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-ppc64le.tar.gz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=
# Tue, 20 Aug 2024 02:01:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 20 Aug 2024 02:01:21 GMT
USER fluent
# Tue, 20 Aug 2024 02:01:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c3045cb4f0dd3320c62c35c3443bc350e64a45c48666004b29e9912a645e7b35`  
		Last Modified: Tue, 12 Nov 2024 00:55:44 GMT  
		Size: 3.4 MB (3364499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b33c8f43c4eff1b8267303f140f58ade3c11f5e79fa0f491d637f8d4692774`  
		Last Modified: Tue, 12 Nov 2024 15:00:28 GMT  
		Size: 13.7 MB (13729746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f9b4ef26232b4d7bddcd73b8669a24b37263be741d91848688bf090f0fa03e`  
		Last Modified: Tue, 12 Nov 2024 15:00:28 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b409fee6cb320ebee1d7bfc44c2b93040bcc66b07a14c49187dcd5b4d4a5ff`  
		Last Modified: Tue, 12 Nov 2024 15:00:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85b6d0b2c47e3c99be8c0d0a18c0bf897e69f21ee2c2598b3c14cf09365916f`  
		Last Modified: Tue, 12 Nov 2024 15:00:28 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:e9be34173bff9e96af7c749f64d8a4f193ca4ad720504311737983351b660b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.7 KB (982705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a477e075435ead18a5a69526d6a2685c9050445a316f0b377e56c30ab2f4212f`

```dockerfile
```

-	Layers:
	-	`sha256:4f79bc3dca836a31276d9d2936ee94a375a32af7c5acdc0febc1dd4b8a9ddddb`  
		Last Modified: Tue, 12 Nov 2024 15:00:28 GMT  
		Size: 968.7 KB (968688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40371f60d5bdfca4e0c777e440a86b74fe457f1086f6208c713d6eae9342ade`  
		Last Modified: Tue, 12 Nov 2024 15:00:28 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:d657da921e0bfa7b572d63685d291d85730099b6fa0eb1fcd99bab7eac08f981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16954604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c881782596f745ad4889da75b98ca8d8ec966935124894ab9b08ee39edca5a0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 20 Aug 2024 02:01:21 GMT
ADD alpine-minirootfs-3.19.4-s390x.tar.gz / # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 20 Aug 2024 02:01:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.17.1
# Tue, 20 Aug 2024 02:01:21 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.5  && gem install json -v 2.7.2  && gem install rexml -v 3.3.5  && gem install async -v 1.32.1  && gem install async-http -v 0.64.2  && gem install fluentd -v 1.17.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 20 Aug 2024 02:01:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 20 Aug 2024 02:01:21 GMT
ENV LD_PRELOAD=
# Tue, 20 Aug 2024 02:01:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 20 Aug 2024 02:01:21 GMT
USER fluent
# Tue, 20 Aug 2024 02:01:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 20 Aug 2024 02:01:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6281353bb84e1beeb4deabf01093d4ab69b089bed69f3a95c18702b149677456`  
		Last Modified: Tue, 12 Nov 2024 00:56:12 GMT  
		Size: 3.3 MB (3253396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f736f1a1bd671aa3390f884a4606f3a4d5aea96bf2e1fd86773516ab90d5a3b0`  
		Last Modified: Tue, 12 Nov 2024 22:32:41 GMT  
		Size: 13.7 MB (13699041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0273588fe5cdd8b6d2d540cb2cfb09aade9bb1f266f07c8132126cf19f3816e2`  
		Last Modified: Tue, 12 Nov 2024 22:32:41 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea26cfb253ceff8e42c3bc0766f0f57e8d954589ac1aced7b6234e6a57ee4c5`  
		Last Modified: Tue, 12 Nov 2024 22:32:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cceb4da2286f8ad771d7c2ff0cefa56a2415682fdd7a6935c0e55839a7bd051`  
		Last Modified: Tue, 12 Nov 2024 22:32:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:ce2ae7cc4489fdfd8c45cb5acab0706fc4deda5e79163c50128184e9c8a6a735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.0 KB (982049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec227fefbd1f9ed888645cf1604ad7a8d14d5683a1d8a637dd5e1341fb6a5c2`

```dockerfile
```

-	Layers:
	-	`sha256:f28039044d4f47370abeea6cedf5f2bbf350578272b7c0c6c87ab292b0a03736`  
		Last Modified: Tue, 12 Nov 2024 22:32:41 GMT  
		Size: 968.1 KB (968072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1624b0fbe155fc5c1a22fea200c62b7ab527e5014ae9e970e48bbe8384b00f52`  
		Last Modified: Tue, 12 Nov 2024 22:32:41 GMT  
		Size: 14.0 KB (13977 bytes)  
		MIME: application/vnd.in-toto+json
