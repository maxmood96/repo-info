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
$ docker pull fluentd@sha256:8a9cbfe2f92f8c91795b526c2867abd97ef220b1d2c5a800a161301f532330c2
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
$ docker pull fluentd@sha256:7f0c43a885a718075a6409f9c8c12b699b5dd15fdc52849dfbb6f143160a034d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85940245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab21435ee61df1ce5cf5686285fa444a38683a5c124cbbae16d2397777685eb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:34:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:34:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 18:45:10 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 18:45:10 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 18:45:10 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 18:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 18:48:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 18:48:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 18:48:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 18:48:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 18:48:45 GMT
CMD ["irb"]
# Thu, 27 Feb 2020 06:00:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 27 Feb 2020 06:00:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 27 Feb 2020 06:00:06 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 06:01:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 27 Feb 2020 06:01:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 27 Feb 2020 06:01:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 27 Feb 2020 06:01:35 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 27 Feb 2020 06:01:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 27 Feb 2020 06:01:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 27 Feb 2020 06:01:36 GMT
EXPOSE 24224 5140
# Thu, 27 Feb 2020 06:01:36 GMT
USER fluent
# Thu, 27 Feb 2020 06:01:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 27 Feb 2020 06:01:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55a61b57e3f6be04fbb54f4f49599cf38837e4be329c9010a4ef6977bdbd99a`  
		Last Modified: Wed, 26 Feb 2020 19:35:59 GMT  
		Size: 12.5 MB (12539730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56979ca8f121c1cc4b85f2c0bff0eb766aa71ada5964ad7a1ce801ae915f5d`  
		Last Modified: Wed, 26 Feb 2020 19:35:56 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a486fb9a30dac6e55b779c44e1dec51d7f68bdbd30b2251d8a5d0f75e979b372`  
		Last Modified: Wed, 26 Feb 2020 19:36:20 GMT  
		Size: 21.4 MB (21445518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4541c61250ed97cb558d4a38ac75e68ca5a45db2445eadbf6884015ed6bc75`  
		Last Modified: Wed, 26 Feb 2020 19:36:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a686cf8fac553c2d27ed0eff3d6358ef0428954c0ca0beec0d37d5ddc1a62d4`  
		Last Modified: Thu, 27 Feb 2020 06:01:57 GMT  
		Size: 24.9 MB (24860166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5fe5aca975bc22d1c80ed8b30d1b15ac6959bb184f98b0ec47b30cfa304968`  
		Last Modified: Thu, 27 Feb 2020 06:01:53 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d351df4ccaaec3b1572723ff03d33bed4983786ca457885d7827e9a878cb25`  
		Last Modified: Thu, 27 Feb 2020 06:01:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59625d22999eb48a1726733ed377ea1461cf721497c24e928ac50cfd17f900e`  
		Last Modified: Thu, 27 Feb 2020 06:01:53 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d8ffcf5d0207d1f7364881a8490f6b23064cc4b0831c285bcfec42ee88e3e08f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79880211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e1fc1dc9d6aebe664466b6ef59d06027b07653a4026234cf61401ca515be67`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:47:49 GMT
ADD file:745d3236976c8213b805ca6d14f150561816cd2eeec5aa7e1aaea44d9d5675e9 in / 
# Wed, 26 Feb 2020 00:47:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 09:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 09:59:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 10:06:50 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 10:06:50 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 10:06:51 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 10:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 10:10:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 10:10:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 10:10:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 10:10:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 10:10:27 GMT
CMD ["irb"]
# Wed, 26 Feb 2020 17:37:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 26 Feb 2020 17:37:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 26 Feb 2020 17:37:50 GMT
ENV TINI_VERSION=0.18.0
# Wed, 26 Feb 2020 17:40:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 26 Feb 2020 17:40:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 26 Feb 2020 17:41:00 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 26 Feb 2020 17:41:00 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 26 Feb 2020 17:41:01 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 26 Feb 2020 17:41:01 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 26 Feb 2020 17:41:02 GMT
EXPOSE 24224 5140
# Wed, 26 Feb 2020 17:41:03 GMT
USER fluent
# Wed, 26 Feb 2020 17:41:03 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 26 Feb 2020 17:41:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d9f9009f908455fa93c5b3e0d3230df44ea75299b2de375ab35b74193f679076`  
		Last Modified: Wed, 26 Feb 2020 00:59:18 GMT  
		Size: 24.8 MB (24830277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b68ae7942ab8c1f01e481345a18e0f571bf957481b361eb7e3280d62c276f`  
		Last Modified: Wed, 26 Feb 2020 11:00:23 GMT  
		Size: 10.3 MB (10326140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f46e35d9e2656201240a1d6a4f31c7b5cf9c50cb65d450a4a4d437e4e59797`  
		Last Modified: Wed, 26 Feb 2020 11:00:20 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73436533bb2028cba708df8d7be4d1b63835899ee160c845d3a1e5bbfc9937c5`  
		Last Modified: Wed, 26 Feb 2020 11:00:56 GMT  
		Size: 20.7 MB (20712817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab44277f341c947585d955ccb59d218101dad1eb488fa43cc078416cc3ab06c8`  
		Last Modified: Wed, 26 Feb 2020 11:00:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92423bb469928f5175c5ba2a71f9767c9d009420941c20c2c0033b4df8995138`  
		Last Modified: Wed, 26 Feb 2020 17:41:31 GMT  
		Size: 24.0 MB (24007909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f4c74ae1235c52cefde28e16f19faa017cce94437184c72fbb98705fa9ede`  
		Last Modified: Wed, 26 Feb 2020 17:41:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb11a009c6307aab078538eb230b41a6dcd0fd2aa52d2f28c4ce95e75d0becd`  
		Last Modified: Wed, 26 Feb 2020 17:41:23 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ff3b309a01796b1f745a404240ab765e360634b6101e14e5d5d7c2ab790cd9`  
		Last Modified: Wed, 26 Feb 2020 17:41:24 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f5f1556e28d980a5a2e406d3bffde3c8c1040c8db87ec0acf0e3b901aa02b106
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77073121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05d0830b0849288ce0d2234c88b2aea93b75c30e00f75c1981bbf881f84c150`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:52:11 GMT
ADD file:2488038744e2e15217e67dd7f4bec5dcc7e9abe8a1010fe720a5ba7cbe7ab0eb in / 
# Wed, 26 Feb 2020 00:52:13 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 12:35:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 12:35:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 12:54:10 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 12:54:10 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 12:54:11 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 12:57:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 12:57:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 12:57:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 12:57:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 12:57:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 12:57:47 GMT
CMD ["irb"]
# Thu, 27 Feb 2020 00:30:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 27 Feb 2020 00:30:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 27 Feb 2020 00:30:23 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 00:33:45 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 27 Feb 2020 00:33:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 27 Feb 2020 00:33:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 27 Feb 2020 00:33:50 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 27 Feb 2020 00:33:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 27 Feb 2020 00:33:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 27 Feb 2020 00:33:52 GMT
EXPOSE 24224 5140
# Thu, 27 Feb 2020 00:33:53 GMT
USER fluent
# Thu, 27 Feb 2020 00:33:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 27 Feb 2020 00:33:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fff3167bf8c79dc08baf67eb607823aadcbee2033f9620cc502e2c49423f605b`  
		Last Modified: Wed, 26 Feb 2020 01:07:32 GMT  
		Size: 22.7 MB (22699783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cd6276ff60a8c8ee1a46ac7bbb759c6a16237a9d2769b871210f54ab843016`  
		Last Modified: Wed, 26 Feb 2020 13:46:26 GMT  
		Size: 9.8 MB (9847377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89da819a89bd9b8de40634d7690032f0c126bf451b9dd968cb140aafc8f039a`  
		Last Modified: Wed, 26 Feb 2020 13:46:22 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca19d76cacd46278fb7886c0be2ff750c7effd1ff3c86069593a4ccb4f7336a5`  
		Last Modified: Wed, 26 Feb 2020 13:47:09 GMT  
		Size: 20.6 MB (20620219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1b35e09252fb4694ab4c9b7fa917b14132fe3f69408d6416fb6d71808b15b1`  
		Last Modified: Wed, 26 Feb 2020 13:47:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67f3643582f030d879e67c0d80327136d030b189120a0f3c81c06b64b27264`  
		Last Modified: Thu, 27 Feb 2020 00:34:20 GMT  
		Size: 23.9 MB (23902681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f033a21b2f3eedd6c1766673d0395a6f703b41a61ae41028f70396c1afb62f4`  
		Last Modified: Thu, 27 Feb 2020 00:34:14 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f7f6d05cdbcdb1ac7fe2e40408e05452d6e3c1dd59dc8a40c8d2bb0dc2ef83`  
		Last Modified: Thu, 27 Feb 2020 00:34:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83e905d105f0d639a1f9db4e64eb699188cd761c6f173d9648c17a6b0844b65`  
		Last Modified: Thu, 27 Feb 2020 00:34:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a8e34ddaaeb09a1c6858f4cdc473b39ec1225a53019dc372818bb0ccb39f4ad9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83240854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2514a660d7ac2b5be03865de7d47e83b1cec327c2624e4b2e41d5ba8595fa2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:51 GMT
ADD file:a93818b0ffcb2823807811dffd78092a3e3f4981aabf48c3cb75f2fa319ac055 in / 
# Wed, 26 Feb 2020 00:46:55 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 06:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:57:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 07:05:33 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 07:05:34 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 07:05:34 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 07:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 07:09:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 07:09:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 07:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 07:09:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 07:09:30 GMT
CMD ["irb"]
# Thu, 27 Feb 2020 00:32:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 27 Feb 2020 00:32:52 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 27 Feb 2020 00:32:54 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 00:35:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 27 Feb 2020 00:35:54 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 27 Feb 2020 00:35:55 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 27 Feb 2020 00:35:55 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 27 Feb 2020 00:35:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 27 Feb 2020 00:35:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 27 Feb 2020 00:35:57 GMT
EXPOSE 24224 5140
# Thu, 27 Feb 2020 00:35:58 GMT
USER fluent
# Thu, 27 Feb 2020 00:35:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 27 Feb 2020 00:35:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f338bc35613f66cfaad272234de7b77a91d6c5422855bf6239f2b0ff9d73f0a4`  
		Last Modified: Wed, 26 Feb 2020 00:56:15 GMT  
		Size: 25.9 MB (25851563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fd24749620c003b67602370b1409f39193b9cd47499ab1be58e4ccb6cea596`  
		Last Modified: Wed, 26 Feb 2020 07:59:53 GMT  
		Size: 11.2 MB (11244746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea1d8071f282def341d45dc200fb8e235764c1d52229704b354c5ab9d9f8faa`  
		Last Modified: Wed, 26 Feb 2020 07:59:49 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279bca24c64fd50cb9f883efb8c369cb25552ccbe8cc927aa41660dba218159a`  
		Last Modified: Wed, 26 Feb 2020 08:00:25 GMT  
		Size: 21.3 MB (21281866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcbfd9a852ba7f9897f7eeec9c26dc38edf3b0b2f5861862096c51f4b3a1aae`  
		Last Modified: Wed, 26 Feb 2020 08:00:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1b5fcac7218fc92517d967c9aa0fdb70e251e751f18697d1875ca3aa49d969`  
		Last Modified: Thu, 27 Feb 2020 00:36:20 GMT  
		Size: 24.9 MB (24859606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eb73fa7b18964f3e127f449eb5e098784acef724cd835fa2171b1e72500204`  
		Last Modified: Thu, 27 Feb 2020 00:36:14 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ee445390c671a4c6db9c4a5efbcb8eac7436bf90a0b8271c00dbb7c81c55f0`  
		Last Modified: Thu, 27 Feb 2020 00:36:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27dacc839ad4cb9b672e441de4e87e4fd42a07680d52ec34e2b5c2945fae253`  
		Last Modified: Thu, 27 Feb 2020 00:36:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:ed23dbeec970b7e04865dfc544a55e99ede1213120cb55a303daaddd71209346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89897876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9ff0aaf2c0640ff638802a3fd847849d165e86a4bc48fca6cde8707b533634`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:32:17 GMT
ADD file:08977fa54555a1ed2ae44a3aec04df157092a6c1c1b70ce0407cc2dc2f8bcd76 in / 
# Wed, 26 Feb 2020 00:32:17 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 15:57:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 15:57:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 16:06:08 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 16:06:08 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 16:06:08 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 16:10:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 16:10:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 16:10:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 16:10:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 16:10:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 16:10:28 GMT
CMD ["irb"]
# Wed, 26 Feb 2020 20:50:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 26 Feb 2020 20:50:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 26 Feb 2020 20:50:20 GMT
ENV TINI_VERSION=0.18.0
# Wed, 26 Feb 2020 20:52:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 26 Feb 2020 20:52:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 26 Feb 2020 20:52:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 26 Feb 2020 20:52:40 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 26 Feb 2020 20:52:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 26 Feb 2020 20:52:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 26 Feb 2020 20:52:41 GMT
EXPOSE 24224 5140
# Wed, 26 Feb 2020 20:52:42 GMT
USER fluent
# Wed, 26 Feb 2020 20:52:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 26 Feb 2020 20:52:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1de10f1ae2a5bfd5f34f19421ebd282580e443321e4947cdf5f943875782b018`  
		Last Modified: Wed, 26 Feb 2020 00:38:34 GMT  
		Size: 27.7 MB (27747667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7a314f740e622b84f3adcef81a7af1abf0036fdd480c77ea8fe0f78f23ce4d`  
		Last Modified: Wed, 26 Feb 2020 17:00:00 GMT  
		Size: 17.2 MB (17206182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4cd4384f7124591475ff1be52c6557bbdfdecaad0f10fe92d3424926a9959`  
		Last Modified: Wed, 26 Feb 2020 16:59:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3354854439a188065dd411e4fb1fcceba83a9997fc223bf2b8c880ef7e37f5`  
		Last Modified: Wed, 26 Feb 2020 17:00:40 GMT  
		Size: 20.9 MB (20885474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac27c0cf01a9587084ace21a1bb88189158e7222082747c53df1e2862594a673`  
		Last Modified: Wed, 26 Feb 2020 17:00:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83776eab4d0571ae6316f079bb8864a6a6d1cd1ad17520dc5878f0c0b01ad8a6`  
		Last Modified: Wed, 26 Feb 2020 20:53:05 GMT  
		Size: 24.1 MB (24055554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514b1ea9ad0537cc0622ab6d320f26bfbcac5a5ebf5dfa74de629293fba66b1a`  
		Last Modified: Wed, 26 Feb 2020 20:52:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f161e478c33fb3013ecf3a3dd76a05fb25f513d726e8ce021c24db793a0d082`  
		Last Modified: Wed, 26 Feb 2020 20:52:57 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d252457f7456ce6d17d184982feab6347f7f6eb5172f82171749db92902f63`  
		Last Modified: Wed, 26 Feb 2020 20:52:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:6c9e19fdae3e1c3ce4ca8087f5f3e763f3ac68eba82ae0f635dc3bba40b0949f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90601981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688edfdd8ad28b75385ebb0c9eaf3566009aa905b8968478fc0110f835afa140`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:54:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:19:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:19:17 GMT
ENV TINI_VERSION=0.18.0
# Fri, 07 Feb 2020 23:24:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:24:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:24:24 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:24:25 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:24:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:24:33 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 07 Feb 2020 23:24:37 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:24:40 GMT
USER fluent
# Fri, 07 Feb 2020 23:24:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:24:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034fc322bbcee376fc669e1a6f9213c827105ba76502ae17583fa60dd6995a77`  
		Last Modified: Fri, 07 Feb 2020 23:25:32 GMT  
		Size: 25.4 MB (25423682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3190342e655032e2f51ea17df43b421cc94569ca8d13af81483ce38659cc5ed4`  
		Last Modified: Fri, 07 Feb 2020 23:25:21 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7103b0907ea021b68df6a329eacbd4a48a2467632189131360d85f8b824409`  
		Last Modified: Fri, 07 Feb 2020 23:25:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e064bb4234cc63582e896369f49c7e695109419d0cd8a07e3ffe496c96f3ee2`  
		Last Modified: Fri, 07 Feb 2020 23:25:20 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:2b7a75af15cad3208d7fe39246ab3ab1ba3850e54163e7d4ffd45b99e47f9a0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83109773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dfc13440e4d83956b9c9828813a8051ce6b80cafee0925af5b310a28c3ba32`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:42:48 GMT
ADD file:3396670211650b5d7c6e1f0ace1a72f1d1587f275baa682dfee6c7bf2603fb34 in / 
# Wed, 26 Feb 2020 00:42:50 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 08:03:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 08:03:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 08:17:58 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 08:17:58 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 08:17:59 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 08:20:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 08:20:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 08:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 08:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 08:20:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 08:20:08 GMT
CMD ["irb"]
# Wed, 26 Feb 2020 15:24:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 26 Feb 2020 15:24:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 26 Feb 2020 15:24:50 GMT
ENV TINI_VERSION=0.18.0
# Wed, 26 Feb 2020 15:26:09 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 26 Feb 2020 15:26:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 26 Feb 2020 15:26:11 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 26 Feb 2020 15:26:11 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 26 Feb 2020 15:26:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 26 Feb 2020 15:26:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 26 Feb 2020 15:26:12 GMT
EXPOSE 24224 5140
# Wed, 26 Feb 2020 15:26:12 GMT
USER fluent
# Wed, 26 Feb 2020 15:26:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 26 Feb 2020 15:26:12 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e25900e2a7f96a6326b79ec6dfdce1ac5461c7a961fb3752ec1770cd82b8d03c`  
		Last Modified: Wed, 26 Feb 2020 00:47:43 GMT  
		Size: 25.7 MB (25705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe74e233a5056d4310cb21e747dd6c9f8fc63222afaf3a08c8b0385a2d0d1f9`  
		Last Modified: Wed, 26 Feb 2020 08:55:34 GMT  
		Size: 10.8 MB (10796148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1f38dc1e077657ee8aed122d95efee83f855295ede05f14c4ad20450bf6352`  
		Last Modified: Wed, 26 Feb 2020 08:55:37 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79adc550ed79b127db0ed952dd2fc7dc368bc6f0a6d7e0bbd5937e233688a8`  
		Last Modified: Wed, 26 Feb 2020 08:56:11 GMT  
		Size: 21.6 MB (21592837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4de0bfc105086e376c31bbb1d943255f52ea32c369c643076fceb3bf731a4b`  
		Last Modified: Wed, 26 Feb 2020 08:56:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc290f827dfd2ff0afbda513ad02528d2d55925e64b2568482ac2b0c9dd537c`  
		Last Modified: Wed, 26 Feb 2020 15:26:28 GMT  
		Size: 25.0 MB (25011786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0b11828e65133e4b927ec96fb61056b2fba9dc8f879da8d22ab914249e32fa`  
		Last Modified: Wed, 26 Feb 2020 15:26:25 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc483d6a31cdefb927a4900eb2a751a258338982eb851960fc098ecc0760abbb`  
		Last Modified: Wed, 26 Feb 2020 15:26:30 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20db265bf8b40df705c94fcbd7c22b446ae6cea501416bebe2a3858b60010c99`  
		Last Modified: Wed, 26 Feb 2020 15:26:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.9-debian-1`

```console
$ docker pull fluentd@sha256:8a9cbfe2f92f8c91795b526c2867abd97ef220b1d2c5a800a161301f532330c2
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
$ docker pull fluentd@sha256:7f0c43a885a718075a6409f9c8c12b699b5dd15fdc52849dfbb6f143160a034d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85940245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab21435ee61df1ce5cf5686285fa444a38683a5c124cbbae16d2397777685eb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:39 GMT
ADD file:e5a364615e0f6961626089c7d658adbf8c8d95b3ae95a390a8bb33875317d434 in / 
# Wed, 26 Feb 2020 00:37:39 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:34:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:34:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 18:45:10 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 18:45:10 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 18:45:10 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 18:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 18:48:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 18:48:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 18:48:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 18:48:44 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 18:48:45 GMT
CMD ["irb"]
# Thu, 27 Feb 2020 06:00:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 27 Feb 2020 06:00:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 27 Feb 2020 06:00:06 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 06:01:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 27 Feb 2020 06:01:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 27 Feb 2020 06:01:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 27 Feb 2020 06:01:35 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 27 Feb 2020 06:01:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 27 Feb 2020 06:01:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 27 Feb 2020 06:01:36 GMT
EXPOSE 24224 5140
# Thu, 27 Feb 2020 06:01:36 GMT
USER fluent
# Thu, 27 Feb 2020 06:01:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 27 Feb 2020 06:01:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:68ced04f60ab5c7a5f1d0b0b4e7572c5a4c8cce44866513d30d9df1a15277d6b`  
		Last Modified: Wed, 26 Feb 2020 00:44:23 GMT  
		Size: 27.1 MB (27091819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55a61b57e3f6be04fbb54f4f49599cf38837e4be329c9010a4ef6977bdbd99a`  
		Last Modified: Wed, 26 Feb 2020 19:35:59 GMT  
		Size: 12.5 MB (12539730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56979ca8f121c1cc4b85f2c0bff0eb766aa71ada5964ad7a1ce801ae915f5d`  
		Last Modified: Wed, 26 Feb 2020 19:35:56 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a486fb9a30dac6e55b779c44e1dec51d7f68bdbd30b2251d8a5d0f75e979b372`  
		Last Modified: Wed, 26 Feb 2020 19:36:20 GMT  
		Size: 21.4 MB (21445518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4541c61250ed97cb558d4a38ac75e68ca5a45db2445eadbf6884015ed6bc75`  
		Last Modified: Wed, 26 Feb 2020 19:36:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a686cf8fac553c2d27ed0eff3d6358ef0428954c0ca0beec0d37d5ddc1a62d4`  
		Last Modified: Thu, 27 Feb 2020 06:01:57 GMT  
		Size: 24.9 MB (24860166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5fe5aca975bc22d1c80ed8b30d1b15ac6959bb184f98b0ec47b30cfa304968`  
		Last Modified: Thu, 27 Feb 2020 06:01:53 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d351df4ccaaec3b1572723ff03d33bed4983786ca457885d7827e9a878cb25`  
		Last Modified: Thu, 27 Feb 2020 06:01:53 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59625d22999eb48a1726733ed377ea1461cf721497c24e928ac50cfd17f900e`  
		Last Modified: Thu, 27 Feb 2020 06:01:53 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d8ffcf5d0207d1f7364881a8490f6b23064cc4b0831c285bcfec42ee88e3e08f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79880211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e1fc1dc9d6aebe664466b6ef59d06027b07653a4026234cf61401ca515be67`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:47:49 GMT
ADD file:745d3236976c8213b805ca6d14f150561816cd2eeec5aa7e1aaea44d9d5675e9 in / 
# Wed, 26 Feb 2020 00:47:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 09:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 09:59:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 10:06:50 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 10:06:50 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 10:06:51 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 10:10:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 10:10:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 10:10:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 10:10:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 10:10:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 10:10:27 GMT
CMD ["irb"]
# Wed, 26 Feb 2020 17:37:47 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 26 Feb 2020 17:37:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 26 Feb 2020 17:37:50 GMT
ENV TINI_VERSION=0.18.0
# Wed, 26 Feb 2020 17:40:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 26 Feb 2020 17:40:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 26 Feb 2020 17:41:00 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 26 Feb 2020 17:41:00 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 26 Feb 2020 17:41:01 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 26 Feb 2020 17:41:01 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 26 Feb 2020 17:41:02 GMT
EXPOSE 24224 5140
# Wed, 26 Feb 2020 17:41:03 GMT
USER fluent
# Wed, 26 Feb 2020 17:41:03 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 26 Feb 2020 17:41:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d9f9009f908455fa93c5b3e0d3230df44ea75299b2de375ab35b74193f679076`  
		Last Modified: Wed, 26 Feb 2020 00:59:18 GMT  
		Size: 24.8 MB (24830277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b68ae7942ab8c1f01e481345a18e0f571bf957481b361eb7e3280d62c276f`  
		Last Modified: Wed, 26 Feb 2020 11:00:23 GMT  
		Size: 10.3 MB (10326140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f46e35d9e2656201240a1d6a4f31c7b5cf9c50cb65d450a4a4d437e4e59797`  
		Last Modified: Wed, 26 Feb 2020 11:00:20 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73436533bb2028cba708df8d7be4d1b63835899ee160c845d3a1e5bbfc9937c5`  
		Last Modified: Wed, 26 Feb 2020 11:00:56 GMT  
		Size: 20.7 MB (20712817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab44277f341c947585d955ccb59d218101dad1eb488fa43cc078416cc3ab06c8`  
		Last Modified: Wed, 26 Feb 2020 11:00:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92423bb469928f5175c5ba2a71f9767c9d009420941c20c2c0033b4df8995138`  
		Last Modified: Wed, 26 Feb 2020 17:41:31 GMT  
		Size: 24.0 MB (24007909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16f4c74ae1235c52cefde28e16f19faa017cce94437184c72fbb98705fa9ede`  
		Last Modified: Wed, 26 Feb 2020 17:41:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb11a009c6307aab078538eb230b41a6dcd0fd2aa52d2f28c4ce95e75d0becd`  
		Last Modified: Wed, 26 Feb 2020 17:41:23 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ff3b309a01796b1f745a404240ab765e360634b6101e14e5d5d7c2ab790cd9`  
		Last Modified: Wed, 26 Feb 2020 17:41:24 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f5f1556e28d980a5a2e406d3bffde3c8c1040c8db87ec0acf0e3b901aa02b106
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77073121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05d0830b0849288ce0d2234c88b2aea93b75c30e00f75c1981bbf881f84c150`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:52:11 GMT
ADD file:2488038744e2e15217e67dd7f4bec5dcc7e9abe8a1010fe720a5ba7cbe7ab0eb in / 
# Wed, 26 Feb 2020 00:52:13 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 12:35:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 12:35:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 12:54:10 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 12:54:10 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 12:54:11 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 12:57:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 12:57:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 12:57:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 12:57:43 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 12:57:46 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 12:57:47 GMT
CMD ["irb"]
# Thu, 27 Feb 2020 00:30:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 27 Feb 2020 00:30:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 27 Feb 2020 00:30:23 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 00:33:45 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 27 Feb 2020 00:33:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 27 Feb 2020 00:33:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 27 Feb 2020 00:33:50 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 27 Feb 2020 00:33:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 27 Feb 2020 00:33:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 27 Feb 2020 00:33:52 GMT
EXPOSE 24224 5140
# Thu, 27 Feb 2020 00:33:53 GMT
USER fluent
# Thu, 27 Feb 2020 00:33:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 27 Feb 2020 00:33:54 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fff3167bf8c79dc08baf67eb607823aadcbee2033f9620cc502e2c49423f605b`  
		Last Modified: Wed, 26 Feb 2020 01:07:32 GMT  
		Size: 22.7 MB (22699783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cd6276ff60a8c8ee1a46ac7bbb759c6a16237a9d2769b871210f54ab843016`  
		Last Modified: Wed, 26 Feb 2020 13:46:26 GMT  
		Size: 9.8 MB (9847377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89da819a89bd9b8de40634d7690032f0c126bf451b9dd968cb140aafc8f039a`  
		Last Modified: Wed, 26 Feb 2020 13:46:22 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca19d76cacd46278fb7886c0be2ff750c7effd1ff3c86069593a4ccb4f7336a5`  
		Last Modified: Wed, 26 Feb 2020 13:47:09 GMT  
		Size: 20.6 MB (20620219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1b35e09252fb4694ab4c9b7fa917b14132fe3f69408d6416fb6d71808b15b1`  
		Last Modified: Wed, 26 Feb 2020 13:47:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67f3643582f030d879e67c0d80327136d030b189120a0f3c81c06b64b27264`  
		Last Modified: Thu, 27 Feb 2020 00:34:20 GMT  
		Size: 23.9 MB (23902681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f033a21b2f3eedd6c1766673d0395a6f703b41a61ae41028f70396c1afb62f4`  
		Last Modified: Thu, 27 Feb 2020 00:34:14 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f7f6d05cdbcdb1ac7fe2e40408e05452d6e3c1dd59dc8a40c8d2bb0dc2ef83`  
		Last Modified: Thu, 27 Feb 2020 00:34:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83e905d105f0d639a1f9db4e64eb699188cd761c6f173d9648c17a6b0844b65`  
		Last Modified: Thu, 27 Feb 2020 00:34:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a8e34ddaaeb09a1c6858f4cdc473b39ec1225a53019dc372818bb0ccb39f4ad9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83240854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2514a660d7ac2b5be03865de7d47e83b1cec327c2624e4b2e41d5ba8595fa2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:51 GMT
ADD file:a93818b0ffcb2823807811dffd78092a3e3f4981aabf48c3cb75f2fa319ac055 in / 
# Wed, 26 Feb 2020 00:46:55 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 06:57:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:57:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 07:05:33 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 07:05:34 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 07:05:34 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 07:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 07:09:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 07:09:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 07:09:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 07:09:29 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 07:09:30 GMT
CMD ["irb"]
# Thu, 27 Feb 2020 00:32:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 27 Feb 2020 00:32:52 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Thu, 27 Feb 2020 00:32:54 GMT
ENV TINI_VERSION=0.18.0
# Thu, 27 Feb 2020 00:35:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Thu, 27 Feb 2020 00:35:54 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 27 Feb 2020 00:35:55 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 27 Feb 2020 00:35:55 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Thu, 27 Feb 2020 00:35:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 27 Feb 2020 00:35:57 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 27 Feb 2020 00:35:57 GMT
EXPOSE 24224 5140
# Thu, 27 Feb 2020 00:35:58 GMT
USER fluent
# Thu, 27 Feb 2020 00:35:59 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 27 Feb 2020 00:35:59 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f338bc35613f66cfaad272234de7b77a91d6c5422855bf6239f2b0ff9d73f0a4`  
		Last Modified: Wed, 26 Feb 2020 00:56:15 GMT  
		Size: 25.9 MB (25851563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fd24749620c003b67602370b1409f39193b9cd47499ab1be58e4ccb6cea596`  
		Last Modified: Wed, 26 Feb 2020 07:59:53 GMT  
		Size: 11.2 MB (11244746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea1d8071f282def341d45dc200fb8e235764c1d52229704b354c5ab9d9f8faa`  
		Last Modified: Wed, 26 Feb 2020 07:59:49 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279bca24c64fd50cb9f883efb8c369cb25552ccbe8cc927aa41660dba218159a`  
		Last Modified: Wed, 26 Feb 2020 08:00:25 GMT  
		Size: 21.3 MB (21281866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcbfd9a852ba7f9897f7eeec9c26dc38edf3b0b2f5861862096c51f4b3a1aae`  
		Last Modified: Wed, 26 Feb 2020 08:00:21 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1b5fcac7218fc92517d967c9aa0fdb70e251e751f18697d1875ca3aa49d969`  
		Last Modified: Thu, 27 Feb 2020 00:36:20 GMT  
		Size: 24.9 MB (24859606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eb73fa7b18964f3e127f449eb5e098784acef724cd835fa2171b1e72500204`  
		Last Modified: Thu, 27 Feb 2020 00:36:14 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ee445390c671a4c6db9c4a5efbcb8eac7436bf90a0b8271c00dbb7c81c55f0`  
		Last Modified: Thu, 27 Feb 2020 00:36:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27dacc839ad4cb9b672e441de4e87e4fd42a07680d52ec34e2b5c2945fae253`  
		Last Modified: Thu, 27 Feb 2020 00:36:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:ed23dbeec970b7e04865dfc544a55e99ede1213120cb55a303daaddd71209346
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89897876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9ff0aaf2c0640ff638802a3fd847849d165e86a4bc48fca6cde8707b533634`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:32:17 GMT
ADD file:08977fa54555a1ed2ae44a3aec04df157092a6c1c1b70ce0407cc2dc2f8bcd76 in / 
# Wed, 26 Feb 2020 00:32:17 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 15:57:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 15:57:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 16:06:08 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 16:06:08 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 16:06:08 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 16:10:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 16:10:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 16:10:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 16:10:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 16:10:28 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 16:10:28 GMT
CMD ["irb"]
# Wed, 26 Feb 2020 20:50:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 26 Feb 2020 20:50:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 26 Feb 2020 20:50:20 GMT
ENV TINI_VERSION=0.18.0
# Wed, 26 Feb 2020 20:52:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 26 Feb 2020 20:52:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 26 Feb 2020 20:52:40 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 26 Feb 2020 20:52:40 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 26 Feb 2020 20:52:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 26 Feb 2020 20:52:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 26 Feb 2020 20:52:41 GMT
EXPOSE 24224 5140
# Wed, 26 Feb 2020 20:52:42 GMT
USER fluent
# Wed, 26 Feb 2020 20:52:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 26 Feb 2020 20:52:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1de10f1ae2a5bfd5f34f19421ebd282580e443321e4947cdf5f943875782b018`  
		Last Modified: Wed, 26 Feb 2020 00:38:34 GMT  
		Size: 27.7 MB (27747667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7a314f740e622b84f3adcef81a7af1abf0036fdd480c77ea8fe0f78f23ce4d`  
		Last Modified: Wed, 26 Feb 2020 17:00:00 GMT  
		Size: 17.2 MB (17206182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a4cd4384f7124591475ff1be52c6557bbdfdecaad0f10fe92d3424926a9959`  
		Last Modified: Wed, 26 Feb 2020 16:59:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3354854439a188065dd411e4fb1fcceba83a9997fc223bf2b8c880ef7e37f5`  
		Last Modified: Wed, 26 Feb 2020 17:00:40 GMT  
		Size: 20.9 MB (20885474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac27c0cf01a9587084ace21a1bb88189158e7222082747c53df1e2862594a673`  
		Last Modified: Wed, 26 Feb 2020 17:00:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83776eab4d0571ae6316f079bb8864a6a6d1cd1ad17520dc5878f0c0b01ad8a6`  
		Last Modified: Wed, 26 Feb 2020 20:53:05 GMT  
		Size: 24.1 MB (24055554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514b1ea9ad0537cc0622ab6d320f26bfbcac5a5ebf5dfa74de629293fba66b1a`  
		Last Modified: Wed, 26 Feb 2020 20:52:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f161e478c33fb3013ecf3a3dd76a05fb25f513d726e8ce021c24db793a0d082`  
		Last Modified: Wed, 26 Feb 2020 20:52:57 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d252457f7456ce6d17d184982feab6347f7f6eb5172f82171749db92902f63`  
		Last Modified: Wed, 26 Feb 2020 20:52:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:6c9e19fdae3e1c3ce4ca8087f5f3e763f3ac68eba82ae0f635dc3bba40b0949f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90601981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688edfdd8ad28b75385ebb0c9eaf3566009aa905b8968478fc0110f835afa140`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:56:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Sun, 02 Feb 2020 07:10:22 GMT
ENV RUBY_MAJOR=2.6
# Sun, 02 Feb 2020 07:10:25 GMT
ENV RUBY_VERSION=2.6.5
# Sun, 02 Feb 2020 07:10:27 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Sun, 02 Feb 2020 07:18:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Sun, 02 Feb 2020 07:18:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 02 Feb 2020 07:18:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 07:18:32 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Sun, 02 Feb 2020 07:18:37 GMT
CMD ["irb"]
# Sun, 02 Feb 2020 16:54:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 07 Feb 2020 23:19:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Fri, 07 Feb 2020 23:19:17 GMT
ENV TINI_VERSION=0.18.0
# Fri, 07 Feb 2020 23:24:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Fri, 07 Feb 2020 23:24:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 07 Feb 2020 23:24:24 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 07 Feb 2020 23:24:25 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Fri, 07 Feb 2020 23:24:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 07 Feb 2020 23:24:33 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 07 Feb 2020 23:24:37 GMT
EXPOSE 24224 5140
# Fri, 07 Feb 2020 23:24:40 GMT
USER fluent
# Fri, 07 Feb 2020 23:24:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 07 Feb 2020 23:24:47 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d44bc1840f426f48fc6d4cc23113f86c02e7f46ef4c400ce5b4c76010c72a2`  
		Last Modified: Sun, 02 Feb 2020 08:19:33 GMT  
		Size: 12.7 MB (12688850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e418c294c298ad8987cb27fc2adff7ce43dee0e55af3c86e59af9271e4c490`  
		Last Modified: Sun, 02 Feb 2020 08:19:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed4fdb4090425730dd3e443c0fd27af2b2cff3415260f22a0056d8ff639b99`  
		Last Modified: Sun, 02 Feb 2020 08:20:20 GMT  
		Size: 22.0 MB (21968679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3472d9aadeeb03ff16dda03cf908dc2438dfbe262d09c2f3fe38ba8a9a8a9a8`  
		Last Modified: Sun, 02 Feb 2020 08:20:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034fc322bbcee376fc669e1a6f9213c827105ba76502ae17583fa60dd6995a77`  
		Last Modified: Fri, 07 Feb 2020 23:25:32 GMT  
		Size: 25.4 MB (25423682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3190342e655032e2f51ea17df43b421cc94569ca8d13af81483ce38659cc5ed4`  
		Last Modified: Fri, 07 Feb 2020 23:25:21 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7103b0907ea021b68df6a329eacbd4a48a2467632189131360d85f8b824409`  
		Last Modified: Fri, 07 Feb 2020 23:25:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e064bb4234cc63582e896369f49c7e695109419d0cd8a07e3ffe496c96f3ee2`  
		Last Modified: Fri, 07 Feb 2020 23:25:20 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.9-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:2b7a75af15cad3208d7fe39246ab3ab1ba3850e54163e7d4ffd45b99e47f9a0c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83109773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dfc13440e4d83956b9c9828813a8051ce6b80cafee0925af5b310a28c3ba32`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 26 Feb 2020 00:42:48 GMT
ADD file:3396670211650b5d7c6e1f0ace1a72f1d1587f275baa682dfee6c7bf2603fb34 in / 
# Wed, 26 Feb 2020 00:42:50 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 08:03:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 08:03:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 26 Feb 2020 08:17:58 GMT
ENV RUBY_MAJOR=2.6
# Wed, 26 Feb 2020 08:17:58 GMT
ENV RUBY_VERSION=2.6.5
# Wed, 26 Feb 2020 08:17:59 GMT
ENV RUBY_DOWNLOAD_SHA256=d5d6da717fd48524596f9b78ac5a2eeb9691753da5c06923a6c31190abe01a62
# Wed, 26 Feb 2020 08:20:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	! dpkg -l | grep -i ruby; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 26 Feb 2020 08:20:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 26 Feb 2020 08:20:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 26 Feb 2020 08:20:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 08:20:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 26 Feb 2020 08:20:08 GMT
CMD ["irb"]
# Wed, 26 Feb 2020 15:24:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 26 Feb 2020 15:24:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.9.1
# Wed, 26 Feb 2020 15:24:50 GMT
ENV TINI_VERSION=0.18.0
# Wed, 26 Feb 2020 15:26:09 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.8.1  && gem install json -v 2.3.0  && gem install async-http -v 0.50.0  && gem install ext_monitor -v 0.1.2  && gem install fluentd -v 1.9.1  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-4.5.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/4.5.0/jemalloc-4.5.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-4.5.0.tar.bz2 && cd jemalloc-4.5.0/  && ./configure && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem
# Wed, 26 Feb 2020 15:26:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 26 Feb 2020 15:26:11 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 26 Feb 2020 15:26:11 GMT
COPY file:f70a6a04a7c32c744ebb989e7d706ca5f78829c1489be8d165d4b1b682c9eaf8 in /bin/ 
# Wed, 26 Feb 2020 15:26:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 26 Feb 2020 15:26:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 26 Feb 2020 15:26:12 GMT
EXPOSE 24224 5140
# Wed, 26 Feb 2020 15:26:12 GMT
USER fluent
# Wed, 26 Feb 2020 15:26:12 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 26 Feb 2020 15:26:12 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e25900e2a7f96a6326b79ec6dfdce1ac5461c7a961fb3752ec1770cd82b8d03c`  
		Last Modified: Wed, 26 Feb 2020 00:47:43 GMT  
		Size: 25.7 MB (25705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe74e233a5056d4310cb21e747dd6c9f8fc63222afaf3a08c8b0385a2d0d1f9`  
		Last Modified: Wed, 26 Feb 2020 08:55:34 GMT  
		Size: 10.8 MB (10796148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1f38dc1e077657ee8aed122d95efee83f855295ede05f14c4ad20450bf6352`  
		Last Modified: Wed, 26 Feb 2020 08:55:37 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f79adc550ed79b127db0ed952dd2fc7dc368bc6f0a6d7e0bbd5937e233688a8`  
		Last Modified: Wed, 26 Feb 2020 08:56:11 GMT  
		Size: 21.6 MB (21592837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4de0bfc105086e376c31bbb1d943255f52ea32c369c643076fceb3bf731a4b`  
		Last Modified: Wed, 26 Feb 2020 08:56:09 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc290f827dfd2ff0afbda513ad02528d2d55925e64b2568482ac2b0c9dd537c`  
		Last Modified: Wed, 26 Feb 2020 15:26:28 GMT  
		Size: 25.0 MB (25011786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0b11828e65133e4b927ec96fb61056b2fba9dc8f879da8d22ab914249e32fa`  
		Last Modified: Wed, 26 Feb 2020 15:26:25 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc483d6a31cdefb927a4900eb2a751a258338982eb851960fc098ecc0760abbb`  
		Last Modified: Wed, 26 Feb 2020 15:26:30 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20db265bf8b40df705c94fcbd7c22b446ae6cea501416bebe2a3858b60010c99`  
		Last Modified: Wed, 26 Feb 2020 15:26:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
