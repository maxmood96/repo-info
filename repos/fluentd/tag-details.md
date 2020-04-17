<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.9-1`](#fluentdv19-1)
-	[`fluentd:v1.9.1-1.0`](#fluentdv191-10)
-	[`fluentd:v1.9.1-debian-1.0`](#fluentdv191-debian-10)
-	[`fluentd:v1.9-debian-1`](#fluentdv19-debian-1)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:08afa70fbfc988563e887a7205ac52270c6f6c152b443204a0d68e5d499def52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:f0ecb6361bf8fd755713bfb7335c2cc2ad4460188ad6340204800918b9a7c6de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16521257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0f50ca7829aa85a5af485cba2c6f70f7ac4513909e032fa6595ef63c02d39b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:21:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:30:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:30:42 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:30:43 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:30:43 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:30:43 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:30:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:30:44 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:30:44 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:30:44 GMT
USER fluent
# Fri, 07 Feb 2020 23:30:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:30:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862b9ac1247f115d6ed5fccfa4122b2c91fb5a2cb20bdba2f2d65c625bf7cd38`  
		Last Modified: Fri, 07 Feb 2020 23:32:39 GMT  
		Size: 13.8 MB (13754916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cafa56e6c87f78764b903781b223c2e0d0e8c6b1b97446ac371a6693137299`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec7d5db4d0b21c67cc0b9bba7eeaa4af6aa7e666b3017e7347aacc514f5ea0`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9831d4e416eab5c9348870b47911d2aad383b39bf9e29bce6421af9543c6d4e`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:3cbf4516542cbb535ecaed8466d3f0364ec8d4afa8e709c38f8ad3dab1d6510e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15971489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92587c7c235fed0ccccf47210c7d051a710bc4eea33d7ed804dd6073035e6fd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:38 GMT
ADD file:7e840db4b1f91900bcc3693359908c82f531fc44027d4d5327ef598e8710ed0f in / 
# Thu, 23 Jan 2020 16:53:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 22:49:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 22:51:02 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 22:51:08 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 22:51:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 22:51:09 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 22:51:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 22:51:11 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 22:51:11 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 22:51:12 GMT
USER fluent
# Fri, 07 Feb 2020 22:51:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 22:51:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1c8737e28b1ca4452315b0127f7c6f4ad64f0c4695a3b52b1a4a3d2d17d3bbd5`  
		Last Modified: Thu, 23 Jan 2020 16:54:15 GMT  
		Size: 2.5 MB (2547672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c57e3e0115870bdc9f822f7e440c2c62b85524be33bb1fe79f70c01a81d96d`  
		Last Modified: Fri, 07 Feb 2020 22:51:42 GMT  
		Size: 13.4 MB (13421595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ff59b5f2cf8a70d8b3cbbf3bec899d6c6111384d8f29bc10c62637a14a20c`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3b75933b541a68291fd1e039e35e3fd9ac4a476f75abe40fc98a89e65fb381`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3970856d2b9e7c950ba9ce220ee79d0584a024fe68ca36603608f28e6dac7e80`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2d49be4a1370ddc86b67fb2af3bceaf94849814df51f0ed3d8bb6a948fa0e35c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16445833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedaf322edc90072768e95b5bd3396ea527c66a798c3ce22dfaffc0f42bb647d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:33:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:39:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:40:47 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:40:50 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:40:51 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:40:51 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:40:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:40:52 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:40:53 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:40:53 GMT
USER fluent
# Fri, 07 Feb 2020 23:40:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:40:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841babaa27d1e80c68a31eb60e0286a171473dc0d192017bc8f33b514620bbd`  
		Last Modified: Fri, 07 Feb 2020 23:44:28 GMT  
		Size: 13.8 MB (13750378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c7536a532d549238612448958b13eb237f2e46c93e7b680a33d7472642e7bb`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb414ccf876927e13a0412a99e84e66452b9d903cf9f2c8348a7b3ccf872eb`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56df000054891dd9243be6b43125d0cb2d09ccac880ab3659349618af9fd4b8a`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:5737f2000005fab4df0d07b2a5234b501e61b4cb4154c2f522547083d562b271
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16427837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c6ccbe8fc68b94a274be474eaf0910957bf50a8e365fc87be56db519b0b577`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:05 GMT
ADD file:4e7195ad2b3e9b85e4596b4a73719eb294f2a293a05b7b8e6096c4cfac0c6fde in / 
# Thu, 23 Jan 2020 16:53:05 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:55:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:38:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:39:08 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:39:09 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:39:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:39:09 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:39:09 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:39:10 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:39:10 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:39:10 GMT
USER fluent
# Fri, 07 Feb 2020 23:39:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:39:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fd25584d30bfc37afa2d99f41ef0a7055a4f2923907582dd992194fb4aa13f1c`  
		Last Modified: Thu, 23 Jan 2020 16:53:27 GMT  
		Size: 2.8 MB (2768519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff23c514810b9ca6a73f1e138e9f349ca6bb63546c029b31657f92cec32d9`  
		Last Modified: Fri, 07 Feb 2020 23:41:08 GMT  
		Size: 13.7 MB (13657151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557a6f32cb04f269164875f46b6037fdedaccab8722bb762378c0118c3618ab`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b5ad654d3d6f1c09dd12376071341f895ee77df103dec8318cc0e59d8d1c3e`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c20a7fe404958adf1fa560c3df30d0c30d5764b4f4dd58f2f49911a3dfa09`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:995bf55b3f99e030f679b2b12fd25058f8a422101cd2875b4717ca73bf559ddb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16963327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d340209ca4e24d09a4c75f89aa74076fd9509089a12ee172774c777f8dd12`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:58:09 GMT
ADD file:b06f16ae13d177baa99c50f4b42de9479a24ae5b68aa967b17dbe98760ed809e in / 
# Thu, 23 Jan 2020 16:58:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:14:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:17:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:18:11 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:18:21 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:18:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:18:25 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:18:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:18:33 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:18:39 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:18:44 GMT
USER fluent
# Fri, 07 Feb 2020 23:18:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:18:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2ef848e1434ec427ca147408f3c6f1cec160019050a04c8a2040f35872ab661b`  
		Last Modified: Thu, 23 Jan 2020 16:58:55 GMT  
		Size: 2.8 MB (2786373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104b5d6b35c6173435c38974cf197ba01062aa634ddd6a3f414f6e3f35e90390`  
		Last Modified: Fri, 07 Feb 2020 23:25:07 GMT  
		Size: 14.2 MB (14174734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328c08a9056e5b7115420fdd10b603d75eab5c1924c854ae01aa01d677d33bd8`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0f5c95314f7910ff39d452078f5811c788d82a3c8f98bd4562349e1712d92`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc023e6f8fddcc68b2d76adc9645961db0d2bbb4d0cdd84556d04b4f638befe`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:2cfa328ac48cd38be6b0791a809563048a9eb22ce0a2cc2b13d6b3cc8e8e05c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16439494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482ed245a3a307c1e2367419bcc9d0c0a15f23d5c9f54cb0fcce1fd982966281`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:49 GMT
ADD file:ca26e76455f243cd87071ecd6ebfbcde01ead913deefd2db5f75d99c561f9e65 in / 
# Thu, 23 Jan 2020 16:52:49 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:21:24 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:43:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:44:25 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:44:26 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:44:26 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:44:26 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:44:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:44:27 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:44:27 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:44:27 GMT
USER fluent
# Fri, 07 Feb 2020 23:44:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:44:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:62196161acf1e37f5a84921c7279f3a67078d6e98ce1deee27c00599e561af83`  
		Last Modified: Thu, 23 Jan 2020 16:53:12 GMT  
		Size: 2.5 MB (2549400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951d3122cae1eef051d0260d8ba3bf14d9edc8499a32fef206eeeecb3930f896`  
		Last Modified: Fri, 07 Feb 2020 23:46:16 GMT  
		Size: 13.9 MB (13887877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d5b72ba463218816ba35b947484675e269f601b3435a59ddb8b023df865ff`  
		Last Modified: Fri, 07 Feb 2020 23:46:14 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407141a4db6a01c3ab5d26d83887c7c5ba7726e596cf797408e50aea310718e6`  
		Last Modified: Fri, 07 Feb 2020 23:46:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9f7aaf0dcb6a0cb6f9fdce7e3367c572b311e8029707d6a181d72c95ac1fb6`  
		Last Modified: Fri, 07 Feb 2020 23:46:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-1`

```console
$ docker pull fluentd@sha256:08afa70fbfc988563e887a7205ac52270c6f6c152b443204a0d68e5d499def52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9-1` - linux; amd64

```console
$ docker pull fluentd@sha256:f0ecb6361bf8fd755713bfb7335c2cc2ad4460188ad6340204800918b9a7c6de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16521257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0f50ca7829aa85a5af485cba2c6f70f7ac4513909e032fa6595ef63c02d39b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:21:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:30:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:30:42 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:30:43 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:30:43 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:30:43 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:30:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:30:44 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:30:44 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:30:44 GMT
USER fluent
# Fri, 07 Feb 2020 23:30:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:30:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862b9ac1247f115d6ed5fccfa4122b2c91fb5a2cb20bdba2f2d65c625bf7cd38`  
		Last Modified: Fri, 07 Feb 2020 23:32:39 GMT  
		Size: 13.8 MB (13754916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cafa56e6c87f78764b903781b223c2e0d0e8c6b1b97446ac371a6693137299`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec7d5db4d0b21c67cc0b9bba7eeaa4af6aa7e666b3017e7347aacc514f5ea0`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9831d4e416eab5c9348870b47911d2aad383b39bf9e29bce6421af9543c6d4e`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:3cbf4516542cbb535ecaed8466d3f0364ec8d4afa8e709c38f8ad3dab1d6510e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15971489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92587c7c235fed0ccccf47210c7d051a710bc4eea33d7ed804dd6073035e6fd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:38 GMT
ADD file:7e840db4b1f91900bcc3693359908c82f531fc44027d4d5327ef598e8710ed0f in / 
# Thu, 23 Jan 2020 16:53:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 22:49:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 22:51:02 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 22:51:08 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 22:51:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 22:51:09 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 22:51:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 22:51:11 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 22:51:11 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 22:51:12 GMT
USER fluent
# Fri, 07 Feb 2020 22:51:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 22:51:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1c8737e28b1ca4452315b0127f7c6f4ad64f0c4695a3b52b1a4a3d2d17d3bbd5`  
		Last Modified: Thu, 23 Jan 2020 16:54:15 GMT  
		Size: 2.5 MB (2547672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c57e3e0115870bdc9f822f7e440c2c62b85524be33bb1fe79f70c01a81d96d`  
		Last Modified: Fri, 07 Feb 2020 22:51:42 GMT  
		Size: 13.4 MB (13421595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ff59b5f2cf8a70d8b3cbbf3bec899d6c6111384d8f29bc10c62637a14a20c`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3b75933b541a68291fd1e039e35e3fd9ac4a476f75abe40fc98a89e65fb381`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3970856d2b9e7c950ba9ce220ee79d0584a024fe68ca36603608f28e6dac7e80`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2d49be4a1370ddc86b67fb2af3bceaf94849814df51f0ed3d8bb6a948fa0e35c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16445833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedaf322edc90072768e95b5bd3396ea527c66a798c3ce22dfaffc0f42bb647d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:33:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:39:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:40:47 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:40:50 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:40:51 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:40:51 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:40:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:40:52 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:40:53 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:40:53 GMT
USER fluent
# Fri, 07 Feb 2020 23:40:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:40:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841babaa27d1e80c68a31eb60e0286a171473dc0d192017bc8f33b514620bbd`  
		Last Modified: Fri, 07 Feb 2020 23:44:28 GMT  
		Size: 13.8 MB (13750378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c7536a532d549238612448958b13eb237f2e46c93e7b680a33d7472642e7bb`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb414ccf876927e13a0412a99e84e66452b9d903cf9f2c8348a7b3ccf872eb`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56df000054891dd9243be6b43125d0cb2d09ccac880ab3659349618af9fd4b8a`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; 386

```console
$ docker pull fluentd@sha256:5737f2000005fab4df0d07b2a5234b501e61b4cb4154c2f522547083d562b271
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16427837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c6ccbe8fc68b94a274be474eaf0910957bf50a8e365fc87be56db519b0b577`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:05 GMT
ADD file:4e7195ad2b3e9b85e4596b4a73719eb294f2a293a05b7b8e6096c4cfac0c6fde in / 
# Thu, 23 Jan 2020 16:53:05 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:55:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:38:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:39:08 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:39:09 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:39:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:39:09 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:39:09 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:39:10 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:39:10 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:39:10 GMT
USER fluent
# Fri, 07 Feb 2020 23:39:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:39:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fd25584d30bfc37afa2d99f41ef0a7055a4f2923907582dd992194fb4aa13f1c`  
		Last Modified: Thu, 23 Jan 2020 16:53:27 GMT  
		Size: 2.8 MB (2768519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff23c514810b9ca6a73f1e138e9f349ca6bb63546c029b31657f92cec32d9`  
		Last Modified: Fri, 07 Feb 2020 23:41:08 GMT  
		Size: 13.7 MB (13657151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557a6f32cb04f269164875f46b6037fdedaccab8722bb762378c0118c3618ab`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b5ad654d3d6f1c09dd12376071341f895ee77df103dec8318cc0e59d8d1c3e`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c20a7fe404958adf1fa560c3df30d0c30d5764b4f4dd58f2f49911a3dfa09`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:995bf55b3f99e030f679b2b12fd25058f8a422101cd2875b4717ca73bf559ddb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16963327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d340209ca4e24d09a4c75f89aa74076fd9509089a12ee172774c777f8dd12`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:58:09 GMT
ADD file:b06f16ae13d177baa99c50f4b42de9479a24ae5b68aa967b17dbe98760ed809e in / 
# Thu, 23 Jan 2020 16:58:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:14:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:17:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:18:11 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:18:21 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:18:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:18:25 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:18:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:18:33 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:18:39 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:18:44 GMT
USER fluent
# Fri, 07 Feb 2020 23:18:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:18:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2ef848e1434ec427ca147408f3c6f1cec160019050a04c8a2040f35872ab661b`  
		Last Modified: Thu, 23 Jan 2020 16:58:55 GMT  
		Size: 2.8 MB (2786373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104b5d6b35c6173435c38974cf197ba01062aa634ddd6a3f414f6e3f35e90390`  
		Last Modified: Fri, 07 Feb 2020 23:25:07 GMT  
		Size: 14.2 MB (14174734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328c08a9056e5b7115420fdd10b603d75eab5c1924c854ae01aa01d677d33bd8`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0f5c95314f7910ff39d452078f5811c788d82a3c8f98bd4562349e1712d92`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc023e6f8fddcc68b2d76adc9645961db0d2bbb4d0cdd84556d04b4f638befe`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-1` - linux; s390x

```console
$ docker pull fluentd@sha256:2cfa328ac48cd38be6b0791a809563048a9eb22ce0a2cc2b13d6b3cc8e8e05c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16439494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482ed245a3a307c1e2367419bcc9d0c0a15f23d5c9f54cb0fcce1fd982966281`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:49 GMT
ADD file:ca26e76455f243cd87071ecd6ebfbcde01ead913deefd2db5f75d99c561f9e65 in / 
# Thu, 23 Jan 2020 16:52:49 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:21:24 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:43:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:44:25 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:44:26 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:44:26 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:44:26 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:44:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:44:27 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:44:27 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:44:27 GMT
USER fluent
# Fri, 07 Feb 2020 23:44:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:44:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:62196161acf1e37f5a84921c7279f3a67078d6e98ce1deee27c00599e561af83`  
		Last Modified: Thu, 23 Jan 2020 16:53:12 GMT  
		Size: 2.5 MB (2549400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951d3122cae1eef051d0260d8ba3bf14d9edc8499a32fef206eeeecb3930f896`  
		Last Modified: Fri, 07 Feb 2020 23:46:16 GMT  
		Size: 13.9 MB (13887877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d5b72ba463218816ba35b947484675e269f601b3435a59ddb8b023df865ff`  
		Last Modified: Fri, 07 Feb 2020 23:46:14 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407141a4db6a01c3ab5d26d83887c7c5ba7726e596cf797408e50aea310718e6`  
		Last Modified: Fri, 07 Feb 2020 23:46:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9f7aaf0dcb6a0cb6f9fdce7e3367c572b311e8029707d6a181d72c95ac1fb6`  
		Last Modified: Fri, 07 Feb 2020 23:46:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9.1-1.0`

```console
$ docker pull fluentd@sha256:08afa70fbfc988563e887a7205ac52270c6f6c152b443204a0d68e5d499def52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9.1-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:f0ecb6361bf8fd755713bfb7335c2cc2ad4460188ad6340204800918b9a7c6de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16521257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0f50ca7829aa85a5af485cba2c6f70f7ac4513909e032fa6595ef63c02d39b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:21:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:30:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:30:42 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:30:43 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:30:43 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:30:43 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:30:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:30:44 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:30:44 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:30:44 GMT
USER fluent
# Fri, 07 Feb 2020 23:30:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:30:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862b9ac1247f115d6ed5fccfa4122b2c91fb5a2cb20bdba2f2d65c625bf7cd38`  
		Last Modified: Fri, 07 Feb 2020 23:32:39 GMT  
		Size: 13.8 MB (13754916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cafa56e6c87f78764b903781b223c2e0d0e8c6b1b97446ac371a6693137299`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec7d5db4d0b21c67cc0b9bba7eeaa4af6aa7e666b3017e7347aacc514f5ea0`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9831d4e416eab5c9348870b47911d2aad383b39bf9e29bce6421af9543c6d4e`  
		Last Modified: Fri, 07 Feb 2020 23:32:37 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:3cbf4516542cbb535ecaed8466d3f0364ec8d4afa8e709c38f8ad3dab1d6510e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15971489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92587c7c235fed0ccccf47210c7d051a710bc4eea33d7ed804dd6073035e6fd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:38 GMT
ADD file:7e840db4b1f91900bcc3693359908c82f531fc44027d4d5327ef598e8710ed0f in / 
# Thu, 23 Jan 2020 16:53:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:09:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 22:49:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 22:51:02 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 22:51:08 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 22:51:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 22:51:09 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 22:51:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 22:51:11 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 22:51:11 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 22:51:12 GMT
USER fluent
# Fri, 07 Feb 2020 22:51:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 22:51:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1c8737e28b1ca4452315b0127f7c6f4ad64f0c4695a3b52b1a4a3d2d17d3bbd5`  
		Last Modified: Thu, 23 Jan 2020 16:54:15 GMT  
		Size: 2.5 MB (2547672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c57e3e0115870bdc9f822f7e440c2c62b85524be33bb1fe79f70c01a81d96d`  
		Last Modified: Fri, 07 Feb 2020 22:51:42 GMT  
		Size: 13.4 MB (13421595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6ff59b5f2cf8a70d8b3cbbf3bec899d6c6111384d8f29bc10c62637a14a20c`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3b75933b541a68291fd1e039e35e3fd9ac4a476f75abe40fc98a89e65fb381`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3970856d2b9e7c950ba9ce220ee79d0584a024fe68ca36603608f28e6dac7e80`  
		Last Modified: Fri, 07 Feb 2020 22:51:29 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2d49be4a1370ddc86b67fb2af3bceaf94849814df51f0ed3d8bb6a948fa0e35c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16445833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedaf322edc90072768e95b5bd3396ea527c66a798c3ce22dfaffc0f42bb647d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:58 GMT
ADD file:92767b5525acd9dbf8657931d32bdcc7cc504cdc33c95e84a75e478b00569bab in / 
# Thu, 23 Jan 2020 16:54:59 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:33:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:39:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:40:47 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:40:50 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:40:51 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:40:51 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:40:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:40:52 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:40:53 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:40:53 GMT
USER fluent
# Fri, 07 Feb 2020 23:40:54 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:40:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb93038481ddcf86a625b70f7551cdc583e38886f206fe7e40ad644008efa815`  
		Last Modified: Thu, 23 Jan 2020 16:55:31 GMT  
		Size: 2.7 MB (2693238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841babaa27d1e80c68a31eb60e0286a171473dc0d192017bc8f33b514620bbd`  
		Last Modified: Fri, 07 Feb 2020 23:44:28 GMT  
		Size: 13.8 MB (13750378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c7536a532d549238612448958b13eb237f2e46c93e7b680a33d7472642e7bb`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb414ccf876927e13a0412a99e84e66452b9d903cf9f2c8348a7b3ccf872eb`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56df000054891dd9243be6b43125d0cb2d09ccac880ab3659349618af9fd4b8a`  
		Last Modified: Fri, 07 Feb 2020 23:44:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5737f2000005fab4df0d07b2a5234b501e61b4cb4154c2f522547083d562b271
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16427837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c6ccbe8fc68b94a274be474eaf0910957bf50a8e365fc87be56db519b0b577`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:05 GMT
ADD file:4e7195ad2b3e9b85e4596b4a73719eb294f2a293a05b7b8e6096c4cfac0c6fde in / 
# Thu, 23 Jan 2020 16:53:05 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:55:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:38:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:39:08 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:39:09 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:39:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:39:09 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:39:09 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:39:10 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:39:10 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:39:10 GMT
USER fluent
# Fri, 07 Feb 2020 23:39:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:39:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fd25584d30bfc37afa2d99f41ef0a7055a4f2923907582dd992194fb4aa13f1c`  
		Last Modified: Thu, 23 Jan 2020 16:53:27 GMT  
		Size: 2.8 MB (2768519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373ff23c514810b9ca6a73f1e138e9f349ca6bb63546c029b31657f92cec32d9`  
		Last Modified: Fri, 07 Feb 2020 23:41:08 GMT  
		Size: 13.7 MB (13657151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557a6f32cb04f269164875f46b6037fdedaccab8722bb762378c0118c3618ab`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b5ad654d3d6f1c09dd12376071341f895ee77df103dec8318cc0e59d8d1c3e`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963c20a7fe404958adf1fa560c3df30d0c30d5764b4f4dd58f2f49911a3dfa09`  
		Last Modified: Fri, 07 Feb 2020 23:41:04 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:995bf55b3f99e030f679b2b12fd25058f8a422101cd2875b4717ca73bf559ddb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16963327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3d340209ca4e24d09a4c75f89aa74076fd9509089a12ee172774c777f8dd12`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:58:09 GMT
ADD file:b06f16ae13d177baa99c50f4b42de9479a24ae5b68aa967b17dbe98760ed809e in / 
# Thu, 23 Jan 2020 16:58:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:14:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:17:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:18:11 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:18:21 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:18:22 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:18:25 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:18:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:18:33 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:18:39 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:18:44 GMT
USER fluent
# Fri, 07 Feb 2020 23:18:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:18:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2ef848e1434ec427ca147408f3c6f1cec160019050a04c8a2040f35872ab661b`  
		Last Modified: Thu, 23 Jan 2020 16:58:55 GMT  
		Size: 2.8 MB (2786373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104b5d6b35c6173435c38974cf197ba01062aa634ddd6a3f414f6e3f35e90390`  
		Last Modified: Fri, 07 Feb 2020 23:25:07 GMT  
		Size: 14.2 MB (14174734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328c08a9056e5b7115420fdd10b603d75eab5c1924c854ae01aa01d677d33bd8`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf0f5c95314f7910ff39d452078f5811c788d82a3c8f98bd4562349e1712d92`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc023e6f8fddcc68b2d76adc9645961db0d2bbb4d0cdd84556d04b4f638befe`  
		Last Modified: Fri, 07 Feb 2020 23:25:03 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:2cfa328ac48cd38be6b0791a809563048a9eb22ce0a2cc2b13d6b3cc8e8e05c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16439494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482ed245a3a307c1e2367419bcc9d0c0a15f23d5c9f54cb0fcce1fd982966281`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:49 GMT
ADD file:ca26e76455f243cd87071ecd6ebfbcde01ead913deefd2db5f75d99c561f9e65 in / 
# Thu, 23 Jan 2020 16:52:49 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:21:24 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:43:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:44:25 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:44:26 GMT
RUN addgroup -S fluent && adduser -S -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:44:26 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:44:26 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:44:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:44:27 GMT
ENV LD_PRELOAD=
# Fri, 07 Feb 2020 23:44:27 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:44:27 GMT
USER fluent
# Fri, 07 Feb 2020 23:44:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:44:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:62196161acf1e37f5a84921c7279f3a67078d6e98ce1deee27c00599e561af83`  
		Last Modified: Thu, 23 Jan 2020 16:53:12 GMT  
		Size: 2.5 MB (2549400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951d3122cae1eef051d0260d8ba3bf14d9edc8499a32fef206eeeecb3930f896`  
		Last Modified: Fri, 07 Feb 2020 23:46:16 GMT  
		Size: 13.9 MB (13887877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7d5b72ba463218816ba35b947484675e269f601b3435a59ddb8b023df865ff`  
		Last Modified: Fri, 07 Feb 2020 23:46:14 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407141a4db6a01c3ab5d26d83887c7c5ba7726e596cf797408e50aea310718e6`  
		Last Modified: Fri, 07 Feb 2020 23:46:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9f7aaf0dcb6a0cb6f9fdce7e3367c572b311e8029707d6a181d72c95ac1fb6`  
		Last Modified: Fri, 07 Feb 2020 23:46:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9.1-debian-1.0`

```console
$ docker pull fluentd@sha256:5d5f3e42eb32498e333900bd73d01cb79081c2e8637e95d5b7760744c7e23c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9.1-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:117f08d69ccc55bc6fd481e8d7421d0ccdb30848496cd6a9b6aeb3f08078ab39
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85953418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f33e6c32c4b387cbf60154aeca66419f299bf0d9f8f7fc3b4ca8d950b0798d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 21:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 21:39:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 21:49:26 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 21:49:26 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 21:49:26 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 21:54:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 21:54:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 21:54:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 21:54:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 21:54:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 21:54:55 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 17:24:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 17:24:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 17:24:04 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 17:25:33 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 17:25:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 17:25:34 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 17:25:34 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 17:25:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 17:25:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 17:25:35 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 17:25:35 GMT
USER fluent
# Fri, 17 Apr 2020 17:25:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 17:25:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec858dd2763ee122a80d72ca9d5d5c49492583b3a805e89ee02cee6fdb58740`  
		Last Modified: Thu, 16 Apr 2020 22:23:29 GMT  
		Size: 12.5 MB (12539760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00fbbbd15a736b56c341301e35ce92c24309e7cb7b3dd65c5465453c57d8611`  
		Last Modified: Thu, 16 Apr 2020 22:23:26 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df95eee77c54a7a7785990b72d54afcd4a6f8420cb8a38dfc6e5a6d5b107e2a`  
		Last Modified: Thu, 16 Apr 2020 22:23:50 GMT  
		Size: 21.4 MB (21449379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27abfda62487dbc41f26aa5e7534109f126974bd5dd2830ddd233452393019f9`  
		Last Modified: Thu, 16 Apr 2020 22:23:47 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e750ecaeb45afb8972d8b084bf6cf6aeaf34c22ab1be5ca1ce11220aa5663285`  
		Last Modified: Fri, 17 Apr 2020 17:25:56 GMT  
		Size: 24.9 MB (24863123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a48164b6bd6789c8de0d2394fb1a909075b81994b7a8acaab961a5ecc67b8e`  
		Last Modified: Fri, 17 Apr 2020 17:25:52 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9bbc2b3c74c34708c50579a80fa73fe6df6294044570089d7957daa1696a22`  
		Last Modified: Fri, 17 Apr 2020 17:25:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2b2ec4edd35723dd2d241185da948e8cf08dbd4a9538e7094e46bfa324c1b5`  
		Last Modified: Fri, 17 Apr 2020 17:25:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:eb31df8eb5acdd1ef527ddfda5ba2d701698f34bc1ebb9c201881c45bfac3445
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79887603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e3064d0804408fe5c5638ef80c439db72f5a0e7ab41bb551cc1da992333d0c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 00:50:14 GMT
ADD file:761a556ec2a7d8c742c860e429c9b9ba3f7abfcd9383c6b3767499de6dcad4bc in / 
# Thu, 16 Apr 2020 00:50:15 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:08:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:08:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 07:12:54 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 07:12:56 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 07:12:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 07:16:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 07:16:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 07:16:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 07:16:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 07:16:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 07:16:46 GMT
CMD ["irb"]
# Thu, 16 Apr 2020 14:03:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 16 Apr 2020 14:03:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 16 Apr 2020 14:03:57 GMT
ENV TINI_VERSION=0.18.0
# Thu, 16 Apr 2020 14:07:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 16 Apr 2020 14:07:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 16 Apr 2020 14:07:29 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 16 Apr 2020 14:07:29 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 16 Apr 2020 14:07:30 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 16 Apr 2020 14:07:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 16 Apr 2020 14:07:31 GMT
EXPOSE 24224 5140
# Thu, 16 Apr 2020 14:07:32 GMT
USER fluent
# Thu, 16 Apr 2020 14:07:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 16 Apr 2020 14:07:33 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:600369660a591bc9594fcf333a847fe997901785f7032d3ad2822b2812c13243`  
		Last Modified: Thu, 16 Apr 2020 00:58:26 GMT  
		Size: 24.8 MB (24836437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14b9f33c17decf0c70dba5a4b3b21f31261cca521bd0e0119004bc2b6a05211`  
		Last Modified: Thu, 16 Apr 2020 07:32:59 GMT  
		Size: 10.3 MB (10326015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30429f0a88e73dca727ed9eb0aa9dbb79556ab08e07eb1dc220ca6dbdda041b8`  
		Last Modified: Thu, 16 Apr 2020 07:32:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f138e7d1a8a2833e808ac8039c6a476c6d1c8ec692b75a91b510a26832bae6a2`  
		Last Modified: Thu, 16 Apr 2020 07:33:34 GMT  
		Size: 20.7 MB (20713518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51d11bc777a0d834c9caf4e839984f8f5740b5173916d14ec7c7b7de0d94c6c`  
		Last Modified: Thu, 16 Apr 2020 07:33:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588002638994b12508c3077dae8aa64cc0d22a10f96597ac8c3fae6aea58ae26`  
		Last Modified: Thu, 16 Apr 2020 14:07:57 GMT  
		Size: 24.0 MB (24008571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0c2f670c6216bfa12797ca2ab2f783894e21760730b89ec6391e600d08cd39`  
		Last Modified: Thu, 16 Apr 2020 14:07:49 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa327ad8677b10e1842fe0c9b476b6aa42b12575af665247154226c7edbf57`  
		Last Modified: Thu, 16 Apr 2020 14:07:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88c8450c5e8360d3f39daa277635c2d4cc7ab2d99ba15f62e914e8848d42c33`  
		Last Modified: Thu, 16 Apr 2020 14:07:49 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:e124420ccd4e5dd375b13c64fe1067d1e3065186187a1e8a6cf4d16971f809ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77081546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df700128ee2c79c38df6eeaa6c3f636d8b9149b46f55ad37655de38d1e835baf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 00:59:45 GMT
ADD file:e346a36a456d66d8019344b5f7d60df8b5b24aea1461c19838982135ad1f4d7d in / 
# Thu, 16 Apr 2020 00:59:47 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 17:31:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 17:31:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 17:47:52 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 17:47:53 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 17:47:54 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 17:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 17:51:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 17:51:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 17:51:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 17:51:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 17:51:26 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 10:26:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 10:26:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 10:26:52 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 10:29:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 10:29:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 10:29:44 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 10:29:45 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 10:29:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 10:29:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 10:29:48 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 10:29:49 GMT
USER fluent
# Fri, 17 Apr 2020 10:29:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 10:29:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:838dc71644c10eab485c4bdfa3879e0fb9e72426de1239cfac1d4c05c23db7be`  
		Last Modified: Thu, 16 Apr 2020 01:08:59 GMT  
		Size: 22.7 MB (22705228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90689245dcf084a6cbe7d0e2eb03ac23596602ca04f8ebeea013edd9163eb36`  
		Last Modified: Thu, 16 Apr 2020 18:12:19 GMT  
		Size: 9.8 MB (9847368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8765a4f122f3e5882a72239acc339fd9c44eb6700bed6b4b33bf6e6a9182cc66`  
		Last Modified: Thu, 16 Apr 2020 18:12:15 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76519570303f782a281ca6e93a1d7576ddeec65f176c4571a8f749c971f3dc`  
		Last Modified: Thu, 16 Apr 2020 18:12:48 GMT  
		Size: 20.6 MB (20622413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8304cb30692800b6c30c0ee835408b3e4dd68255043f36572f6bbd7d270f0d3d`  
		Last Modified: Thu, 16 Apr 2020 18:12:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75ff7652520e2a2476859b2c995da48d4eb6c49cc11d4a195f3afdefdd0e35`  
		Last Modified: Fri, 17 Apr 2020 10:30:21 GMT  
		Size: 23.9 MB (23903476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fafecca7a068d49c9580d51ffbd77494422042b698c3275b2dae44bda192a6`  
		Last Modified: Fri, 17 Apr 2020 10:30:13 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5450dc58aecfe88ea0f17dcdaa63f4a4f68ac6d22b341ada1a5cb1a4f9b70047`  
		Last Modified: Fri, 17 Apr 2020 10:30:13 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e0bbfb7289830dadcdd1b1ca52ff8a5c84b1d61ff3fde7fb4b7c6b1b5c5132`  
		Last Modified: Fri, 17 Apr 2020 10:30:14 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f82ea36f929b4db45daa0e096c38152d7b2d40e93e6eeafe6146f19cbbd73368
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83255448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b786ceb5ed82ed34284bf3de304e4e739442f27f53a11460950f267e3c4270`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 19:30:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 19:30:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 19:38:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 19:38:10 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 19:38:12 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 19:41:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 19:41:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 19:41:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 19:41:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 19:41:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 19:41:42 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 11:31:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 11:31:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 11:31:32 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 11:34:29 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 11:34:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 11:34:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 11:34:35 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 11:34:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 11:34:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 11:34:38 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 11:34:39 GMT
USER fluent
# Fri, 17 Apr 2020 11:34:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 11:34:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdd33f108215db58bd0e6f140401d93c4b1b536c7ad089a4d0d0edcd2054704`  
		Last Modified: Thu, 16 Apr 2020 20:03:55 GMT  
		Size: 11.2 MB (11244664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b731403e546d6ee4346d854724aeec93f5a7d40b2896f756531171bb5634bf`  
		Last Modified: Thu, 16 Apr 2020 20:03:51 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a07cc279b68bee894882cdb8295d12fba14a21f2759618f21e2e41ec57136dc`  
		Last Modified: Thu, 16 Apr 2020 20:04:26 GMT  
		Size: 21.3 MB (21287940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a03216b543b88961e7600433fc393801a20caacb3e2fa5e42c65bd7e841559`  
		Last Modified: Thu, 16 Apr 2020 20:04:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fea13ad1bc58b9fa8029450158090337d45aef396f1b493dfa8a2714d594417`  
		Last Modified: Fri, 17 Apr 2020 11:35:02 GMT  
		Size: 24.9 MB (24862054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4149688bde9af13b204f968457d905fb6b5ecde45574eb9db8c60834af401db6`  
		Last Modified: Fri, 17 Apr 2020 11:34:55 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef322d0c58b72619341e8181d673b6dc4b15bba889e06063909fff33b1565662`  
		Last Modified: Fri, 17 Apr 2020 11:34:55 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b59e3b6c99be4d2958a60f67f0e30bc7362ab25a4953bddd309936d2dea4c6`  
		Last Modified: Fri, 17 Apr 2020 11:34:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:97d5f2ce78bc7ebb0be7ed64d44c32614e6bf525b3f07dd43524b8f0a6df3d81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89901821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c516dba573d9304ff1995067782370f755f0fc1093f1140d598806242708ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:55 GMT
ADD file:ab0bbfba6c4b56420ffffc6cdddcc4592fff018f0cd07578c7dc0a5faa49df2f in / 
# Thu, 16 Apr 2020 01:39:56 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 18:58:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 18:58:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 19:07:30 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 19:07:30 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 19:07:30 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 19:11:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 19:11:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 19:11:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 19:11:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 19:11:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 19:11:55 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 03:00:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 03:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 03:00:49 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 03:03:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 03:03:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 03:03:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 03:03:51 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 03:03:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 03:03:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 03:03:52 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 03:03:52 GMT
USER fluent
# Fri, 17 Apr 2020 03:03:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 03:03:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:75bc60a98e6523be3fadd9128c1a630cb5cbd2d2d813ee5e99dc146a3de22254`  
		Last Modified: Thu, 16 Apr 2020 01:46:20 GMT  
		Size: 27.8 MB (27753976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783bdcb00a31ddb1d118dfa8d886b0d2e30c62594fa8361a86e654efd45406e6`  
		Last Modified: Thu, 16 Apr 2020 19:37:48 GMT  
		Size: 17.2 MB (17206366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72053eeb282be50e3047d9cd2ae172aaad371c097382a1077137de3a97a9d3cc`  
		Last Modified: Thu, 16 Apr 2020 19:37:35 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15481f295fd66433885c614bfcf02bfabad0cd62b1c30ec711d6c40aa84c8f81`  
		Last Modified: Thu, 16 Apr 2020 19:38:26 GMT  
		Size: 20.9 MB (20884671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6649bd52b6b678aea81fed1c03dc5d4cee9289a9d1ef4d6cf8ca5daafcb94a`  
		Last Modified: Thu, 16 Apr 2020 19:38:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368b2a10146a1d706a0fa76584f599fd107ace38ef756f6b10211c98006c3742`  
		Last Modified: Fri, 17 Apr 2020 03:04:24 GMT  
		Size: 24.1 MB (24053806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09404772a94dbb8361623646a3911a5df162f4bbf2296525a7fe71e64d5fbaf4`  
		Last Modified: Fri, 17 Apr 2020 03:04:14 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a213f31572e131959b6da0f33cecbd776f3c0a08e683237cdfd68564d31fe81`  
		Last Modified: Fri, 17 Apr 2020 03:04:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b4824dc2b513dbab5d6e55ec528718cb31b67db377ae2560e001265154fc84`  
		Last Modified: Fri, 17 Apr 2020 03:04:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:403c7c0c21e5c008db1846820ff961b606cd79ae07a7ce7ca0252e133aa352a0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90614237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c6e3d83979f7632606abe4022bed23ed3cfd3dd8466ff8f55657cfc803c576`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 01:38:30 GMT
ADD file:9beea54416432abbd09d26b965c3c8e5bea8e233113f9bc308294c0008ee886f in / 
# Thu, 16 Apr 2020 01:38:39 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 19:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 19:16:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 19:28:29 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 19:28:31 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 19:28:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 19:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 19:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 19:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 19:34:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 19:34:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 19:34:20 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 14:06:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 14:06:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 14:06:55 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 14:10:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 14:10:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 14:10:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 14:10:54 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 14:10:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 14:10:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 14:11:03 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 14:11:06 GMT
USER fluent
# Fri, 17 Apr 2020 14:11:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 14:11:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f268991f8af64097bbfefa3f01dd3fdb7f715051a3681f352504a3ecaa9d3596`  
		Last Modified: Thu, 16 Apr 2020 01:54:39 GMT  
		Size: 30.5 MB (30524651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15685aad3fb9e1d84d711d87fb33735e4dd57b5932878df2ace869e4a780ceb6`  
		Last Modified: Thu, 16 Apr 2020 20:17:24 GMT  
		Size: 12.7 MB (12688931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f4d9d02c66049edc351b659f0f004509dd1c8be0260c16389859564015ff4e`  
		Last Modified: Thu, 16 Apr 2020 20:17:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18bc1f29ea478826b4de8fb21220b195b9a805aa4cdf5e049e01b9c760767ce`  
		Last Modified: Thu, 16 Apr 2020 20:18:18 GMT  
		Size: 22.0 MB (21969912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b3ebe4e226c0aa6e94eebb79d298a6dd9d9b34da659eef00e315a111f25221`  
		Last Modified: Thu, 16 Apr 2020 20:18:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bba79fbed0f3ecd1460bcaa8dc65d9cbd46b3ac88745953ff82ae6b52aee72`  
		Last Modified: Fri, 17 Apr 2020 14:11:41 GMT  
		Size: 25.4 MB (25427657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3107aba9932fa6d6b6fc8d24bf918a012426dc9d1a705ada70fa1615d1bbf0`  
		Last Modified: Fri, 17 Apr 2020 14:11:36 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0ba5005546ded83f9b07def8e6108bc3e980b7523e3476962adad5f4943a24`  
		Last Modified: Fri, 17 Apr 2020 14:11:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4813a5f48ac923687b351df1fa16ea4c92dbb84cd4766e9d631046c04811c`  
		Last Modified: Fri, 17 Apr 2020 14:11:36 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:6f8c44c274e11a154c96c269488799ea33e6e98bdfe245019936348e03afc14f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83123887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63ee3e0f99422e0dd6de0e63b8e39b3e2c7275f120153aa04f8ea8c63a42fa2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:19 GMT
ADD file:f328b5d6dce2eaf00360542c1e3280958b818268b9150b12ffd1fddf030daf2f in / 
# Thu, 16 Apr 2020 00:42:20 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 08:47:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 08:47:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 08:58:22 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 08:58:22 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 08:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 08:59:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 08:59:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 08:59:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 08:59:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 08:59:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 08:59:59 GMT
CMD ["irb"]
# Thu, 16 Apr 2020 15:41:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 16 Apr 2020 15:41:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 16 Apr 2020 15:41:29 GMT
ENV TINI_VERSION=0.18.0
# Thu, 16 Apr 2020 15:42:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 16 Apr 2020 15:42:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 16 Apr 2020 15:42:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 16 Apr 2020 15:42:50 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 16 Apr 2020 15:42:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 16 Apr 2020 15:42:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 16 Apr 2020 15:42:51 GMT
EXPOSE 24224 5140
# Thu, 16 Apr 2020 15:42:51 GMT
USER fluent
# Thu, 16 Apr 2020 15:42:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 16 Apr 2020 15:42:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:043f95f5412a986fb082b0193860bb9c0388c2fbcb5e8bf5bcbbeefb0e45c9c5`  
		Last Modified: Thu, 16 Apr 2020 00:46:19 GMT  
		Size: 25.7 MB (25712234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b75fe3310f9c32d5941f1caa91999b62d997dc4bf0e605396e9afccd42178c4`  
		Last Modified: Thu, 16 Apr 2020 09:11:15 GMT  
		Size: 10.8 MB (10796107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b70f5aaa809370d4906cf147578f4131e840a326a37b79fb926ed50ea4bad7f`  
		Last Modified: Thu, 16 Apr 2020 09:11:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d735d9ef922265545cb6cbd6c59664f169d700b71bd1b88c3185f0cdd582e0`  
		Last Modified: Thu, 16 Apr 2020 09:11:42 GMT  
		Size: 21.6 MB (21596699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06be3c628df077c7f2c9a751eabe7edb4552488b561f3a77f960a9e11e50e689`  
		Last Modified: Thu, 16 Apr 2020 09:11:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829a3abac3d8a220c8a247ed3da0bd9e7757b8cf3189a7372a34354a233d4331`  
		Last Modified: Thu, 16 Apr 2020 15:43:08 GMT  
		Size: 25.0 MB (25015777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae59e87f260cbbb61e8ee33640d9366cf5d9dd3961086116ac3345f6c2db6bbd`  
		Last Modified: Thu, 16 Apr 2020 15:43:06 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1e23554dd6528f1c363cfb5c5626960017564827136e3e50498f0019101761`  
		Last Modified: Thu, 16 Apr 2020 15:43:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b2df542cfb2632ad09fb206ba92331a772401a0e3eff06c6b8d932c45a2be2`  
		Last Modified: Thu, 16 Apr 2020 15:43:05 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-debian-1`

```console
$ docker pull fluentd@sha256:5d5f3e42eb32498e333900bd73d01cb79081c2e8637e95d5b7760744c7e23c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.9-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:117f08d69ccc55bc6fd481e8d7421d0ccdb30848496cd6a9b6aeb3f08078ab39
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85953418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f33e6c32c4b387cbf60154aeca66419f299bf0d9f8f7fc3b4ca8d950b0798d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 21:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 21:39:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 21:49:26 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 21:49:26 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 21:49:26 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 21:54:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 21:54:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 21:54:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 21:54:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 21:54:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 21:54:55 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 17:24:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 17:24:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 17:24:04 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 17:25:33 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 17:25:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 17:25:34 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 17:25:34 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 17:25:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 17:25:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 17:25:35 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 17:25:35 GMT
USER fluent
# Fri, 17 Apr 2020 17:25:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 17:25:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec858dd2763ee122a80d72ca9d5d5c49492583b3a805e89ee02cee6fdb58740`  
		Last Modified: Thu, 16 Apr 2020 22:23:29 GMT  
		Size: 12.5 MB (12539760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00fbbbd15a736b56c341301e35ce92c24309e7cb7b3dd65c5465453c57d8611`  
		Last Modified: Thu, 16 Apr 2020 22:23:26 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df95eee77c54a7a7785990b72d54afcd4a6f8420cb8a38dfc6e5a6d5b107e2a`  
		Last Modified: Thu, 16 Apr 2020 22:23:50 GMT  
		Size: 21.4 MB (21449379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27abfda62487dbc41f26aa5e7534109f126974bd5dd2830ddd233452393019f9`  
		Last Modified: Thu, 16 Apr 2020 22:23:47 GMT  
		Size: 144.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e750ecaeb45afb8972d8b084bf6cf6aeaf34c22ab1be5ca1ce11220aa5663285`  
		Last Modified: Fri, 17 Apr 2020 17:25:56 GMT  
		Size: 24.9 MB (24863123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a48164b6bd6789c8de0d2394fb1a909075b81994b7a8acaab961a5ecc67b8e`  
		Last Modified: Fri, 17 Apr 2020 17:25:52 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9bbc2b3c74c34708c50579a80fa73fe6df6294044570089d7957daa1696a22`  
		Last Modified: Fri, 17 Apr 2020 17:25:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2b2ec4edd35723dd2d241185da948e8cf08dbd4a9538e7094e46bfa324c1b5`  
		Last Modified: Fri, 17 Apr 2020 17:25:52 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:eb31df8eb5acdd1ef527ddfda5ba2d701698f34bc1ebb9c201881c45bfac3445
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79887603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e3064d0804408fe5c5638ef80c439db72f5a0e7ab41bb551cc1da992333d0c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 00:50:14 GMT
ADD file:761a556ec2a7d8c742c860e429c9b9ba3f7abfcd9383c6b3767499de6dcad4bc in / 
# Thu, 16 Apr 2020 00:50:15 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:08:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:08:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 07:12:54 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 07:12:56 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 07:12:57 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 07:16:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 07:16:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 07:16:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 07:16:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 07:16:45 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 07:16:46 GMT
CMD ["irb"]
# Thu, 16 Apr 2020 14:03:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 16 Apr 2020 14:03:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 16 Apr 2020 14:03:57 GMT
ENV TINI_VERSION=0.18.0
# Thu, 16 Apr 2020 14:07:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 16 Apr 2020 14:07:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 16 Apr 2020 14:07:29 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 16 Apr 2020 14:07:29 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 16 Apr 2020 14:07:30 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 16 Apr 2020 14:07:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 16 Apr 2020 14:07:31 GMT
EXPOSE 24224 5140
# Thu, 16 Apr 2020 14:07:32 GMT
USER fluent
# Thu, 16 Apr 2020 14:07:33 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 16 Apr 2020 14:07:33 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:600369660a591bc9594fcf333a847fe997901785f7032d3ad2822b2812c13243`  
		Last Modified: Thu, 16 Apr 2020 00:58:26 GMT  
		Size: 24.8 MB (24836437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14b9f33c17decf0c70dba5a4b3b21f31261cca521bd0e0119004bc2b6a05211`  
		Last Modified: Thu, 16 Apr 2020 07:32:59 GMT  
		Size: 10.3 MB (10326015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30429f0a88e73dca727ed9eb0aa9dbb79556ab08e07eb1dc220ca6dbdda041b8`  
		Last Modified: Thu, 16 Apr 2020 07:32:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f138e7d1a8a2833e808ac8039c6a476c6d1c8ec692b75a91b510a26832bae6a2`  
		Last Modified: Thu, 16 Apr 2020 07:33:34 GMT  
		Size: 20.7 MB (20713518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51d11bc777a0d834c9caf4e839984f8f5740b5173916d14ec7c7b7de0d94c6c`  
		Last Modified: Thu, 16 Apr 2020 07:33:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588002638994b12508c3077dae8aa64cc0d22a10f96597ac8c3fae6aea58ae26`  
		Last Modified: Thu, 16 Apr 2020 14:07:57 GMT  
		Size: 24.0 MB (24008571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0c2f670c6216bfa12797ca2ab2f783894e21760730b89ec6391e600d08cd39`  
		Last Modified: Thu, 16 Apr 2020 14:07:49 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa327ad8677b10e1842fe0c9b476b6aa42b12575af665247154226c7edbf57`  
		Last Modified: Thu, 16 Apr 2020 14:07:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88c8450c5e8360d3f39daa277635c2d4cc7ab2d99ba15f62e914e8848d42c33`  
		Last Modified: Thu, 16 Apr 2020 14:07:49 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:e124420ccd4e5dd375b13c64fe1067d1e3065186187a1e8a6cf4d16971f809ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77081546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df700128ee2c79c38df6eeaa6c3f636d8b9149b46f55ad37655de38d1e835baf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 00:59:45 GMT
ADD file:e346a36a456d66d8019344b5f7d60df8b5b24aea1461c19838982135ad1f4d7d in / 
# Thu, 16 Apr 2020 00:59:47 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 17:31:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 17:31:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 17:47:52 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 17:47:53 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 17:47:54 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 17:51:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 17:51:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 17:51:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 17:51:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 17:51:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 17:51:26 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 10:26:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 10:26:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 10:26:52 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 10:29:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 10:29:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 10:29:44 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 10:29:45 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 10:29:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 10:29:47 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 10:29:48 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 10:29:49 GMT
USER fluent
# Fri, 17 Apr 2020 10:29:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 10:29:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:838dc71644c10eab485c4bdfa3879e0fb9e72426de1239cfac1d4c05c23db7be`  
		Last Modified: Thu, 16 Apr 2020 01:08:59 GMT  
		Size: 22.7 MB (22705228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90689245dcf084a6cbe7d0e2eb03ac23596602ca04f8ebeea013edd9163eb36`  
		Last Modified: Thu, 16 Apr 2020 18:12:19 GMT  
		Size: 9.8 MB (9847368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8765a4f122f3e5882a72239acc339fd9c44eb6700bed6b4b33bf6e6a9182cc66`  
		Last Modified: Thu, 16 Apr 2020 18:12:15 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a76519570303f782a281ca6e93a1d7576ddeec65f176c4571a8f749c971f3dc`  
		Last Modified: Thu, 16 Apr 2020 18:12:48 GMT  
		Size: 20.6 MB (20622413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8304cb30692800b6c30c0ee835408b3e4dd68255043f36572f6bbd7d270f0d3d`  
		Last Modified: Thu, 16 Apr 2020 18:12:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75ff7652520e2a2476859b2c995da48d4eb6c49cc11d4a195f3afdefdd0e35`  
		Last Modified: Fri, 17 Apr 2020 10:30:21 GMT  
		Size: 23.9 MB (23903476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fafecca7a068d49c9580d51ffbd77494422042b698c3275b2dae44bda192a6`  
		Last Modified: Fri, 17 Apr 2020 10:30:13 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5450dc58aecfe88ea0f17dcdaa63f4a4f68ac6d22b341ada1a5cb1a4f9b70047`  
		Last Modified: Fri, 17 Apr 2020 10:30:13 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e0bbfb7289830dadcdd1b1ca52ff8a5c84b1d61ff3fde7fb4b7c6b1b5c5132`  
		Last Modified: Fri, 17 Apr 2020 10:30:14 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:f82ea36f929b4db45daa0e096c38152d7b2d40e93e6eeafe6146f19cbbd73368
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83255448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b786ceb5ed82ed34284bf3de304e4e739442f27f53a11460950f267e3c4270`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 19:30:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 19:30:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 19:38:08 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 19:38:10 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 19:38:12 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 19:41:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 19:41:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 19:41:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 19:41:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 19:41:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 19:41:42 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 11:31:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 11:31:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 11:31:32 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 11:34:29 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 11:34:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 11:34:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 11:34:35 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 11:34:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 11:34:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 11:34:38 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 11:34:39 GMT
USER fluent
# Fri, 17 Apr 2020 11:34:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 11:34:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdd33f108215db58bd0e6f140401d93c4b1b536c7ad089a4d0d0edcd2054704`  
		Last Modified: Thu, 16 Apr 2020 20:03:55 GMT  
		Size: 11.2 MB (11244664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b731403e546d6ee4346d854724aeec93f5a7d40b2896f756531171bb5634bf`  
		Last Modified: Thu, 16 Apr 2020 20:03:51 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a07cc279b68bee894882cdb8295d12fba14a21f2759618f21e2e41ec57136dc`  
		Last Modified: Thu, 16 Apr 2020 20:04:26 GMT  
		Size: 21.3 MB (21287940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a03216b543b88961e7600433fc393801a20caacb3e2fa5e42c65bd7e841559`  
		Last Modified: Thu, 16 Apr 2020 20:04:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fea13ad1bc58b9fa8029450158090337d45aef396f1b493dfa8a2714d594417`  
		Last Modified: Fri, 17 Apr 2020 11:35:02 GMT  
		Size: 24.9 MB (24862054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4149688bde9af13b204f968457d905fb6b5ecde45574eb9db8c60834af401db6`  
		Last Modified: Fri, 17 Apr 2020 11:34:55 GMT  
		Size: 1.8 KB (1844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef322d0c58b72619341e8181d673b6dc4b15bba889e06063909fff33b1565662`  
		Last Modified: Fri, 17 Apr 2020 11:34:55 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b59e3b6c99be4d2958a60f67f0e30bc7362ab25a4953bddd309936d2dea4c6`  
		Last Modified: Fri, 17 Apr 2020 11:34:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:97d5f2ce78bc7ebb0be7ed64d44c32614e6bf525b3f07dd43524b8f0a6df3d81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89901821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c516dba573d9304ff1995067782370f755f0fc1093f1140d598806242708ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:55 GMT
ADD file:ab0bbfba6c4b56420ffffc6cdddcc4592fff018f0cd07578c7dc0a5faa49df2f in / 
# Thu, 16 Apr 2020 01:39:56 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 18:58:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 18:58:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 19:07:30 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 19:07:30 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 19:07:30 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 19:11:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 19:11:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 19:11:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 19:11:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 19:11:54 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 19:11:55 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 03:00:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 03:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 03:00:49 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 03:03:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 03:03:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 03:03:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 03:03:51 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 03:03:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 03:03:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 03:03:52 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 03:03:52 GMT
USER fluent
# Fri, 17 Apr 2020 03:03:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 03:03:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:75bc60a98e6523be3fadd9128c1a630cb5cbd2d2d813ee5e99dc146a3de22254`  
		Last Modified: Thu, 16 Apr 2020 01:46:20 GMT  
		Size: 27.8 MB (27753976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783bdcb00a31ddb1d118dfa8d886b0d2e30c62594fa8361a86e654efd45406e6`  
		Last Modified: Thu, 16 Apr 2020 19:37:48 GMT  
		Size: 17.2 MB (17206366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72053eeb282be50e3047d9cd2ae172aaad371c097382a1077137de3a97a9d3cc`  
		Last Modified: Thu, 16 Apr 2020 19:37:35 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15481f295fd66433885c614bfcf02bfabad0cd62b1c30ec711d6c40aa84c8f81`  
		Last Modified: Thu, 16 Apr 2020 19:38:26 GMT  
		Size: 20.9 MB (20884671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6649bd52b6b678aea81fed1c03dc5d4cee9289a9d1ef4d6cf8ca5daafcb94a`  
		Last Modified: Thu, 16 Apr 2020 19:38:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368b2a10146a1d706a0fa76584f599fd107ace38ef756f6b10211c98006c3742`  
		Last Modified: Fri, 17 Apr 2020 03:04:24 GMT  
		Size: 24.1 MB (24053806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09404772a94dbb8361623646a3911a5df162f4bbf2296525a7fe71e64d5fbaf4`  
		Last Modified: Fri, 17 Apr 2020 03:04:14 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a213f31572e131959b6da0f33cecbd776f3c0a08e683237cdfd68564d31fe81`  
		Last Modified: Fri, 17 Apr 2020 03:04:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b4824dc2b513dbab5d6e55ec528718cb31b67db377ae2560e001265154fc84`  
		Last Modified: Fri, 17 Apr 2020 03:04:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:403c7c0c21e5c008db1846820ff961b606cd79ae07a7ce7ca0252e133aa352a0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90614237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c6e3d83979f7632606abe4022bed23ed3cfd3dd8466ff8f55657cfc803c576`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 01:38:30 GMT
ADD file:9beea54416432abbd09d26b965c3c8e5bea8e233113f9bc308294c0008ee886f in / 
# Thu, 16 Apr 2020 01:38:39 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 19:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 19:16:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 19:28:29 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 19:28:31 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 19:28:33 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 19:34:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 19:34:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 19:34:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 19:34:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 19:34:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 19:34:20 GMT
CMD ["irb"]
# Fri, 17 Apr 2020 14:06:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 17 Apr 2020 14:06:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 17 Apr 2020 14:06:55 GMT
ENV TINI_VERSION=0.18.0
# Fri, 17 Apr 2020 14:10:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 17 Apr 2020 14:10:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 17 Apr 2020 14:10:52 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 17 Apr 2020 14:10:54 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 17 Apr 2020 14:10:57 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 17 Apr 2020 14:10:59 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 17 Apr 2020 14:11:03 GMT
EXPOSE 24224 5140
# Fri, 17 Apr 2020 14:11:06 GMT
USER fluent
# Fri, 17 Apr 2020 14:11:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 17 Apr 2020 14:11:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f268991f8af64097bbfefa3f01dd3fdb7f715051a3681f352504a3ecaa9d3596`  
		Last Modified: Thu, 16 Apr 2020 01:54:39 GMT  
		Size: 30.5 MB (30524651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15685aad3fb9e1d84d711d87fb33735e4dd57b5932878df2ace869e4a780ceb6`  
		Last Modified: Thu, 16 Apr 2020 20:17:24 GMT  
		Size: 12.7 MB (12688931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f4d9d02c66049edc351b659f0f004509dd1c8be0260c16389859564015ff4e`  
		Last Modified: Thu, 16 Apr 2020 20:17:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18bc1f29ea478826b4de8fb21220b195b9a805aa4cdf5e049e01b9c760767ce`  
		Last Modified: Thu, 16 Apr 2020 20:18:18 GMT  
		Size: 22.0 MB (21969912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b3ebe4e226c0aa6e94eebb79d298a6dd9d9b34da659eef00e315a111f25221`  
		Last Modified: Thu, 16 Apr 2020 20:18:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bba79fbed0f3ecd1460bcaa8dc65d9cbd46b3ac88745953ff82ae6b52aee72`  
		Last Modified: Fri, 17 Apr 2020 14:11:41 GMT  
		Size: 25.4 MB (25427657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3107aba9932fa6d6b6fc8d24bf918a012426dc9d1a705ada70fa1615d1bbf0`  
		Last Modified: Fri, 17 Apr 2020 14:11:36 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0ba5005546ded83f9b07def8e6108bc3e980b7523e3476962adad5f4943a24`  
		Last Modified: Fri, 17 Apr 2020 14:11:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e4813a5f48ac923687b351df1fa16ea4c92dbb84cd4766e9d631046c04811c`  
		Last Modified: Fri, 17 Apr 2020 14:11:36 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:6f8c44c274e11a154c96c269488799ea33e6e98bdfe245019936348e03afc14f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83123887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63ee3e0f99422e0dd6de0e63b8e39b3e2c7275f120153aa04f8ea8c63a42fa2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:19 GMT
ADD file:f328b5d6dce2eaf00360542c1e3280958b818268b9150b12ffd1fddf030daf2f in / 
# Thu, 16 Apr 2020 00:42:20 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 08:47:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 08:47:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 16 Apr 2020 08:58:22 GMT
ENV RUBY_MAJOR=2.6
# Thu, 16 Apr 2020 08:58:22 GMT
ENV RUBY_VERSION=2.6.6
# Thu, 16 Apr 2020 08:58:23 GMT
ENV RUBY_DOWNLOAD_SHA256=5db187882b7ac34016cd48d7032e197f07e4968f406b0690e20193b9b424841f
# Thu, 16 Apr 2020 08:59:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 16 Apr 2020 08:59:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 16 Apr 2020 08:59:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 16 Apr 2020 08:59:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 08:59:59 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 16 Apr 2020 08:59:59 GMT
CMD ["irb"]
# Thu, 16 Apr 2020 15:41:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 16 Apr 2020 15:41:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 16 Apr 2020 15:41:29 GMT
ENV TINI_VERSION=0.18.0
# Thu, 16 Apr 2020 15:42:48 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 16 Apr 2020 15:42:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 16 Apr 2020 15:42:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 16 Apr 2020 15:42:50 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 16 Apr 2020 15:42:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 16 Apr 2020 15:42:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 16 Apr 2020 15:42:51 GMT
EXPOSE 24224 5140
# Thu, 16 Apr 2020 15:42:51 GMT
USER fluent
# Thu, 16 Apr 2020 15:42:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 16 Apr 2020 15:42:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:043f95f5412a986fb082b0193860bb9c0388c2fbcb5e8bf5bcbbeefb0e45c9c5`  
		Last Modified: Thu, 16 Apr 2020 00:46:19 GMT  
		Size: 25.7 MB (25712234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b75fe3310f9c32d5941f1caa91999b62d997dc4bf0e605396e9afccd42178c4`  
		Last Modified: Thu, 16 Apr 2020 09:11:15 GMT  
		Size: 10.8 MB (10796107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b70f5aaa809370d4906cf147578f4131e840a326a37b79fb926ed50ea4bad7f`  
		Last Modified: Thu, 16 Apr 2020 09:11:13 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d735d9ef922265545cb6cbd6c59664f169d700b71bd1b88c3185f0cdd582e0`  
		Last Modified: Thu, 16 Apr 2020 09:11:42 GMT  
		Size: 21.6 MB (21596699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06be3c628df077c7f2c9a751eabe7edb4552488b561f3a77f960a9e11e50e689`  
		Last Modified: Thu, 16 Apr 2020 09:11:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829a3abac3d8a220c8a247ed3da0bd9e7757b8cf3189a7372a34354a233d4331`  
		Last Modified: Thu, 16 Apr 2020 15:43:08 GMT  
		Size: 25.0 MB (25015777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae59e87f260cbbb61e8ee33640d9366cf5d9dd3961086116ac3345f6c2db6bbd`  
		Last Modified: Thu, 16 Apr 2020 15:43:06 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1e23554dd6528f1c363cfb5c5626960017564827136e3e50498f0019101761`  
		Last Modified: Thu, 16 Apr 2020 15:43:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b2df542cfb2632ad09fb206ba92331a772401a0e3eff06c6b8d932c45a2be2`  
		Last Modified: Thu, 16 Apr 2020 15:43:05 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
