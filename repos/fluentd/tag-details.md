<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.0-1.0`](#fluentdv1160-10)
-	[`fluentd:v1.16.0-debian-1.0`](#fluentdv1160-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:fa22cbe77cba960e8311cdd956a503708127e9e9b3530a89e708c26f12dea812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:d07aaa6eba6a96328e2b3a0a0ccb586e556e629f1937141c7f1bd8689798cd30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25138920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d619c23c9ae269bd4d905563b3b29e8cf52f3b43a98e608ae7f3bc9f3813a07d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:33:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 22:33:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 22:34:23 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 22:34:23 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 22:34:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 22:34:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 22:34:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 22:34:24 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 22:34:24 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 22:34:24 GMT
USER fluent
# Wed, 14 Jun 2023 22:34:24 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 22:34:24 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e89884591749689529cd5fa296197dbf2d081b89aa1acf0d521f4c2c6f96bf`  
		Last Modified: Wed, 14 Jun 2023 22:34:37 GMT  
		Size: 21.8 MB (21761995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390a858b50010d973d4e1a5f6da84ba514b82536de40dc734fc35889c5579cca`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d69a60bc67d80beffeb819bcf5409aa6ac1cece761ac175179bcbd081de713`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389b15490d254354e083d9cecd8372dd8a7d24f42f48553b5be44087f846d3cb`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:4c7a522f2f52fded55c7e7eb1cbfbf95071cb89602efd1c16d10173e1052bc19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23818795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9449002b91a5e83fa600b072a1849a3bde33395ab9912736df9ebcf0af9ca07a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:39:12 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 20:39:12 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 20:40:14 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 20:40:14 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 20:40:14 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 20:40:15 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 20:40:15 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 20:40:15 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 20:40:15 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 20:40:15 GMT
USER fluent
# Wed, 14 Jun 2023 20:40:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 20:40:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff90db882f9f0c92f1e98e1b0070fce952033d478a6d6f2139bc6b8deccf4c1`  
		Last Modified: Wed, 14 Jun 2023 20:40:32 GMT  
		Size: 20.7 MB (20705668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409eb899470f9c46b8b52fef13f7747862956ea44d1131402ecdf43a4e62cd4e`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8c355cf22653f5ecf08a38e9747568282212437249dbde1843db76413ac703`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d173e8e240a98c6b2fead4204509ef9ee0ef181fa18818047b1a21744741ef6`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5504f34bf0fdd8c584dde9ece653aef92fab0ec0488b02d09c0c60773873fec0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24615958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625b9c7556aca650f5c149011e1045a1f41a52c022bf6c00d120a443212a2135`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:16:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 23:16:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 23:17:17 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 23:17:18 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 23:17:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 23:17:18 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 23:17:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 23:17:18 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 23:17:18 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 23:17:18 GMT
USER fluent
# Wed, 14 Jun 2023 23:17:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 23:17:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c596c0811598d44ad0388635c2457814da7ec0aeeaa500f5a227ea1ef522859`  
		Last Modified: Wed, 14 Jun 2023 23:17:36 GMT  
		Size: 21.4 MB (21352606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdb87eceb2348af0bce9ef18e4af5f4138cce349e7ddfa9e358e589f1a61928`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8277de9dddc2b555e88ca9500be77262f4bfd85ec1150f4f0bbd390d5d0a86`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2236a61df5e8c4f1cb997555c37c1bec0623a75612f1541cbac90f9f00ffe7b6`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:70073fa5febf90614d06e9ff0993cebadb1d5e3e997a08eb2a3d59133a4f8290
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24413017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98833d32fe9d59d6ae41f918d717cabd71fab1a49b6d830d13eea6a2cace22b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:04:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 03:04:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 03:05:53 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 03:05:54 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 03:05:54 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 03:05:54 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 03:05:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 03:05:55 GMT
ENV LD_PRELOAD=
# Thu, 15 Jun 2023 03:05:55 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 03:05:55 GMT
USER fluent
# Thu, 15 Jun 2023 03:05:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 03:05:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04560289ee3119fe99bb33739daabb776b0eaf4089ddac2f7a1be9070a9a83f1`  
		Last Modified: Thu, 15 Jun 2023 03:06:13 GMT  
		Size: 21.0 MB (20998130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda7a209cb4c0bbe12aa1ec14332a039e01a4cc4312ffafbf410faae5128fc75`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ce2515314e17a9c15c6b48663f19f86f2f2c88cebffcce95f5a5fa6616d135`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d55f05dd933db96cfff6a4e5f483c12fdb5d4853b472efdc34addfba9adce5`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:46f944b88b8a13c7421c07ea51f731e58a987b2635fdf8650e87e9ac9840126d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24990384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc39fbef2781915c079d96adc5598538cb87a840f94451f468afb2d58272f08`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:56 GMT
ADD file:1c25b0be52aae22767603d9404fb777e27c5dd1bcd627221aac7517ac1bce1e3 in / 
# Thu, 15 Jun 2023 00:39:57 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:19:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 01:19:45 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 01:21:32 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 01:21:34 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 01:21:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 01:21:35 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 01:21:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 01:21:35 GMT
ENV LD_PRELOAD=
# Thu, 15 Jun 2023 01:21:35 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 01:21:36 GMT
USER fluent
# Thu, 15 Jun 2023 01:21:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 01:21:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8436307590cda5ccded8a952bb1d66684f8700d07029527293dd695eac6fabc9`  
		Last Modified: Thu, 15 Jun 2023 00:40:39 GMT  
		Size: 3.4 MB (3389905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36c754d297b712a3b01e94c0889e4ee1ac910329697a77af30c59399c6f35e`  
		Last Modified: Thu, 15 Jun 2023 01:21:53 GMT  
		Size: 21.6 MB (21598263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de15ece87dd127cea88f5fbf5585862b80ea0d42a78277c7630fff6e390f5d6e`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90690dc8b53f185884d4cdf4637b55205c9ec69ae8ca4230bfefcc56f0d73059`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40d3764445452729ff14f9baa7741a4629e8559bda9a15d056127079610ad5`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:0eca4ef0016e438285466df4bb26d01bcb4b5f6917204fc624ebcea277da19af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24350771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6380a5ce2eebdc34d9d306fb1bce908c794d935a07b34ffcdbc8e9670b949888`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 15 Jun 2023 05:19:50 GMT
ADD file:8ad8a62cf274ba5a6568f68473359114136cb5c7704bfdfce6c38efef3081782 in / 
# Thu, 15 Jun 2023 05:19:51 GMT
CMD ["/bin/sh"]
# Fri, 16 Jun 2023 15:59:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 16 Jun 2023 15:59:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Fri, 16 Jun 2023 15:59:48 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Fri, 16 Jun 2023 15:59:50 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 16 Jun 2023 15:59:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 16 Jun 2023 15:59:50 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Fri, 16 Jun 2023 15:59:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 16 Jun 2023 15:59:50 GMT
ENV LD_PRELOAD=
# Fri, 16 Jun 2023 15:59:50 GMT
EXPOSE 24224 5140
# Fri, 16 Jun 2023 15:59:50 GMT
USER fluent
# Fri, 16 Jun 2023 15:59:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 16 Jun 2023 15:59:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb857838eb854a669f87c5df4d936d905fb3129287a93ef485da9454c11d83cd`  
		Last Modified: Thu, 15 Jun 2023 05:30:48 GMT  
		Size: 3.2 MB (3174898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f1b18f8ded554cde5661033b74a4e3b4bad2bd80230481b96b69f3360160d`  
		Last Modified: Fri, 16 Jun 2023 16:02:29 GMT  
		Size: 21.2 MB (21173659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad936c342ea21c5106019b9be1df731153880705e616c6e2d71d446753c0b2c5`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace1d7c86ddcf6229d208ec207fc224767ec347ccf4f974b8c57c8a26eeaffb0`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50102c62b4f97e641525451ef7002e41759658e1a5248bb17918d5190dbecea`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:fa22cbe77cba960e8311cdd956a503708127e9e9b3530a89e708c26f12dea812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16-1` - linux; amd64

```console
$ docker pull fluentd@sha256:d07aaa6eba6a96328e2b3a0a0ccb586e556e629f1937141c7f1bd8689798cd30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25138920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d619c23c9ae269bd4d905563b3b29e8cf52f3b43a98e608ae7f3bc9f3813a07d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:33:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 22:33:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 22:34:23 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 22:34:23 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 22:34:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 22:34:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 22:34:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 22:34:24 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 22:34:24 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 22:34:24 GMT
USER fluent
# Wed, 14 Jun 2023 22:34:24 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 22:34:24 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e89884591749689529cd5fa296197dbf2d081b89aa1acf0d521f4c2c6f96bf`  
		Last Modified: Wed, 14 Jun 2023 22:34:37 GMT  
		Size: 21.8 MB (21761995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390a858b50010d973d4e1a5f6da84ba514b82536de40dc734fc35889c5579cca`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d69a60bc67d80beffeb819bcf5409aa6ac1cece761ac175179bcbd081de713`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389b15490d254354e083d9cecd8372dd8a7d24f42f48553b5be44087f846d3cb`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:4c7a522f2f52fded55c7e7eb1cbfbf95071cb89602efd1c16d10173e1052bc19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23818795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9449002b91a5e83fa600b072a1849a3bde33395ab9912736df9ebcf0af9ca07a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:39:12 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 20:39:12 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 20:40:14 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 20:40:14 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 20:40:14 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 20:40:15 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 20:40:15 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 20:40:15 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 20:40:15 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 20:40:15 GMT
USER fluent
# Wed, 14 Jun 2023 20:40:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 20:40:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff90db882f9f0c92f1e98e1b0070fce952033d478a6d6f2139bc6b8deccf4c1`  
		Last Modified: Wed, 14 Jun 2023 20:40:32 GMT  
		Size: 20.7 MB (20705668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409eb899470f9c46b8b52fef13f7747862956ea44d1131402ecdf43a4e62cd4e`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8c355cf22653f5ecf08a38e9747568282212437249dbde1843db76413ac703`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d173e8e240a98c6b2fead4204509ef9ee0ef181fa18818047b1a21744741ef6`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5504f34bf0fdd8c584dde9ece653aef92fab0ec0488b02d09c0c60773873fec0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24615958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625b9c7556aca650f5c149011e1045a1f41a52c022bf6c00d120a443212a2135`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:16:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 23:16:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 23:17:17 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 23:17:18 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 23:17:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 23:17:18 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 23:17:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 23:17:18 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 23:17:18 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 23:17:18 GMT
USER fluent
# Wed, 14 Jun 2023 23:17:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 23:17:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c596c0811598d44ad0388635c2457814da7ec0aeeaa500f5a227ea1ef522859`  
		Last Modified: Wed, 14 Jun 2023 23:17:36 GMT  
		Size: 21.4 MB (21352606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdb87eceb2348af0bce9ef18e4af5f4138cce349e7ddfa9e358e589f1a61928`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8277de9dddc2b555e88ca9500be77262f4bfd85ec1150f4f0bbd390d5d0a86`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2236a61df5e8c4f1cb997555c37c1bec0623a75612f1541cbac90f9f00ffe7b6`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:70073fa5febf90614d06e9ff0993cebadb1d5e3e997a08eb2a3d59133a4f8290
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24413017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98833d32fe9d59d6ae41f918d717cabd71fab1a49b6d830d13eea6a2cace22b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:04:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 03:04:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 03:05:53 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 03:05:54 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 03:05:54 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 03:05:54 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 03:05:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 03:05:55 GMT
ENV LD_PRELOAD=
# Thu, 15 Jun 2023 03:05:55 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 03:05:55 GMT
USER fluent
# Thu, 15 Jun 2023 03:05:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 03:05:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04560289ee3119fe99bb33739daabb776b0eaf4089ddac2f7a1be9070a9a83f1`  
		Last Modified: Thu, 15 Jun 2023 03:06:13 GMT  
		Size: 21.0 MB (20998130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda7a209cb4c0bbe12aa1ec14332a039e01a4cc4312ffafbf410faae5128fc75`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ce2515314e17a9c15c6b48663f19f86f2f2c88cebffcce95f5a5fa6616d135`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d55f05dd933db96cfff6a4e5f483c12fdb5d4853b472efdc34addfba9adce5`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:46f944b88b8a13c7421c07ea51f731e58a987b2635fdf8650e87e9ac9840126d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24990384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc39fbef2781915c079d96adc5598538cb87a840f94451f468afb2d58272f08`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:56 GMT
ADD file:1c25b0be52aae22767603d9404fb777e27c5dd1bcd627221aac7517ac1bce1e3 in / 
# Thu, 15 Jun 2023 00:39:57 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:19:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 01:19:45 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 01:21:32 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 01:21:34 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 01:21:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 01:21:35 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 01:21:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 01:21:35 GMT
ENV LD_PRELOAD=
# Thu, 15 Jun 2023 01:21:35 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 01:21:36 GMT
USER fluent
# Thu, 15 Jun 2023 01:21:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 01:21:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8436307590cda5ccded8a952bb1d66684f8700d07029527293dd695eac6fabc9`  
		Last Modified: Thu, 15 Jun 2023 00:40:39 GMT  
		Size: 3.4 MB (3389905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36c754d297b712a3b01e94c0889e4ee1ac910329697a77af30c59399c6f35e`  
		Last Modified: Thu, 15 Jun 2023 01:21:53 GMT  
		Size: 21.6 MB (21598263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de15ece87dd127cea88f5fbf5585862b80ea0d42a78277c7630fff6e390f5d6e`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90690dc8b53f185884d4cdf4637b55205c9ec69ae8ca4230bfefcc56f0d73059`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40d3764445452729ff14f9baa7741a4629e8559bda9a15d056127079610ad5`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:0eca4ef0016e438285466df4bb26d01bcb4b5f6917204fc624ebcea277da19af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24350771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6380a5ce2eebdc34d9d306fb1bce908c794d935a07b34ffcdbc8e9670b949888`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 15 Jun 2023 05:19:50 GMT
ADD file:8ad8a62cf274ba5a6568f68473359114136cb5c7704bfdfce6c38efef3081782 in / 
# Thu, 15 Jun 2023 05:19:51 GMT
CMD ["/bin/sh"]
# Fri, 16 Jun 2023 15:59:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 16 Jun 2023 15:59:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Fri, 16 Jun 2023 15:59:48 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Fri, 16 Jun 2023 15:59:50 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 16 Jun 2023 15:59:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 16 Jun 2023 15:59:50 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Fri, 16 Jun 2023 15:59:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 16 Jun 2023 15:59:50 GMT
ENV LD_PRELOAD=
# Fri, 16 Jun 2023 15:59:50 GMT
EXPOSE 24224 5140
# Fri, 16 Jun 2023 15:59:50 GMT
USER fluent
# Fri, 16 Jun 2023 15:59:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 16 Jun 2023 15:59:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb857838eb854a669f87c5df4d936d905fb3129287a93ef485da9454c11d83cd`  
		Last Modified: Thu, 15 Jun 2023 05:30:48 GMT  
		Size: 3.2 MB (3174898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f1b18f8ded554cde5661033b74a4e3b4bad2bd80230481b96b69f3360160d`  
		Last Modified: Fri, 16 Jun 2023 16:02:29 GMT  
		Size: 21.2 MB (21173659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad936c342ea21c5106019b9be1df731153880705e616c6e2d71d446753c0b2c5`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace1d7c86ddcf6229d208ec207fc224767ec347ccf4f974b8c57c8a26eeaffb0`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50102c62b4f97e641525451ef7002e41759658e1a5248bb17918d5190dbecea`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:9c71b09b27421d7fe56dd9afb67138f0719d2a68d06b4ead2b1589222022fd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:2b62dafd30ec556da7ce1bd29373b7d25e3d7e1a577262477c20d2cec7553850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101774005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2887eae1bfd0e107a0f5d37e696fbb8fdc850220f389ae182ba618ff215958ec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:35:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 13:35:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 13:55:34 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 13:55:34 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 13:55:34 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 20:06:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 20:06:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 20:06:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 20:06:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 20:06:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 20:06:23 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 20:38:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 20:38:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 20:38:48 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 20:41:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 20:41:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 20:41:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 20:41:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 20:41:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 20:41:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 20:41:23 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 20:41:23 GMT
USER fluent
# Wed, 14 Jun 2023 20:41:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 20:41:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59420411322ab5f192608db1f415e70c504baffc041aff12c8289f0d2d7387d7`  
		Last Modified: Tue, 13 Jun 2023 14:12:08 GMT  
		Size: 10.0 MB (10020678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69ab9c0147a72fbe0792264cab42ee7557130f85e5a90e1a8326fed4ff3ac8`  
		Last Modified: Tue, 13 Jun 2023 14:12:06 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db1102f90fac1553dc82ee7770d769f7344c25ffb9b87f87f2e60766923cf16`  
		Last Modified: Wed, 14 Jun 2023 20:19:18 GMT  
		Size: 32.6 MB (32626065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49db04b1e9718b0df8f4cbb6ebcb1629f545d3cbc12edaa08fa548814b51226`  
		Last Modified: Wed, 14 Jun 2023 20:19:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90b7510995ec6b8e6f78b99c56ab2fa47758a0a568b220f7b92851185026be8`  
		Last Modified: Wed, 14 Jun 2023 20:41:36 GMT  
		Size: 27.7 MB (27706775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ee4b99bc316ca9f7e95a2bab404daea5403ff491c08ea9f7acc900a984b92b`  
		Last Modified: Wed, 14 Jun 2023 20:41:32 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b457c6d0b268a8dd8b4206aa9132677bbbb8d7dae683203a8c59adbf15d26d69`  
		Last Modified: Wed, 14 Jun 2023 20:41:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eec0a3cb62c2f1248d42ad789853c763a5e9a09aae0d890143e5438336f3c10`  
		Last Modified: Wed, 14 Jun 2023 20:41:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:958bf7bdeea456fba34521b2141eae053aef8344223587c67e416468b1b20453
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95269245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fc656f38bff690f14d0991751275f8844368d3b4d23f410f816eddeaa99b94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:48:46 GMT
ADD file:b2773fa62bdb5672863ef317ee1b58de2a6074fe6aa0d8287a7cd0999028d7d2 in / 
# Mon, 12 Jun 2023 23:48:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 09:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 09:28:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 09:28:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 09:37:44 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 09:37:44 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 09:37:45 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 21:18:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 21:18:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 21:18:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 21:18:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 21:18:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 21:18:07 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 21:46:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 21:46:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 21:46:46 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 21:50:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 21:50:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 21:50:19 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 21:50:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 21:50:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 21:50:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 21:50:20 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 21:50:20 GMT
USER fluent
# Wed, 14 Jun 2023 21:50:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 21:50:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c04d7d6633d9b8cf1bfa9f6831ac7dd6f985411cb6307d91c6373085b09b8c19`  
		Last Modified: Mon, 12 Jun 2023 23:52:06 GMT  
		Size: 28.9 MB (28918779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2530008eaccbf72a6d2e8dc83176f59f6bb5682cfa7196c800473b54e569b9`  
		Last Modified: Tue, 13 Jun 2023 09:44:56 GMT  
		Size: 8.6 MB (8632331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271b74ac6a22fefe1943af855b14148bd832a4527d79a57d261c3c44dd905f2`  
		Last Modified: Tue, 13 Jun 2023 09:44:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d5170d2ff7cb9c4da63a96b1fdbcb7fdba69ebb3bc0cc88d853f8512e2d886`  
		Last Modified: Wed, 14 Jun 2023 21:30:56 GMT  
		Size: 31.2 MB (31166052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece56e482f0e2e4c0f6a537d7b23ab7b5a4b2fb481da552a11aee1b5929505d`  
		Last Modified: Wed, 14 Jun 2023 21:30:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00f9c9b23617f63a4f48143190a9ee7d6cab51668390635f7292d1d9a1bf5f0`  
		Last Modified: Wed, 14 Jun 2023 21:50:34 GMT  
		Size: 26.5 MB (26549014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718f190d616a22230a70fd27a7a72386dafc4994834571fe3dd98c19265da676`  
		Last Modified: Wed, 14 Jun 2023 21:50:29 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08201d74e5aa39b983fe90e919211b44f84b9bbe18bf35186b48c9e62bda60`  
		Last Modified: Wed, 14 Jun 2023 21:50:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6967807a7323b36e15ccd4d578f8bb8f44fb56dcf90df56c87b3330367bbe1f`  
		Last Modified: Wed, 14 Jun 2023 21:50:29 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:638dfa126c2923a8d813fc7f5bf48652bdd1ce335e5cfec4e4bcdfe9dda0899a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92142506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0738379acd46890b92ff70f8c0140c3a968647e44fdae0773627cec43cd8b71b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 14:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 14:33:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 14:33:56 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 14:58:46 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 14:58:47 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 14:58:47 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 21:50:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 21:50:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 21:50:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 21:50:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 21:50:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 21:50:40 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 22:31:57 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 22:31:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 22:31:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 22:35:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 22:35:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 22:35:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 22:35:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 22:35:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 22:35:24 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 22:35:24 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 22:35:24 GMT
USER fluent
# Wed, 14 Jun 2023 22:35:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 22:35:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999000f64bf28ef182f07e5f4ba36592dd2706cff1575d5f7ca90df97f79ab00`  
		Last Modified: Tue, 13 Jun 2023 15:16:19 GMT  
		Size: 8.1 MB (8141546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab00ea46680fc55ca887a14fced3aa27fae13c44b7352faa153ba339ae2b7139`  
		Last Modified: Tue, 13 Jun 2023 15:16:17 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1a83c629c9c8fccb8ae2505159e462aec0a767dff7f507dc7d239b9b56dc15`  
		Last Modified: Wed, 14 Jun 2023 22:10:25 GMT  
		Size: 31.0 MB (31035390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b8831b4b656f1ee08d25a3779ebf89b387af027fa9fd0007cc9fbe4be3a842`  
		Last Modified: Wed, 14 Jun 2023 22:10:20 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e18eae1bb80b57bd995c69a086475a7237466c7e7801838743320431603c1a`  
		Last Modified: Wed, 14 Jun 2023 22:35:46 GMT  
		Size: 26.4 MB (26383806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a675b3ef506729b9aa2c3e55073cd0c184bfd914943ea2da3368679106dc6862`  
		Last Modified: Wed, 14 Jun 2023 22:35:40 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27068cc9d6741a0b964932ebc24225407bdf7132b46cd17854caaa52a62764f`  
		Last Modified: Wed, 14 Jun 2023 22:35:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257abcec41581086b81dd4a4157539790488a4489e08a0e858082157d66f3e1a`  
		Last Modified: Wed, 14 Jun 2023 22:35:40 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:265290eac3a3b0e730962af326206b41548e5cdc4dc62eab0aefc61ad410dda2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98777554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084516af09ee1e692ccd5af3b49506735136d94e51ca501c994e7cfcf3a83321`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:07:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 13:07:21 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 13:24:06 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 13:24:06 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 13:24:07 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 20:13:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 20:13:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 20:13:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 20:13:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 20:13:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 20:13:15 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 20:44:02 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 20:44:02 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 20:44:02 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 20:46:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 20:46:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 20:46:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 20:46:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 20:46:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 20:46:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 20:46:20 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 20:46:20 GMT
USER fluent
# Wed, 14 Jun 2023 20:46:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 20:46:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6764f9140e90ce73f5fb4d2a65dcfe0fe6c9923b4258b62641cca67b8617d91f`  
		Last Modified: Tue, 13 Jun 2023 13:36:54 GMT  
		Size: 9.2 MB (9242110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bb19ae3f8d4635186d2a44346ad9d54f1fe0aee91d1a3795a8a53f76bb3fc0`  
		Last Modified: Tue, 13 Jun 2023 13:36:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6569f27e27c33ce56a0ea0cfcb75299cec795e3bd2b216c2575de9e8e8b175`  
		Last Modified: Wed, 14 Jun 2023 20:23:58 GMT  
		Size: 32.0 MB (31987325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ae9e9f387ec7cd850e6f15ef05379fc0adede2002f99fb51fe29478f737e`  
		Last Modified: Wed, 14 Jun 2023 20:23:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6579ab2a30a64f4f5a41f221348667791d7cee7314eae7a5376a51cbb50b0ebf`  
		Last Modified: Wed, 14 Jun 2023 20:46:34 GMT  
		Size: 27.5 MB (27482203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f4f1d04efa08cd66343efed3a25bc93f306843fcc43f69bd648ae543e0772`  
		Last Modified: Wed, 14 Jun 2023 20:46:31 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38885c8d68da579855553ce2827900bb2f10215ea317e931b23e0672c9f81d2`  
		Last Modified: Wed, 14 Jun 2023 20:46:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fcdbcc3ed11e024906fd5edd8cd6d005ab2aba38e3ca027d38ebe2fd8f93a0`  
		Last Modified: Wed, 14 Jun 2023 20:46:31 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:d26fdb3de1a9fba3a67d64f2188514041596558b0fcc4bb297e31c69d4b796b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102170573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d761cf2ddfb6b92b77cf4bb86af8034be3d98300a5b087aa6bbc8ba312fd676`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 00:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 00:07:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 00:07:52 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 00:23:23 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 00:23:23 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 00:23:23 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 18:38:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 18:38:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 18:38:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 18:38:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 18:39:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 18:39:00 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 22:14:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 22:14:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 22:14:11 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 22:17:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 22:17:12 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 22:17:12 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 22:17:12 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 22:17:12 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 22:17:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 22:17:13 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 22:17:13 GMT
USER fluent
# Wed, 14 Jun 2023 22:17:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 22:17:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae39782333ba3b6797929e1de5919e6f957f07c4bf4f388316b264ad2de47abd`  
		Last Modified: Tue, 13 Jun 2023 00:38:45 GMT  
		Size: 12.0 MB (11994868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbed6977b262b949787e1f257c80b388f10f3e706301cdf5ebcae6f87adb254`  
		Last Modified: Tue, 13 Jun 2023 00:38:41 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b58c6bd82e64852dedd16b0c9bf371668361a08456e2ae2a7fb54ff7696b99`  
		Last Modified: Wed, 14 Jun 2023 18:56:29 GMT  
		Size: 31.2 MB (31181698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1168f0602606a4764bd9199ce64d841467925d1424587cc20fb40dcffb62ef`  
		Last Modified: Wed, 14 Jun 2023 18:56:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1feb3eda883ea03c3920d608f2b8de848c5a0be279f8bf3cc473acf69a7f056`  
		Last Modified: Wed, 14 Jun 2023 22:17:32 GMT  
		Size: 26.6 MB (26593550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f55ee4d8d1db832ab044a310e1cdf37b943d19478ebe7603837839dc6316b0`  
		Last Modified: Wed, 14 Jun 2023 22:17:28 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002dcaacc2acb43ceaa709e771ecfedf2db1f77098386d5817b85007a52f6489`  
		Last Modified: Wed, 14 Jun 2023 22:17:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767512f5f03efe4aa3ee14779e556efc4478d70010b4c3e999f834f846a1dc21`  
		Last Modified: Wed, 14 Jun 2023 22:17:28 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:de4a254772d7baa6b6acaf231d087f91036436022712625540ffb1b151c4f22d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106775294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ecd7b2b5794f16aa691277c98b08d4bb09c10e9335785c232248240e09fb69`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:06:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 07:06:52 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:15:37 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 07:15:37 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 07:15:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 23:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 23:30:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 23:30:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 23:30:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 23:30:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 23:30:09 GMT
CMD ["irb"]
# Thu, 15 Jun 2023 00:32:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 00:32:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 00:32:42 GMT
ENV TINI_VERSION=0.18.0
# Thu, 15 Jun 2023 00:37:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 00:37:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 00:37:55 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 00:37:55 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 00:37:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 00:37:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 15 Jun 2023 00:37:56 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 00:37:56 GMT
USER fluent
# Thu, 15 Jun 2023 00:37:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 00:37:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba11d9646199a3947e54ff4f564451778648eefd9055af564c1038e730488cb4`  
		Last Modified: Tue, 13 Jun 2023 07:24:25 GMT  
		Size: 10.5 MB (10478333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d79ea6089ae4241c276607e8b544d5c626cf8223e52c3dd7a42d03c6a44ae98`  
		Last Modified: Tue, 13 Jun 2023 07:24:22 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dacdff1086d66ea2e321cd6dc456d8880416267dcd38492948bbfc77958fbe4`  
		Last Modified: Wed, 14 Jun 2023 23:42:09 GMT  
		Size: 32.8 MB (32791556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c55ccf4f31798e6eaf295778f2994f8cdf51dbe03e8d96dc9ecbad85465ee8`  
		Last Modified: Wed, 14 Jun 2023 23:42:04 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f6aab677dfcab0b85f56a74bd03cd703b36c6ca8f7aa952461187e4995e83`  
		Last Modified: Thu, 15 Jun 2023 00:38:22 GMT  
		Size: 28.2 MB (28211535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d932948fb8dfa58cc95c0621ff2d5aa52c6f1e26516819322dd5de667c4452`  
		Last Modified: Thu, 15 Jun 2023 00:38:15 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98106a542a935a9d32cc61c0e0545150bc2de6d343a1529b996c274574742aa1`  
		Last Modified: Thu, 15 Jun 2023 00:38:15 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c33060818be3afe37d5177ab68aa46f5ce1d0fa1738731cd12ebb5ba27549f`  
		Last Modified: Thu, 15 Jun 2023 00:38:16 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:3ea4a6edd4c873532726c47a17be26ed3ca7027055dfe1a5d4e1b6ab3589c9ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98901239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df46366c41abe4c0e894aa34298d2bb93d1ceb68b84a3fc459d7157d538327f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:09:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:09:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 18:09:07 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:14:11 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:14:11 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:14:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 15 Jun 2023 16:23:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 16:23:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 16:23:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 16:23:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 16:23:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 16:23:38 GMT
CMD ["irb"]
# Fri, 16 Jun 2023 16:00:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 16 Jun 2023 16:00:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Fri, 16 Jun 2023 16:00:00 GMT
ENV TINI_VERSION=0.18.0
# Fri, 16 Jun 2023 16:02:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Fri, 16 Jun 2023 16:02:09 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 16 Jun 2023 16:02:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 16 Jun 2023 16:02:09 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Fri, 16 Jun 2023 16:02:09 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 16 Jun 2023 16:02:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 16 Jun 2023 16:02:10 GMT
EXPOSE 24224 5140
# Fri, 16 Jun 2023 16:02:10 GMT
USER fluent
# Fri, 16 Jun 2023 16:02:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 16 Jun 2023 16:02:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324883160edf8f3ab5900f91d3562af2eb6fe2e5199bb0cf5466029297d8a685`  
		Last Modified: Tue, 13 Jun 2023 18:19:42 GMT  
		Size: 8.9 MB (8861927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3903959d9528f3e1013f3b14204e97e6b43ed28f73143ea14374e21dbf260cbd`  
		Last Modified: Tue, 13 Jun 2023 18:19:40 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42442750523fba0b3b1195c59f3424d6360fbe07a34e912f8a38dc73786a1e4e`  
		Last Modified: Thu, 15 Jun 2023 17:25:16 GMT  
		Size: 32.4 MB (32444923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b366d91a9011a26dc8e18532df71398718c7f8c91b8af69f3aa9d38ed5ed08e`  
		Last Modified: Thu, 15 Jun 2023 17:25:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7c3c84d330c977e441c794474e5024c79578d393b81c1f4319601b6911ee82`  
		Last Modified: Fri, 16 Jun 2023 16:02:41 GMT  
		Size: 27.9 MB (27938798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdccd2f69a2a1ca7c963c873a257091bb52bfd19a0205474db0ae15ea16f5fe8`  
		Last Modified: Fri, 16 Jun 2023 16:02:36 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1633ee4e3112b4e9d3837630b8345f37ada86287c1734d7bd53d9c8ce2b55a`  
		Last Modified: Fri, 16 Jun 2023 16:02:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fbefff65957dd4705fdc33cec4914bf818e19fc45e80f6bdd7269851e5ba42`  
		Last Modified: Fri, 16 Jun 2023 16:02:37 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.0-1.0`

```console
$ docker pull fluentd@sha256:fa22cbe77cba960e8311cdd956a503708127e9e9b3530a89e708c26f12dea812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16.0-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:d07aaa6eba6a96328e2b3a0a0ccb586e556e629f1937141c7f1bd8689798cd30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25138920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d619c23c9ae269bd4d905563b3b29e8cf52f3b43a98e608ae7f3bc9f3813a07d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:33:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 22:33:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 22:34:23 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 22:34:23 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 22:34:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 22:34:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 22:34:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 22:34:24 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 22:34:24 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 22:34:24 GMT
USER fluent
# Wed, 14 Jun 2023 22:34:24 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 22:34:24 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e89884591749689529cd5fa296197dbf2d081b89aa1acf0d521f4c2c6f96bf`  
		Last Modified: Wed, 14 Jun 2023 22:34:37 GMT  
		Size: 21.8 MB (21761995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390a858b50010d973d4e1a5f6da84ba514b82536de40dc734fc35889c5579cca`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d69a60bc67d80beffeb819bcf5409aa6ac1cece761ac175179bcbd081de713`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389b15490d254354e083d9cecd8372dd8a7d24f42f48553b5be44087f846d3cb`  
		Last Modified: Wed, 14 Jun 2023 22:34:34 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:4c7a522f2f52fded55c7e7eb1cbfbf95071cb89602efd1c16d10173e1052bc19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23818795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9449002b91a5e83fa600b072a1849a3bde33395ab9912736df9ebcf0af9ca07a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:39:12 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 20:39:12 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 20:40:14 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 20:40:14 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 20:40:14 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 20:40:15 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 20:40:15 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 20:40:15 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 20:40:15 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 20:40:15 GMT
USER fluent
# Wed, 14 Jun 2023 20:40:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 20:40:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff90db882f9f0c92f1e98e1b0070fce952033d478a6d6f2139bc6b8deccf4c1`  
		Last Modified: Wed, 14 Jun 2023 20:40:32 GMT  
		Size: 20.7 MB (20705668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409eb899470f9c46b8b52fef13f7747862956ea44d1131402ecdf43a4e62cd4e`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8c355cf22653f5ecf08a38e9747568282212437249dbde1843db76413ac703`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d173e8e240a98c6b2fead4204509ef9ee0ef181fa18818047b1a21744741ef6`  
		Last Modified: Wed, 14 Jun 2023 20:40:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5504f34bf0fdd8c584dde9ece653aef92fab0ec0488b02d09c0c60773873fec0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24615958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625b9c7556aca650f5c149011e1045a1f41a52c022bf6c00d120a443212a2135`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:16:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 23:16:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 23:17:17 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 23:17:18 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 23:17:18 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 23:17:18 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 23:17:18 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 23:17:18 GMT
ENV LD_PRELOAD=
# Wed, 14 Jun 2023 23:17:18 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 23:17:18 GMT
USER fluent
# Wed, 14 Jun 2023 23:17:18 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 23:17:18 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c596c0811598d44ad0388635c2457814da7ec0aeeaa500f5a227ea1ef522859`  
		Last Modified: Wed, 14 Jun 2023 23:17:36 GMT  
		Size: 21.4 MB (21352606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdb87eceb2348af0bce9ef18e4af5f4138cce349e7ddfa9e358e589f1a61928`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8277de9dddc2b555e88ca9500be77262f4bfd85ec1150f4f0bbd390d5d0a86`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2236a61df5e8c4f1cb997555c37c1bec0623a75612f1541cbac90f9f00ffe7b6`  
		Last Modified: Wed, 14 Jun 2023 23:17:34 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:70073fa5febf90614d06e9ff0993cebadb1d5e3e997a08eb2a3d59133a4f8290
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24413017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98833d32fe9d59d6ae41f918d717cabd71fab1a49b6d830d13eea6a2cace22b4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:04:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 03:04:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 03:05:53 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 03:05:54 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 03:05:54 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 03:05:54 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 03:05:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 03:05:55 GMT
ENV LD_PRELOAD=
# Thu, 15 Jun 2023 03:05:55 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 03:05:55 GMT
USER fluent
# Thu, 15 Jun 2023 03:05:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 03:05:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04560289ee3119fe99bb33739daabb776b0eaf4089ddac2f7a1be9070a9a83f1`  
		Last Modified: Thu, 15 Jun 2023 03:06:13 GMT  
		Size: 21.0 MB (20998130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda7a209cb4c0bbe12aa1ec14332a039e01a4cc4312ffafbf410faae5128fc75`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ce2515314e17a9c15c6b48663f19f86f2f2c88cebffcce95f5a5fa6616d135`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d55f05dd933db96cfff6a4e5f483c12fdb5d4853b472efdc34addfba9adce5`  
		Last Modified: Thu, 15 Jun 2023 03:06:09 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:46f944b88b8a13c7421c07ea51f731e58a987b2635fdf8650e87e9ac9840126d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24990384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc39fbef2781915c079d96adc5598538cb87a840f94451f468afb2d58272f08`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:56 GMT
ADD file:1c25b0be52aae22767603d9404fb777e27c5dd1bcd627221aac7517ac1bce1e3 in / 
# Thu, 15 Jun 2023 00:39:57 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:19:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 01:19:45 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 01:21:32 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 01:21:34 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 01:21:35 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 01:21:35 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 01:21:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 01:21:35 GMT
ENV LD_PRELOAD=
# Thu, 15 Jun 2023 01:21:35 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 01:21:36 GMT
USER fluent
# Thu, 15 Jun 2023 01:21:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 01:21:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8436307590cda5ccded8a952bb1d66684f8700d07029527293dd695eac6fabc9`  
		Last Modified: Thu, 15 Jun 2023 00:40:39 GMT  
		Size: 3.4 MB (3389905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df36c754d297b712a3b01e94c0889e4ee1ac910329697a77af30c59399c6f35e`  
		Last Modified: Thu, 15 Jun 2023 01:21:53 GMT  
		Size: 21.6 MB (21598263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de15ece87dd127cea88f5fbf5585862b80ea0d42a78277c7630fff6e390f5d6e`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90690dc8b53f185884d4cdf4637b55205c9ec69ae8ca4230bfefcc56f0d73059`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e40d3764445452729ff14f9baa7741a4629e8559bda9a15d056127079610ad5`  
		Last Modified: Thu, 15 Jun 2023 01:21:48 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:0eca4ef0016e438285466df4bb26d01bcb4b5f6917204fc624ebcea277da19af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24350771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6380a5ce2eebdc34d9d306fb1bce908c794d935a07b34ffcdbc8e9670b949888`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 15 Jun 2023 05:19:50 GMT
ADD file:8ad8a62cf274ba5a6568f68473359114136cb5c7704bfdfce6c38efef3081782 in / 
# Thu, 15 Jun 2023 05:19:51 GMT
CMD ["/bin/sh"]
# Fri, 16 Jun 2023 15:59:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 16 Jun 2023 15:59:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Fri, 16 Jun 2023 15:59:48 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Fri, 16 Jun 2023 15:59:50 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 16 Jun 2023 15:59:50 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 16 Jun 2023 15:59:50 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Fri, 16 Jun 2023 15:59:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 16 Jun 2023 15:59:50 GMT
ENV LD_PRELOAD=
# Fri, 16 Jun 2023 15:59:50 GMT
EXPOSE 24224 5140
# Fri, 16 Jun 2023 15:59:50 GMT
USER fluent
# Fri, 16 Jun 2023 15:59:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 16 Jun 2023 15:59:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb857838eb854a669f87c5df4d936d905fb3129287a93ef485da9454c11d83cd`  
		Last Modified: Thu, 15 Jun 2023 05:30:48 GMT  
		Size: 3.2 MB (3174898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f1b18f8ded554cde5661033b74a4e3b4bad2bd80230481b96b69f3360160d`  
		Last Modified: Fri, 16 Jun 2023 16:02:29 GMT  
		Size: 21.2 MB (21173659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad936c342ea21c5106019b9be1df731153880705e616c6e2d71d446753c0b2c5`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace1d7c86ddcf6229d208ec207fc224767ec347ccf4f974b8c57c8a26eeaffb0`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50102c62b4f97e641525451ef7002e41759658e1a5248bb17918d5190dbecea`  
		Last Modified: Fri, 16 Jun 2023 16:02:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fluentd:v1.16.0-debian-1.0`

```console
$ docker pull fluentd@sha256:9c71b09b27421d7fe56dd9afb67138f0719d2a68d06b4ead2b1589222022fd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `fluentd:v1.16.0-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:2b62dafd30ec556da7ce1bd29373b7d25e3d7e1a577262477c20d2cec7553850
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101774005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2887eae1bfd0e107a0f5d37e696fbb8fdc850220f389ae182ba618ff215958ec`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:35:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 13:35:11 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 13:55:34 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 13:55:34 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 13:55:34 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 20:06:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 20:06:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 20:06:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 20:06:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 20:06:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 20:06:23 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 20:38:48 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 20:38:48 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 20:38:48 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 20:41:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 20:41:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 20:41:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 20:41:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 20:41:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 20:41:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 20:41:23 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 20:41:23 GMT
USER fluent
# Wed, 14 Jun 2023 20:41:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 20:41:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59420411322ab5f192608db1f415e70c504baffc041aff12c8289f0d2d7387d7`  
		Last Modified: Tue, 13 Jun 2023 14:12:08 GMT  
		Size: 10.0 MB (10020678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a69ab9c0147a72fbe0792264cab42ee7557130f85e5a90e1a8326fed4ff3ac8`  
		Last Modified: Tue, 13 Jun 2023 14:12:06 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db1102f90fac1553dc82ee7770d769f7344c25ffb9b87f87f2e60766923cf16`  
		Last Modified: Wed, 14 Jun 2023 20:19:18 GMT  
		Size: 32.6 MB (32626065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49db04b1e9718b0df8f4cbb6ebcb1629f545d3cbc12edaa08fa548814b51226`  
		Last Modified: Wed, 14 Jun 2023 20:19:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90b7510995ec6b8e6f78b99c56ab2fa47758a0a568b220f7b92851185026be8`  
		Last Modified: Wed, 14 Jun 2023 20:41:36 GMT  
		Size: 27.7 MB (27706775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ee4b99bc316ca9f7e95a2bab404daea5403ff491c08ea9f7acc900a984b92b`  
		Last Modified: Wed, 14 Jun 2023 20:41:32 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b457c6d0b268a8dd8b4206aa9132677bbbb8d7dae683203a8c59adbf15d26d69`  
		Last Modified: Wed, 14 Jun 2023 20:41:33 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eec0a3cb62c2f1248d42ad789853c763a5e9a09aae0d890143e5438336f3c10`  
		Last Modified: Wed, 14 Jun 2023 20:41:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:958bf7bdeea456fba34521b2141eae053aef8344223587c67e416468b1b20453
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95269245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fc656f38bff690f14d0991751275f8844368d3b4d23f410f816eddeaa99b94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:48:46 GMT
ADD file:b2773fa62bdb5672863ef317ee1b58de2a6074fe6aa0d8287a7cd0999028d7d2 in / 
# Mon, 12 Jun 2023 23:48:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 09:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 09:28:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 09:28:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 09:37:44 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 09:37:44 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 09:37:45 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 21:18:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 21:18:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 21:18:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 21:18:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 21:18:07 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 21:18:07 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 21:46:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 21:46:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 21:46:46 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 21:50:18 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 21:50:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 21:50:19 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 21:50:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 21:50:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 21:50:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 21:50:20 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 21:50:20 GMT
USER fluent
# Wed, 14 Jun 2023 21:50:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 21:50:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c04d7d6633d9b8cf1bfa9f6831ac7dd6f985411cb6307d91c6373085b09b8c19`  
		Last Modified: Mon, 12 Jun 2023 23:52:06 GMT  
		Size: 28.9 MB (28918779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2530008eaccbf72a6d2e8dc83176f59f6bb5682cfa7196c800473b54e569b9`  
		Last Modified: Tue, 13 Jun 2023 09:44:56 GMT  
		Size: 8.6 MB (8632331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271b74ac6a22fefe1943af855b14148bd832a4527d79a57d261c3c44dd905f2`  
		Last Modified: Tue, 13 Jun 2023 09:44:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d5170d2ff7cb9c4da63a96b1fdbcb7fdba69ebb3bc0cc88d853f8512e2d886`  
		Last Modified: Wed, 14 Jun 2023 21:30:56 GMT  
		Size: 31.2 MB (31166052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece56e482f0e2e4c0f6a537d7b23ab7b5a4b2fb481da552a11aee1b5929505d`  
		Last Modified: Wed, 14 Jun 2023 21:30:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00f9c9b23617f63a4f48143190a9ee7d6cab51668390635f7292d1d9a1bf5f0`  
		Last Modified: Wed, 14 Jun 2023 21:50:34 GMT  
		Size: 26.5 MB (26549014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718f190d616a22230a70fd27a7a72386dafc4994834571fe3dd98c19265da676`  
		Last Modified: Wed, 14 Jun 2023 21:50:29 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef08201d74e5aa39b983fe90e919211b44f84b9bbe18bf35186b48c9e62bda60`  
		Last Modified: Wed, 14 Jun 2023 21:50:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6967807a7323b36e15ccd4d578f8bb8f44fb56dcf90df56c87b3330367bbe1f`  
		Last Modified: Wed, 14 Jun 2023 21:50:29 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:638dfa126c2923a8d813fc7f5bf48652bdd1ce335e5cfec4e4bcdfe9dda0899a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92142506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0738379acd46890b92ff70f8c0140c3a968647e44fdae0773627cec43cd8b71b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:58:47 GMT
ADD file:319a24b7e30fc548f9dcf48ad6cee469e8bf7e89c67901cf3851e41e75693489 in / 
# Mon, 12 Jun 2023 23:58:47 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 14:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 14:33:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 14:33:56 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 14:58:46 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 14:58:47 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 14:58:47 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 21:50:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 21:50:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 21:50:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 21:50:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 21:50:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 21:50:40 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 22:31:57 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 22:31:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 22:31:58 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 22:35:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 22:35:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 22:35:23 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 22:35:23 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 22:35:24 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 22:35:24 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 22:35:24 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 22:35:24 GMT
USER fluent
# Wed, 14 Jun 2023 22:35:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 22:35:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b7c295cb849275e211d18b720d2349cc84c0038be1a362aca4765ceb3342043c`  
		Last Modified: Tue, 13 Jun 2023 00:04:24 GMT  
		Size: 26.6 MB (26578690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999000f64bf28ef182f07e5f4ba36592dd2706cff1575d5f7ca90df97f79ab00`  
		Last Modified: Tue, 13 Jun 2023 15:16:19 GMT  
		Size: 8.1 MB (8141546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab00ea46680fc55ca887a14fced3aa27fae13c44b7352faa153ba339ae2b7139`  
		Last Modified: Tue, 13 Jun 2023 15:16:17 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1a83c629c9c8fccb8ae2505159e462aec0a767dff7f507dc7d239b9b56dc15`  
		Last Modified: Wed, 14 Jun 2023 22:10:25 GMT  
		Size: 31.0 MB (31035390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b8831b4b656f1ee08d25a3779ebf89b387af027fa9fd0007cc9fbe4be3a842`  
		Last Modified: Wed, 14 Jun 2023 22:10:20 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e18eae1bb80b57bd995c69a086475a7237466c7e7801838743320431603c1a`  
		Last Modified: Wed, 14 Jun 2023 22:35:46 GMT  
		Size: 26.4 MB (26383806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a675b3ef506729b9aa2c3e55073cd0c184bfd914943ea2da3368679106dc6862`  
		Last Modified: Wed, 14 Jun 2023 22:35:40 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27068cc9d6741a0b964932ebc24225407bdf7132b46cd17854caaa52a62764f`  
		Last Modified: Wed, 14 Jun 2023 22:35:40 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257abcec41581086b81dd4a4157539790488a4489e08a0e858082157d66f3e1a`  
		Last Modified: Wed, 14 Jun 2023 22:35:40 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:265290eac3a3b0e730962af326206b41548e5cdc4dc62eab0aefc61ad410dda2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98777554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084516af09ee1e692ccd5af3b49506735136d94e51ca501c994e7cfcf3a83321`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 13:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 13:07:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 13:07:21 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 13:24:06 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 13:24:06 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 13:24:07 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 20:13:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 20:13:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 20:13:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 20:13:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 20:13:15 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 20:13:15 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 20:44:02 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 20:44:02 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 20:44:02 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 20:46:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 20:46:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 20:46:20 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 20:46:20 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 20:46:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 20:46:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 20:46:20 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 20:46:20 GMT
USER fluent
# Wed, 14 Jun 2023 20:46:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 20:46:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6764f9140e90ce73f5fb4d2a65dcfe0fe6c9923b4258b62641cca67b8617d91f`  
		Last Modified: Tue, 13 Jun 2023 13:36:54 GMT  
		Size: 9.2 MB (9242110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bb19ae3f8d4635186d2a44346ad9d54f1fe0aee91d1a3795a8a53f76bb3fc0`  
		Last Modified: Tue, 13 Jun 2023 13:36:53 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6569f27e27c33ce56a0ea0cfcb75299cec795e3bd2b216c2575de9e8e8b175`  
		Last Modified: Wed, 14 Jun 2023 20:23:58 GMT  
		Size: 32.0 MB (31987325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ae9e9f387ec7cd850e6f15ef05379fc0adede2002f99fb51fe29478f737e`  
		Last Modified: Wed, 14 Jun 2023 20:23:56 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6579ab2a30a64f4f5a41f221348667791d7cee7314eae7a5376a51cbb50b0ebf`  
		Last Modified: Wed, 14 Jun 2023 20:46:34 GMT  
		Size: 27.5 MB (27482203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f4f1d04efa08cd66343efed3a25bc93f306843fcc43f69bd648ae543e0772`  
		Last Modified: Wed, 14 Jun 2023 20:46:31 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38885c8d68da579855553ce2827900bb2f10215ea317e931b23e0672c9f81d2`  
		Last Modified: Wed, 14 Jun 2023 20:46:31 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fcdbcc3ed11e024906fd5edd8cd6d005ab2aba38e3ca027d38ebe2fd8f93a0`  
		Last Modified: Wed, 14 Jun 2023 20:46:31 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d26fdb3de1a9fba3a67d64f2188514041596558b0fcc4bb297e31c69d4b796b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102170573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d761cf2ddfb6b92b77cf4bb86af8034be3d98300a5b087aa6bbc8ba312fd676`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:58 GMT
ADD file:440924fd31c090a7f5e3d36276d17574922eb3e8ececce333fa42f7a95bdd9ce in / 
# Mon, 12 Jun 2023 23:39:58 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 00:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 00:07:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 00:07:52 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 00:23:23 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 00:23:23 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 00:23:23 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 18:38:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 18:38:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 18:38:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 18:38:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 18:39:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 18:39:00 GMT
CMD ["irb"]
# Wed, 14 Jun 2023 22:14:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jun 2023 22:14:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Wed, 14 Jun 2023 22:14:11 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jun 2023 22:17:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Wed, 14 Jun 2023 22:17:12 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Wed, 14 Jun 2023 22:17:12 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Wed, 14 Jun 2023 22:17:12 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Wed, 14 Jun 2023 22:17:12 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jun 2023 22:17:12 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jun 2023 22:17:13 GMT
EXPOSE 24224 5140
# Wed, 14 Jun 2023 22:17:13 GMT
USER fluent
# Wed, 14 Jun 2023 22:17:13 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jun 2023 22:17:13 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1646137eb700afc9e891c03fdf28d3f5bc489ef0200fdacc67beee837d48db7d`  
		Last Modified: Mon, 12 Jun 2023 23:47:07 GMT  
		Size: 32.4 MB (32397388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae39782333ba3b6797929e1de5919e6f957f07c4bf4f388316b264ad2de47abd`  
		Last Modified: Tue, 13 Jun 2023 00:38:45 GMT  
		Size: 12.0 MB (11994868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbed6977b262b949787e1f257c80b388f10f3e706301cdf5ebcae6f87adb254`  
		Last Modified: Tue, 13 Jun 2023 00:38:41 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b58c6bd82e64852dedd16b0c9bf371668361a08456e2ae2a7fb54ff7696b99`  
		Last Modified: Wed, 14 Jun 2023 18:56:29 GMT  
		Size: 31.2 MB (31181698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1168f0602606a4764bd9199ce64d841467925d1424587cc20fb40dcffb62ef`  
		Last Modified: Wed, 14 Jun 2023 18:56:25 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1feb3eda883ea03c3920d608f2b8de848c5a0be279f8bf3cc473acf69a7f056`  
		Last Modified: Wed, 14 Jun 2023 22:17:32 GMT  
		Size: 26.6 MB (26593550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f55ee4d8d1db832ab044a310e1cdf37b943d19478ebe7603837839dc6316b0`  
		Last Modified: Wed, 14 Jun 2023 22:17:28 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002dcaacc2acb43ceaa709e771ecfedf2db1f77098386d5817b85007a52f6489`  
		Last Modified: Wed, 14 Jun 2023 22:17:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767512f5f03efe4aa3ee14779e556efc4478d70010b4c3e999f834f846a1dc21`  
		Last Modified: Wed, 14 Jun 2023 22:17:28 GMT  
		Size: 461.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:de4a254772d7baa6b6acaf231d087f91036436022712625540ffb1b151c4f22d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106775294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ecd7b2b5794f16aa691277c98b08d4bb09c10e9335785c232248240e09fb69`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jun 2023 23:18:20 GMT
ADD file:b17eabe509462fa1a2e4c5421e877e3e4149085e3da07a421a66c7b06566c457 in / 
# Mon, 12 Jun 2023 23:18:22 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 07:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:06:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 07:06:52 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 07:15:37 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 07:15:37 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 07:15:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Wed, 14 Jun 2023 23:30:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 14 Jun 2023 23:30:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jun 2023 23:30:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jun 2023 23:30:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 23:30:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 14 Jun 2023 23:30:09 GMT
CMD ["irb"]
# Thu, 15 Jun 2023 00:32:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 15 Jun 2023 00:32:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Thu, 15 Jun 2023 00:32:42 GMT
ENV TINI_VERSION=0.18.0
# Thu, 15 Jun 2023 00:37:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Thu, 15 Jun 2023 00:37:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Thu, 15 Jun 2023 00:37:55 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Thu, 15 Jun 2023 00:37:55 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Thu, 15 Jun 2023 00:37:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 15 Jun 2023 00:37:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 15 Jun 2023 00:37:56 GMT
EXPOSE 24224 5140
# Thu, 15 Jun 2023 00:37:56 GMT
USER fluent
# Thu, 15 Jun 2023 00:37:57 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 15 Jun 2023 00:37:57 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2973ac0be4a80a6cecbb73370e92810a6f67a98e12e61b3044aa63a322dab03a`  
		Last Modified: Mon, 12 Jun 2023 23:25:03 GMT  
		Size: 35.3 MB (35290790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba11d9646199a3947e54ff4f564451778648eefd9055af564c1038e730488cb4`  
		Last Modified: Tue, 13 Jun 2023 07:24:25 GMT  
		Size: 10.5 MB (10478333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d79ea6089ae4241c276607e8b544d5c626cf8223e52c3dd7a42d03c6a44ae98`  
		Last Modified: Tue, 13 Jun 2023 07:24:22 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dacdff1086d66ea2e321cd6dc456d8880416267dcd38492948bbfc77958fbe4`  
		Last Modified: Wed, 14 Jun 2023 23:42:09 GMT  
		Size: 32.8 MB (32791556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c55ccf4f31798e6eaf295778f2994f8cdf51dbe03e8d96dc9ecbad85465ee8`  
		Last Modified: Wed, 14 Jun 2023 23:42:04 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7f6aab677dfcab0b85f56a74bd03cd703b36c6ca8f7aa952461187e4995e83`  
		Last Modified: Thu, 15 Jun 2023 00:38:22 GMT  
		Size: 28.2 MB (28211535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d932948fb8dfa58cc95c0621ff2d5aa52c6f1e26516819322dd5de667c4452`  
		Last Modified: Thu, 15 Jun 2023 00:38:15 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98106a542a935a9d32cc61c0e0545150bc2de6d343a1529b996c274574742aa1`  
		Last Modified: Thu, 15 Jun 2023 00:38:15 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c33060818be3afe37d5177ab68aa46f5ce1d0fa1738731cd12ebb5ba27549f`  
		Last Modified: Thu, 15 Jun 2023 00:38:16 GMT  
		Size: 459.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fluentd:v1.16.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:3ea4a6edd4c873532726c47a17be26ed3ca7027055dfe1a5d4e1b6ab3589c9ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98901239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df46366c41abe4c0e894aa34298d2bb93d1ceb68b84a3fc459d7157d538327f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 13 Jun 2023 04:30:13 GMT
ADD file:558e8c34e969d458ce6bf4207d9c0fe05d2e67d3457c1d5689666749e82ef2ab in / 
# Tue, 13 Jun 2023 04:30:14 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 18:09:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 18:09:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 13 Jun 2023 18:09:07 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 18:14:11 GMT
ENV RUBY_MAJOR=3.1
# Tue, 13 Jun 2023 18:14:11 GMT
ENV RUBY_VERSION=3.1.4
# Tue, 13 Jun 2023 18:14:11 GMT
ENV RUBY_DOWNLOAD_SHA256=1b6d6010e76036c937b9671f4752f065aeca800a6c664f71f6c9a699453af94f
# Thu, 15 Jun 2023 16:23:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 16:23:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 16:23:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 16:23:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 16:23:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 16:23:38 GMT
CMD ["irb"]
# Fri, 16 Jun 2023 16:00:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 16 Jun 2023 16:00:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.0
# Fri, 16 Jun 2023 16:00:00 GMT
ENV TINI_VERSION=0.18.0
# Fri, 16 Jun 2023 16:02:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.14.2  && gem install json -v 2.6.3  && gem install rexml -v 3.2.5  && gem install async -v 1.30.3  && gem install async-http -v 0.56.6  && gem install fluentd -v 1.16.0  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test
# Fri, 16 Jun 2023 16:02:09 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd
# Fri, 16 Jun 2023 16:02:09 GMT
COPY file:06d9a84b9b428b4e0ef5a9e3699798758dc9716908d82091239fb9f85dd30d70 in /fluentd/etc/ 
# Fri, 16 Jun 2023 16:02:09 GMT
COPY file:977670d9d298d60208db6e5110a5919bfde19ee7da9c19df693163ecd07caea6 in /bin/ 
# Fri, 16 Jun 2023 16:02:09 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 16 Jun 2023 16:02:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 16 Jun 2023 16:02:10 GMT
EXPOSE 24224 5140
# Fri, 16 Jun 2023 16:02:10 GMT
USER fluent
# Fri, 16 Jun 2023 16:02:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 16 Jun 2023 16:02:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6a752e2308c741009b6f5a88a8ea6764b96ebe7f544197912d8ef9a3ec8c8763`  
		Last Modified: Tue, 13 Jun 2023 04:34:49 GMT  
		Size: 29.7 MB (29652514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324883160edf8f3ab5900f91d3562af2eb6fe2e5199bb0cf5466029297d8a685`  
		Last Modified: Tue, 13 Jun 2023 18:19:42 GMT  
		Size: 8.9 MB (8861927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3903959d9528f3e1013f3b14204e97e6b43ed28f73143ea14374e21dbf260cbd`  
		Last Modified: Tue, 13 Jun 2023 18:19:40 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42442750523fba0b3b1195c59f3424d6360fbe07a34e912f8a38dc73786a1e4e`  
		Last Modified: Thu, 15 Jun 2023 17:25:16 GMT  
		Size: 32.4 MB (32444923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b366d91a9011a26dc8e18532df71398718c7f8c91b8af69f3aa9d38ed5ed08e`  
		Last Modified: Thu, 15 Jun 2023 17:25:13 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7c3c84d330c977e441c794474e5024c79578d393b81c1f4319601b6911ee82`  
		Last Modified: Fri, 16 Jun 2023 16:02:41 GMT  
		Size: 27.9 MB (27938798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdccd2f69a2a1ca7c963c873a257091bb52bfd19a0205474db0ae15ea16f5fe8`  
		Last Modified: Fri, 16 Jun 2023 16:02:36 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1633ee4e3112b4e9d3837630b8345f37ada86287c1734d7bd53d9c8ce2b55a`  
		Last Modified: Fri, 16 Jun 2023 16:02:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fbefff65957dd4705fdc33cec4914bf818e19fc45e80f6bdd7269851e5ba42`  
		Last Modified: Fri, 16 Jun 2023 16:02:37 GMT  
		Size: 458.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
